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
  - I've had reports of hover preview not displaying Excalidraw drawings.
- [Header Enhance](https://github.com/HoBeedzc/obsidian-header-enhancer-plugin): when Auto numbering enabled toggle between Excalidraw and Markdown view mode does not function. [More info](https://forum.obsidian.md/t/excalidraw-full-featured-sketching-plugin-in-obsidian/17367/114)
- [Encore Theme](https://github.com/Carbonateb/obsidian-encore-theme/issues): The Excalidraw tools panel is not visible.
- [Style Settings plugin](https://github.com/mgmeyers/obsidian-style-settings/issues/115#issuecomment-2416514409). Navigation in Obsidian settings is sluggish. [More info](https://github.com/zsviczian/obsidian-excalidraw-plugin/issues/1826)
- [OmniSearch](https://github.com/scambier/obsidian-omnisearch) Significant performance degradation. [More info](https://github.com/zsviczian/obsidian-excalidraw-plugin/issues/2055#issuecomment-2401376219)
- [Math+](https://github.com/ocapraro/obsidian-math-plus) Some users have reported that after installing the plugin the Excalidraw toolbar disappeared.
- [Linter](https://github.com/platers/obsidian-linter) changes files in the background which can lead to corrupt Excalidraw files. For example the `lint on focus file change` option was reported as such a problematic setting. [#1715](https://github.com/zsviczian/obsidian-excalidraw-plugin/issues/1715#issuecomment-2571640643)

%%
# Excalidraw Data

## Text Elements
## Drawing
```compressed-json
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
```
%%