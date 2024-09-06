---
excalidraw-plugin: parsed
tags:
  - excalidraw
excalidraw-autoexport: svg
excalidraw-open-md: true
---
# [[Compatibility Issues - Plugins to Watch Out For]]

Here's a list of plugins that have caused performance issues or other problems when used in conjunction with Excalidraw:
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


%%
# Excalidraw Data
## Text Elements
## Drawing
```compressed-json
N4KAkARALgngDgUwgLgAQQQDwMYEMA2AlgCYBOuA7hADTgQBuCpAzoQPYB2KqATLZMzYBXUtiRoIACyhQ4zZAHoFAc0JRJQgEYA6bGwC2CgF7N6hbEcK4OCtptbErHALRY8RMpWdx8Q1TdIEfARcZgRmBShcZQUebQAWbQBGGjoghH0EDihmbgBtAF1+CFw4OABlKKhxVFAwSHUMmogiZWlU+oZCBAoAIVxsAGtlUmEOYgBhNnw2Um4IAGIAMxXV

jshsEUDsgElq/UrRwYQpmbmJBaSEK6v1iE3Sbag9jP6hkbHJ6dn5qHIOZhwXBPO4PJ4vfQAMUI+HwlRgwXmgg8oK2WWe+0ObGOAHUSOpuHxwBs0btMX9sQh4YiJMiSKjHuiIQAlYRtDjhXJoJL8EmMskZADyQOwahg3CSAAZJbz7qSMRlIZwoJDcPoYeK0ABWWVgpn7JXZcqEIw1Hgy4ly/kK/QAFSwUAAgq0uBJgksoAzweTgU7HmwKJIQsRuBw

hLDdfKIQBRcaO/2B4PzYGjKiR60Q+Op23wZqjITjO7MbCjWEADW4AGYAGxJbQ6y3F0v4ACa3HiAE44g3OkY2AZuHVOvQCEIakliQBfdPejKsgvEDnMLnofOF2UjEjG02Ei2dTfESoIODcHuQA8AWTYxAQsdwmmCIbQSwIYQ3pBIpx+aCHkF60yfdAFgmDsQJA9ZIGZBBlHDYF5gWaMABEkKQiApxndEsWOYUoHYAFQ3DfBZSWchMig8YmEIDhlEH

YlICye9H24P4x15DYiBPNAWIQNiIA4NUam43jhCgIgOWY0gx3Qy07AAKwQbAcnKfi4CvG87wfBBAJffA30tAZcMYW1+3wWj6gaXMkXSRS8IguVmCgAwc0QAiIzolo2CGLTuB0vTzJaUInRsoyTNc/Ap3Aac6CWGFwkHScQEnIA==
```
%%