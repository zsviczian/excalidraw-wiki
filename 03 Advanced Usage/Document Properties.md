---
excalidraw-plugin: parsed
tags:
  - excalidraw
excalidraw-autoexport: svg
excalidraw-open-md: true
excalidraw-export-transparent: true

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
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=
```
%%