This is an advanced version of the template Nicole is using in her video here: 
![Why I changed all my templates](https://youtu.be/zmgqMZi6QL8?t=950)

This template assumes you have [Templater](https://github.com/SilentVoid13/Templater) installed and configured to fire for new file creation. The below template will create an Excalidraw file that 
- by default will open in markdown mode, 
- but you can toggle to open in Excalidraw View mode using the command palette action `Excalidraw: Toggle between Excalidraw and Markdown mode` 
- when you save the file in Excalidraw mode, the file will auto-export an svg with the same name
- the template creates a tiny dummy SVG file so when you rename your new "Untitled" note, "Untitled.svg" follows this name change.

How to use the snippet below:
1. Copy the below markdown block to an empty note (make sure your empty note does not have any document properties or switch Obsidian Editor to Properties in Source mode to be sure).
2. Be sure to replace the escaped ticks by removing the ` \ ` escape characters (there are 6 in total, 3 next to `json` and 3 at the end right before the second `%%`.

```markdown
---
excalidraw-plugin: parsed
excalidraw-open-md: true
excalidraw-autoexport: svg
---

# [[<% tp.file.title%>]]

![[<% tp.file.title%>.svg]]
<%*
  const path = (tp.file.folder() === "" ? "" : `${tp.file.folder()}/`) + `${tp.file.title}.svg`;
  if(!app.vault.getAbstractFileByPath(path)) {
	app.vault.create(path, `<svg version="1.1" xmlns="http://www.w3.org/2000/svg" width="0" height="0"></svg>`);
  }
%>

%%
# Excalidraw Data
## Text Elements
## Drawing
\`\`\`json
{"type":"excalidraw","version":2,"source":"","elements":[],"appState":{}}
\`\`\`
%%
```