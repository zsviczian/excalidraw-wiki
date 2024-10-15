---
excalidraw-plugin: parsed
tags:
  - excalidraw
excalidraw-autoexport: svg
excalidraw-open-md: true
aliases:
  - wiki/color-palette
---
# [[WIKI/03 Advanced Usage/Color Palette]]
You can define your custom color palettes. The steps are a bit technical, however, once you've set up the Color Palette, you can [[Create your Template]], load the palette to the template, and all your new Excalidraw documents will have your custom color palette.

You will find the [Palette Loader Script](https://github.com/zsviczian/obsidian-excalidraw-plugin/blob/master/ea-scripts/Palette%20loader.md) in the Excalidraw Automate [[Script Library]].

These two videos explain how to set up a color palette:
![Color Picker](https://youtu.be/diBT5iaoAYo)

Link:: [Color Picker Video](https://youtu.be/diBT5iaoAYo)

![Palette Loader](https://youtu.be/epYNx2FSf2w)

Link:: [Palette Loader Video](https://youtu.be/epYNx2FSf2w)
## Structure of the palette file
Here's a sample palette file. The 6 digit hexadecimal values listed one after the other in new rows are the colors. Notice how they are in batches of 5, matching the palette in Excalidraw. Notice also that the numbers do not have the "#" sign at the front.

There are two things you need to understand about the sequence of the colors.
- The first batch is the first row of colors in the picker, the second the second, etc. You can have as many batches as you'd like.
- The batches of 5 are tricky. Colors are in the order of 3-1-2-4-5, that is, the middle color is the first in the sequence. The strange sequence has historical reasons... now, it cannot be changed else impacting backwards compatibility.

Notice also that you can add lines with non-color codes to your file. Palette Loader will skip these. You can use these lines to store the original palette definition should you need to go back to it later.
```
source:: [Paletton Palette](https://paletton.com/#uid=43j0t0kpSAtfHMQl6FTy1xHyjol)
22A5AB
6CCED2
41B7BC
01989F
017075

FFBA31
FFD582
FFC757
FFAA00
C28100

FF3B31
FF8882
FF5F57
FF0D00
C20A00

FF9031
FFBC82
FFA557
FF7600
C25A00
```

The palette in the file above looks like this:
![[Screenshot - Demo Palette.png|200]]

The colors in the first row of the palette are automatically generated. The two grays are tinted based on the middle color of the first first row of your palette: "d" in the screenshot above.

### The Palettes Folder
The palette file is a simple markdown file placed in the Palettes Folder. By Default it is the `Excalidraw/Palettes` folder. After downloading the [[Palette Loader Script]] you need to run it from Obsidian Command Palette. At the first run, the script will register a custom settings section at the bottom of Excalidraw Plugin Settings. You may configure the palette folder here. Note, that foler names are CasE seNSitIVe. You may also define the light and dark gray values used by the script to create the tinted grays in the palette as mentioned above.

![[Screenshot - Plugin Settings - Palette Loader Settings.jpeg]]
## Designing your Palette
You can design your palette at http://paletton.com/
![[Screenshot - Paletton Config Screen.jpeg]]

Once you are happy with the colors you need to export the palette. 

The easiest option is to click Tables/Export in the bottom right of the screen - **However, unfortunately, this feature often does not work :(** If you run into issues you'll find alternative approaches further below

1) Click the "Tables/Export" button as shown on the screenshot above.
2) On the next screen click "as text". You will need to manually delete "#" from the exported values, and format the file to match the example above, but it only takes a minute.

![[Screenshot - Paletton Export Screen.jpeg]]
### In case "as text" does not work
You have two options in case "as text" does not work.
#### Option 1 - Manually copy values into a text file
Open a new note in Obsidian and type in the values from the export screen. Don't forget, in each row the middle value comes first, then the first, second, fourth and fifth. This should take no more than 5 minutes.

#### Option 2 - Use script to extract the values
If you are comfortable with scripting you can follow the below approach. However, note, that sometimes the structure of the Paletton page changes, in this case you may need to tweak the code a bit.

![[Screenshot - Paletton Export with Code.jpeg]]

0. On the palette configuration page press CTRL+SHIFT+i or (CMD+OPT+i on a Mac).
1. Click "Console"
2. Paste the below script. Note, if you have not pasted script to console before you will be prompted with a warning. You need to type: "allow pasting".
3. Paste the code and run it. If you run into an error, then Paletton has likely changed something. You can try to figure out the change using the Elements browser. At this point your on your own. You are probably better off manually copying the values to a text file as per the previous point.
4. Select the result, copy it to the clipboard and paste it to your palette file in Obsidian.

Here's the script you want to run:
```javascript
s=`source:: [Paletton Palette](${window.location.href})`;
document
  .querySelector(".pane.pane-palette")
  .querySelectorAll("[title]")
  .forEach((x,i)=>{
    s += `\n${x.getAttribute("title")}`;
    if((i+1)%5===0) s+="\n";
  })
console.log(s)
```

## The Excalidraw appState Custom Palette Data Object
The Excalidraw drawing is stored in a JSON data structure under Excalidraw Data / Drawing. You can find this JSON by switching to [[Markdown View]] and selecting [[Decompress current Excalidraw File]] from the Obsidian Command Palette (in case you see [[compressed-json]] in the [[Drawing Section]] of the file).

The color palette is at the end of the JSON in the `appState` section. This is its structure:

```js
colorPalette: {
  canvasBackground: [string, string, string, string, string][] | string[],
  elementBackground: [string, string, string, string, string][] | string[],
  elementStroke: [string, string, string, string, string][] | string[],
  topPicks: {
    canvasBackground: [string, string, string, string, string],
    elementStroke: [string, string, string, string, string],
    elementBackground: [string, string, string, string, string] 
  },
}
```

Finally there is a GitHub Gist with the code. In case of questions you might find answers [here](https://gist.github.com/zsviczian/28b0864569ae50a59a65c3bd23e35c1a)

%%
# Excalidraw Data
## Text Elements
## Drawing
```compressed-json
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
```
%%