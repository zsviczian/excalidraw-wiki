---
excalidraw-plugin: parsed
tags:
  - excalidraw
excalidraw-autoexport: svg
excalidraw-open-md: true
excalidraw-export-transparent: true
aliases:
  - WIKI/03+Advanced+Usage/Document+Properties
permalink: wiki/properties
---
# [[Document Properties]]

Excalidraw document properties control Excalidraw's behavior at a file level. These properties override plugin settings for the document. Properties offer some very powerful file level customization opportunities or even, like in the case of "onload-script" scripted automation.

| Property                      | Type     | Description                                                                                                                                                                                                                                                          | Example                                                               |
| ----------------------------- | -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| excalidraw-autoexport         | text     | Override autoexport settings for this file. Valid values are: `none \| both \| png \| svg`<br>                                                                                                                                                                       | png                                                                   |
| excalidraw-border-color       | text     | This key applies to Markdown Embeds. You can control the appearance of the embedded markdown file on a file by file bases by adding the this frontmatter key to your markdown document. Valid values are: css-color-name\|\#HEXcolor\|any-other-html-standard-format | SteelBlue                                                             |
| excalidraw-css                | text     | This key applies to Markdown Embeds. You can control the appearance of the embedded markdown file on a file by file bases by adding the this front matter keys to your markdown document. Valid values are: "css-filename\|css snippet"                              | ""                                                                    |
| excalidraw-default-mode       | text     | Specifies how Excalidraw should open by default. Valid values are: view\|zen                                                                                                                                                                                         | view                                                                  |
| excalidraw-embeddable-theme   | text     | Override embeddable's theme plugin-settings for this file. 'auto' will match the Excalidraw theme, 'default' will match the Obsidian theme. Valid values are: `dark \| light \| auto \| default`<br>                                                                 | auto                                                                  |
| excalidraw-export-dark        | checkbox | If this key is present it will override the default excalidraw embed and export setting. true == Dark mode / false == light mode                                                                                                                                     | true                                                                  |
| excalidraw-export-embed-scene | checkbox | If this key is present it will override the default excalidraw embed and export setting.                                                                                                                                                                             | false                                                                 |
| excalidraw-export-padding     | number   | If this key is present it will override the default excalidraw embed and export setting. This only affects both SVG and PNG export. Specify the export padding for the image.                                                                                        | 5                                                                     |
| excalidraw-export-pngscale    | number   | If this key is present it will override the default excalidraw embed and export setting. This only affects export to PNG. Specify the export scale for the image. The typical range is between 0.5 and 5, but you can experiment with other values as well.          | 1                                                                     |
| excalidraw-export-transparent | checkbox | If this key is present it will override the default excalidraw embed and export setting. true == Transparent / false == with background                                                                                                                              | true                                                                  |
| excalidraw-font               | text     | This key applies to Markdown Embeds. You can control the appearance of the embedded markdown file on a file by file bases by adding the this frontmatter key to your markdown document. Valid values are: Virgil\|Cascadia\|font_file_name.extension                 | Virgil                                                                |
| excalidraw-font-color         | text     | This key applies to Markdown Embeds. You can control the appearance of the embedded markdown file on a file by file bases by adding the this frontmatter key to your markdown document. Valid values are: css-color-name\|\#HEXcolor\|any-other-html-standard-format | SteelBlue                                                             |
| excalidraw-link-brackets      | checkbox | Set to true, if you want to display [\[square brackets]] around the links in Text Elements                                                                                                                                                                           | true                                                                  |
| excalidraw-link-prefix        | text     | Set custom prefix to denote text element containing a valid internal link. Set to empty string if you do not want to show a prefix                                                                                                                                   | "📍"                                                                  |
| excalidraw-linkbutton-opacity | number   | The opacity of the blue link button in the top right of the element overriding the respective setting in plugin settings. Valid values are between 0 and 1, where 0 means the button is transparent.                                                                 | 0.5                                                                   |
| excalidraw-mask               | checkbox | If this key is present the drawing will be handled as a mask to crop an image.                                                                                                                                                                                       | true                                                                  |
| excalidraw-onload-script      | text     | The value of this field will be executed as javascript code using the Script Engine environment. Use this to initiate custom actions or logic when loading your drawing.                                                                                             | "new Notice(`Hello World!\n\nFile: ${ea.targetView.file.basename}`);" |
| excalidraw-open-md            | checkbox | If this key is present the file will be opened as a markdown file in the editor                                                                                                                                                                                      | true                                                                  |
| excalidraw-plugin             | text     | Denotes an excalidraw file. If key is not present, the file will not be recognized as an Excalidarw file. Valid values are 'parsed' and 'raw'                                                                                                                        | parsed                                                                |
| excalidraw-url-prefix         | text     | Set custom prefix to denote text element containing a valid external link. Set to empty string if you do not want to show a prefix                                                                                                                                   | "🌐"                                                                  |


%%
# Excalidraw Data

## Text Elements
## Drawing
```compressed-json
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
```
%%