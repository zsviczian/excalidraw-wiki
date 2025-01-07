---
permalink: wiki/prompt-for-rename
---
# Prompt for Filename When File Is Excalidraw Drawing is Created

> How can I set up that I can manually input the drawing name / filename when the excalidraw drawing is created?

> Right now when i create an excalidraw drawing, it's filename is pretty much the date created, which is pretty useless for identifying the drawing. I have to manually go back and rename it. Is it possible to have it ask for the file name that I want, every time I create a drawing?

This is a question I've received many times.... so here's a short overview of the solution.

Excalidraw publishes a number of events (or hooks). You can attach to these events by creating a startup script.

![[Screenshot - Setting up Excalidraw Startup Script.png]]

One of these hooks is the `onFileCreateHook`. Simply attach the below one liner code to this hook.

```js
/**
 * if set, this callback is triggered, when an Excalidraw file is created
 * see also: https://github.com/zsviczian/obsidian-excalidraw-plugin/issues/1124
 *   onFileCreateHook: (data: {
 *     ea: ExcalidrawAutomate;
 *     excalidrawFile: TFile; //the file being created
 *     view: ExcalidrawView;
 *   }) => Promise<void>;
 */
ea.onFileCreateHook = (data) => {
  app.fileManager.promptForFileRename(data.excalidrawFile);
};
```

## Steps
1. Create or open your startup script from plugin settings
2. Update the script as described above
3. Restart Obsidian for the startup script to take effect
4. Enjoy!  🎉🥳🍾

## Advanced usage
Of course, using the same hook you could also add any custom logic here. For example, if you'd want you could automatically rename the file based on some criteria. Here's a boilerplate for renaming the file based on the host file, the file into which you've just inserted the drawing using the [[Command Palette Actions|Command Palette Action]]: `Exalidraw: Create new .... and embed ...`)

```js
ea.onFileCreateHook = (data) => {
  const backlinks = getBacklinks(data.excalidrawFile);
  if(backlinks.length !== 1) {
    //if there are no files, or multiple files prompt for name
    app.fileManager.promptForFileRename(data.excalidrawFile);
    return;
  }
  const hostFile = backlinks[0];
  //do your magic
  const newFilePath = data.excalidrawFile.path;

  //rename the file
  app.fileManager.renameFile(data.excalidrawFile, newFilePath);
}

function getBacklinks(file) {
  const backlinks = app.metadataCache.resolvedLinks;

  const linkedFiles = Object.entries(backlinks)
    .filter(([sourcePath, links]) => links[file.path])
    .map(([sourcePath]) => app.vault.getFileByPath(sourcePath));

  return linkedFiles;
}
```