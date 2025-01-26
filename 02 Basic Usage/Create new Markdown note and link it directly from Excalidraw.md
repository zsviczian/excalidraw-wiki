---
excalidraw-plugin: parsed
tags:
  - excalidraw
excalidraw-autoexport: svg
excalidraw-open-md: true
permalink: wiki/Create-new-note
---

# [[Create new Markdown note and link it directly from Excalidraw]]

As explained in [this](https://github.com/zsviczian/obsidian-excalidraw-plugin/issues/2008) issue there are multiple ways to create a new note on the spot from Excalidraw.

## Converting a block of text already present

Using a block of text already present in the sketch, you can use the "Convert to file" option of the context menu (right click after selecting the element):
![[Screenshot - Create file on the spot Convert to file option.png|500]]
This will prompt to insert a name for the file, after that it will save the note in the Excalidraw directory. After that an editable preview of the file will appear in the drawing:
![[Screenshot - Create file on the spot Editable preview.png|500]]

## Linking to a non existent note

If you create a link with the usual wiki-link syntax (`[[FILENAME]]`) to a note that does not exist, the moment you try to navigate to it you will be prompted to choose between the various options:
![[Screenshot - Create file on the spot Link to non existent note.png|500]]
- `Embed MD` will create a new note and embed an editable preview like in the [[#Converting a block of text already present|previous]] section
- `Create MD` will create a new note and link the text to it
- `Create EX` will create a new Excalidraw and link the text to it
- `Nevermind` will dismiss the popup

All of the option other than `Nevermind` will create a file with the same name as the initial link

## Using Excalidraw Automate scripts

### Creating a new note

Using the `Create new markdown file and embed into active drawing` script (available at [this](https://github.com/zsviczian/obsidian-excalidraw-plugin/blob/master/ea-scripts/Create%20new%20markdown%20file%20and%20embed%20into%20active%20drawing.md) link or in the script manager) you can create a new note, after being prompted for the title, and it will be embedded in the drawing as an image that updates if the note content is changed:
![[Screenshot - Create file on the spot File content image.png|500]]

### Extracting part of a note into

Using the `Deconstruct selected elements into new drawing` script (available at [this](https://github.com/zsviczian/obsidian-excalidraw-plugin/blob/master/ea-scripts/Deconstruct%20selected%20elements%20into%20new%20drawing.md) link or in the script manager) you can select part of the drawing and extrapolate it to a new note after being prompted for the name and the eventual template to use.
Initial drawing on the left with extrapolated part selected and new drawing on the right:
![[Screenshot - Create file on the spot Extrapolate some elements to new drawing.png|800]]


%%
# Excalidraw Data
## Text Elements
## Drawing
```compressed-json
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
```
%%