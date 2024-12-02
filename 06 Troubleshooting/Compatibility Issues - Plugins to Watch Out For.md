---
excalidraw-plugin: parsed
tags:
  - excalidraw
excalidraw-autoexport: svg
excalidraw-open-md: true
aliases:
  - WIKI/06+Troubleshooting/Compatibility+Issues+-+Plugins+to+Watch+Out+For
permalink: wiki/troubleshooting/compatibility
---
# [[Compatibility Issues - Plugins to Watch Out For]]

Here's a list of plugins and themes that have caused performance issues or other problems when used in conjunction with Excalidraw:
- [Typing Transformer](https://github.com/aptend/typing-transformer-obsidian): text in embedded markdown files is blurred. [#1990](https://github.com/zsviczian/obsidian-excalidraw-plugin/issues/1990)
- [Columns](https://github.com/tnichols217/obsidian-columns): Excalidraw drawings do not render in markdown. [#1896](https://github.com/zsviczian/obsidian-excalidraw-plugin/issues/1896)
- [Templater](https://github.com/SilentVoid13/Templater)
  - Templater scripts only work on markdown files not on Excalidraw files [#1512](https://github.com/zsviczian/obsidian-excalidraw-plugin/issues/1512)
    - But Templater scripts do work inside markdown embeddables inside Excalidraw
    - You can create ExcalidrawAutomate scripts for automating Excalidraw operations
  - Syntax highlighting results in very slow markdown file editing for back-of-the-drawing markdown notes on the back of large canvases. Turning off Templater Syntax Highlighting in plugin settings improves performance
- [Make.md](https://github.com/Make-md/makemd): Excalidraw + Make.md plugin breaks Obsidian Quick Switcher function to create and switch to files clicked on quick switcher view [#1498](https://github.com/zsviczian/obsidian-excalidraw-plugin/issues/1498)
- [Obsidian Link Opener](https://github.com/zorazrr/obsidian-link-opener): More tools dropdown does not work in Excalidraw [#1402](https://github.com/zsviczian/obsidian-excalidraw-plugin/issues/1402)
- [Metadata Menu](https://github.com/mdelobelle/metadatamenu): Performance impact across Obsidian if Metadata Menu and Excalidraw are both enabled. There is more information on this issue [here](https://github.com/mdelobelle/metadatamenu/issues/660) [#1744](https://github.com/zsviczian/obsidian-excalidraw-plugin/issues/1744)
- [Minimal Theme](https://github.com/kepano/obsidian-minimal)
  - Text in Excalidraw menus not readable, buttons are black. You can turn on Dynamic Styling in Excalidraw plugin settings under Appearance and Behavior > Theme and Styling which will override Minimal Theme's styling for Excalidraw.
  - Performance impact, when Excalidraw and Minimal Theme are both installed Obsidian becomes laggier. 
  - Size parameter of embedded Excalidraw drawing doesn't work with Minimal Theme Settings enabled [#2000](https://github.com/zsviczian/obsidian-excalidraw-plugin/issues/2000)
- [Header Enhance](https://github.com/HoBeedzc/obsidian-header-enhancer-plugin): when Auto numbering enabled toggle between Excalidraw and Markdown view mode does not function. [More info](https://forum.obsidian.md/t/excalidraw-full-featured-sketching-plugin-in-obsidian/17367/114)
- [Encore Theme](https://github.com/Carbonateb/obsidian-encore-theme/issues): The Excalidraw tools panel is not visible.
- [Style Settings plugin](https://github.com/mgmeyers/obsidian-style-settings/issues/115#issuecomment-2416514409). Navigation in Obsidian settings is sluggish. [More info](https://github.com/zsviczian/obsidian-excalidraw-plugin/issues/1826)
- [OmniSearch](https://github.com/scambier/obsidian-omnisearch) Significant performance degradation. [More info](https://github.com/zsviczian/obsidian-excalidraw-plugin/issues/2055#issuecomment-2401376219)
- [Math+](https://github.com/ocapraro/obsidian-math-plus) Some users have reported that after installing the plugin the Excalidraw toolbar disappeared.


%%
# Excalidraw Data
## Text Elements
## Drawing
```compressed-json
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=
```
%%