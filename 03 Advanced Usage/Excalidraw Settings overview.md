---
excalidraw-plugin: parsed
tags:
  - excalidraw
excalidraw-autoexport: svg
excalidraw-open-md: true
excalidraw-export-transparent: true
aliases:
  - wiki/settings
---
# [[Excalidraw Settings overview]]

Excalidraw plugin settings can be a daunting experience. There are so many things you can do, and it can be hard to find the right setting. Below is a copy/paste of the settings page. This way you can atleast search in settings. I hope someone will pick this up and transform it into a well structured reference of all the great plugin features.

![[Be Part of the Story!.svg]]

# Basic

In the "Basic" settings, you can configure options such as displaying release notes after updates, receiving plugin update notifications, setting the default location for new drawings, specifying the Excalidraw folder for embedding drawings into active documents, defining an Excalidraw template file, and designating an Excalidraw Automate script folder for managing automation scripts.

##### Display Release Notes after update

**Toggle ON:** Display release notes each time you update Excalidraw to a newer version.  
**Toggle OFF:** Silent mode. You can still read release notes on [GitHub](https://github.com/zsviczian/obsidian-excalidraw-plugin/releases).

##### Plugin update notification

**Toggle ON:** Show a notification when a new version of the plugin is available.  
**Toggle OFF:** Silent mode. You need to check for plugin updates in Community Plugins.

##### Excalidraw folder

Default location for new drawings. If empty, drawings will be created in the Vault root.

##### Use Excalidraw folder when embedding a drawing into the active document

Define which folder to place the newly inserted drawing into when using the command palette action: 'Create a new drawing and embed into active document'.  
**Toggle ON:** Use Excalidraw folder  
**Toggle OFF:** Use the attachments folder defined in Obsidian settings.

##### Crop file folder

Default location for new drawings created when cropping an image. If empty, drawings will be created following the Vault attachments settings.

##### Image annotation file folder

Default location for new drawings created when annotating an image. If empty, drawings will be created following the Vault attachments settings.

##### Excalidraw template file or folder

Full filepath or folderpath to the Excalidraw template.  
**Template File:**E.g.: If your template is in the default Excalidraw folder and its name is Template.md, the setting would be: Excalidraw/Template.md (or just Excalidraw/Template - you may omit the .md file extension). If you are using Excalidraw in compatibility mode, then your template must be a legacy Excalidraw file as well such as Excalidraw/Template.excalidraw.  
**Template Folder:** You can also set a folder as your template. In this case you will be prompted which tempalte to use when creating a new drawing.  
**Pro Tip:** If you are using the Obsidian Templater plugin, you can add Templater code to your different Excalidraw templates to automate configuration of your drawings.

##### Excalidraw Automate script folder (CASE SeNSitiVE!)

The files you place in this folder will be treated as Excalidraw Automate scripts. You can access your scripts from Excalidraw via the Obsidian Command Palette. Assign hotkeys to your favorite scripts just like to any other Obsidian command. The folder may not be the root folder of your Vault.

# Saving

In the 'Saving' section of Excalidraw Settings, you can configure how your drawings are saved. This includes options for compressing Excalidraw JSON in Markdown, setting autosave intervals for both desktop and mobile, defining filename formats, and choosing whether to use the .excalidraw.md or .md file extension.

##### Compress Excalidraw JSON in Markdown

By enabling this feature Excalidraw will store the drawing JSON in a Base64 compressed format using the [LZ-String](https://pieroxy.net/blog/pages/lz-string/index.html) algorithm. This will reduce the chance of Excalidraw JSON cluttering your search results in Obsidian. As a side effect, this will also reduce the filesize of Excalidraw drawings. When you switch an Excalidraw drawing to Markdown view, using the options menu in Excalidraw, the file will be saved without compression, so that you can read and edit the JSON string. The drawing will be compressed again once you switch back to Excalidraw view. The setting only has effect 'point forward', meaning, existing drawings will not be affected by the setting until you open them and save them.  
**Toggle ON:** Compress drawing JSON  
**Toggle OFF:** Leave drawing JSON uncompressed

##### Decompress Excalidraw JSON in Markdown View

By enabling this feature Excalidraw will automatically decompress the drawing JSON when you switch to Markdown view. This will allow you to easily read and edit the JSON string. The drawing will be compressed again once you switch back to Excalidraw view and save the drawing (CTRL+S).  
I recommend switching this feature off as it will result in smaller file sizes and avoiding unnecessary results in Obsidian search. You can always use the 'Excalidraw: Decompress current Excalidraw file' command from the command palette to manually decompress the drawing JSON when you need to read or edit it.

##### Interval for autosave on Desktop

The time interval between saves. Autosave will skip if there are no changes in the drawing. Excalidraw will also save the file when closing a workspace tab or navigating within Obsidian, but away from the active Excalidraw tab (i.e. clicking on the Obsidian ribbon or checking backlinks, etc.). Excalidraw will not be able to save your work when terminating Obsidian directly either by killing the Obsidian process, or clicking to close Obsidian altogether.

- Very frequent (every 15 seconds)
- Frequent (every 30 seconds)
- Moderate (every 60 seconds)
- Rare (every 5 minutes)
- Practically never (every 15 minutes)

##### Interval for autosave on Mobile

I recommend a more frequent interval for Mobiles. Excalidraw will also save the file when closing a workspace tab or navigating within Obsidian, but away from the active Excalidraw tab (i.e. tapping on the Obsidian ribbon or checking backlinks, etc.). Excalidraw will not be able to save your work when terminating Obsidian directly (i.e. swiping it away). Also note, that when you switch apps on a Mobile device, sometimes Android and iOS closes Obsidian in the background to save system resources. In such a case Excalidraw will not be able to save the latest changes.

- Very frequent (every 10 seconds)
- Frequent (every 20 seconds)
- Moderate (every 30 seconds)
- Rare (every 1 minute)
- Practically never (every 5 minutes)

## Filename

Click this link for the [date and time format reference](https://momentjs.com/docs/#/displaying/format/).

Filename for a new drawing is: [Excalidraw 2024-09-09 18.05.md](https://www.youtube.com/channel/UCC0gns4a9fhVkGkngvSumAQ)  
Filename for a new embedded drawing is: [{NOTE_NAME}2024-09-09 18.05.md](https://www.youtube.com/channel/UCC0gns4a9fhVkGkngvSumAQ)

##### Filename prefix

The first part of the filename

##### Filename prefix when embedding a new drawing into a markdown note

Should the filename of the newly inserted drawing start with the name of the active markdown note when using the command palette action: `Create a new drawing and embed into active document`?  
**Toggle ON:** Yes, the filename of a new drawing should start with filename of the active document  
**Toggle OFF:** No, filename of a new drawing should not include the filename of the active document

##### Custom text after markdown Note's name when embedding

Affects filename only when embedding into a markdown document. This text will be inserted after the note's name, but before the date.

##### Filename Date

The last part of the filename. Leave empty if you do not want a date.

##### .excalidraw.md or .md

This setting does not apply if you use Excalidraw in compatibility mode, i.e. you are not using Excalidraw markdown files.  
**Toggle ON:** filename ends with .excalidraw.md  
**Toggle OFF:** filename ends with .md

##### Crop file prefix

The first part of the filename for new drawings created when cropping an image. If empty the default 'cropped_' will be used.

##### Annotation file prefix

The first part of the filename for new drawings created when annotating an image. If empty the default 'annotated_' will be used.

##### Preserve image size when annotating

When annotating an image in markdown the replacment image link will include the width of the original image.

# AI Settings - Experimental

In the "AI" settings, you can configure options for using OpenAI's GPT API. While the OpenAI API is in beta, its use is strictly limited — as such we require you use your own API key. You can create an OpenAI account, add a small credit (5 USD minimum), and generate your own API key. Once API key is set, you can use the AI tools in Excalidraw.

##### OpenAI API key

You can get your OpenAI API key from your [OpenAI account](https://platform.openai.com/api-keys).

##### Default AI model

The default AI model to use when generating text. This is a freetext field, so you can enter any valid OpenAI model name. Find out more about the available models on the [OpenAI website](https://platform.openai.com/docs/models).

##### Default AI vision model

The default AI vision model to use when generating text from images. This is a freetext field, so you can enter any valid OpenAI model name. Find out more about the available models on the [OpenAI website](https://platform.openai.com/docs/models).

##### Default Image Generation AI model

The default AI model to use when generating images. Image editing and variations are only supported by dall-e-2 at this time by OpenAI, for this reason dall-e-2 will automatically be used in such cases regardless of this setting.  
This is a freetext field, so you can enter any valid OpenAI model name. Find out more about the available models on the [OpenAI website](https://platform.openai.com/docs/models).

##### OpenAI API URL

The default OpenAI API URL. This is a freetext field, so you can enter any valid OpenAI API compatible URL. Excalidraw will use this URL when posting API requests to OpenAI. I am not doing any error handling on this field, so make sure you enter a valid URL and only change this if you know what you are doing.

# Excalidraw appearance and behavior

In the 'appearance and behavior' section of Excalidraw Settings, you can fine-tune how Excalidraw appears and behaves. This includes options for dynamic styling, left-handed mode, matching Excalidraw and Obsidian themes, default modes, and more.

##### Pen mode

Should pen mode be automatically enabled when opening Excalidraw?

- Never
- On Obsidian Mobile
- Always

##### Enable double-tap eraser in pen mode

##### Show (+) crosshair in pen mode

Show crosshair in pen mode when using the freedraw tool. **Toggle ON:** SHOW **Toggle OFF:** HIDE  
The effect depends on the device. Crosshair is typically visible on drawing tablets, MS Surface, but not on iOS.

Render as image when in markdown reading mode of an Excalidraw file

When you are in markdown reading mode (aka. reading the back side of the drawing) should the Excalidraw drawing be rendered as an image? This setting will not affect the display of the drawing when you are in Excalidraw mode or when you embed the drawing into a markdown document or when rendering hover preview.  

- See other related setting for [PDF Export](#PDFExport) under 'Embedding and Exporting' further below.

  
You must close the active excalidraw/markdown file and reopen it for this change to take effect.

##### Render Excalidraw file as an image in hover preview...

...even if the file has the **excalidraw-open-md: true** frontmatter key.  
When this setting is off and the file is set to open in md by default, the hover preview will show the markdown side of the document.

##### Left-handed mode

Currently only has effect in tray-mode. If turned on, the tray will be on the right side.  
**Toggle ON:** Left-handed mode.  
**Toggle OFF:** Right-handed moded

##### Show splash screen in new drawings

## Hotkey overrides

Some of the Excalidraw hotkeys such as `CMD+Enter` to edit text or `CMD+K` to create an element link conflict with Obsidian hotkey settings. The hotkey combinations you add below will override Obsidian's hotkey settings while useing Excalidraw, thus you can add `CMD+G` if you want to default to Group Object in Excalidraw instead of opening Graph View.

**Code:** Mod + ENTER | **Apple:** CMD + ENTER | **Windows:** CTRL + ENTER

**Code:** Mod + K | **Apple:** CMD + K | **Windows:** CTRL + K

**Code:** Mod + G | **Apple:** CMD + G | **Windows:** CTRL + G

**Code:** Alt + ARROWLEFT | **Apple:** OPTION + ARROWLEFT | **Windows:** ALT + ARROWLEFT

**Code:** Alt + ARROWRIGHT | **Apple:** OPTION + ARROWRIGHT | **Windows:** ALT + ARROWRIGHT

## Theme and styling

##### Dynamic styling

Change Excalidraw UI colors to match the canvas color

- Dynamic Styling OFF
- Match color
- Gray, match tone

##### Markdown embeds to match Excalidraw theme

**Toggle ON:** Set this to true if for example you are using Obsidian in dark-mode but use excalidraw with a light background. With this setting the embedded Obsidian markdown document will match the Excalidraw theme (i.e. light colors if Excalidraw is in light mode).  
**Toggle OFF:** Set this to false if you want the embedded Obsidian markdown document to match the Obsidian theme (i.e. dark colors if Obsidian is in dark mode).

##### New drawing to match Obsidian theme

If theme is dark, new drawing will be created in dark mode. This does not apply when you use a template for new drawings. Also this will not affect when you open an existing drawing. Those will follow the theme of the template/drawing respectively.  
**Toggle ON:** Follow Obsidian Theme  
**Toggle OFF:** Follow theme defined in your template

##### Existing drawings to match Obsidian theme

If theme is dark, drawings will be opened in dark mode. If your theme is light, they will be opened in light mode.  
**Toggle ON:** Match Obsidian theme  
**Toggle OFF:** Open with the same theme as last saved

##### Excalidraw to follow when Obsidian Theme changes

If this option is enabled open Excalidraw pane will switch to light/dark mode when Obsidian theme changes.  
**Toggle ON:** Follow theme changes  
**Toggle OFF:** Drawings are not affected by Obsidian theme changes

##### Default mode when opening Excalidraw

Specifies the mode how Excalidraw opens: Normal, Zen, or View mode. You may also set this behavior on a file level by adding the excalidraw-default-mode frontmatter key with a value of: normal, view, or zen to your document.

- Always in normal-mode
- Always in zen-mode
- Always in view-mode
- Usually normal, but view-mode on Phone

## Zoom

##### Allow pinch zoom in pen mode

Pinch zoom in pen mode when using the freedraw tool is disabled by default to prevent unwanted accidental zooming with your palm.  
**Toggle ON:** Enable pinch zoom in pen mode  
**Toggle OFF:**Disable pinch zoom in pen mode

##### Mouse wheel to zoom by default

**Toggle ON:** Mouse wheel to zoom; CMD + mouse wheel to scroll  
**Toggle OFF:**CMD + mouse wheel to zoom; Mouse wheel to scroll

##### Zoom to fit on file open

Zoom to fit drawing when the drawing is first opened  
**Toggle ON:** Zoom to fit  
**Toggle OFF:** Auto zoom disabled

##### Zoom to fit on view resize

Zoom to fit drawing when the pane is resized  
**Toggle ON:** Zoom to fit  
**Toggle OFF:** Auto zoom disabled

##### Zoom to fit max ZOOM level

Set the maximum level to which zoom to fit will enlarge the drawing. Minimum is 0.5 (50%) and maximum is 10 (1000%).

## Laser pointer

##### Laser pointer color

##### Laser pointer decay time

Laser pointer decay time in milliseconds. Default is 1000 (i.e. 1 second).

##### Laser pointer decay length.

Laser pointer decay length in line points. Default is 50.

## Link Click and Drag&Drop Modifier Keys

Modifier key behavior when clicking links and dragging and dropping elements. Excalidraw will not validate your configuration... pay attention to avoid conflicting settings. These settings are different for Apple and non-Apple. If you use Obsidian on multiple platforms, you'll need to make the settings separately. The toggles follow the order of SHIFT, CMD, OPT, CONTROL.

##### Long press to open desktop

Long press delay in milliseconds to open an Excalidraw Drawing embedded in a Markdown file.

##### Long press to open mobile

Long press delay in milliseconds to open an Excalidraw Drawing embedded in a Markdown file.

### Web Browser Drag Action

In case none of the combinations apply the default action for this group is: Insert Image or YouTube Thumbnail with URL

##### Insert Image or YouTube Thumbnail with URL

##### Insert Link

##### Insert Interactive-Frame

##### Import Image to Vault

### OS Local File Drag Action

In case none of the combinations apply the default action for this group is: Import external file or reuse existing file if path is from the Vault

##### Import external file or reuse existing file if path is from the Vault

##### Insert Link: local URI or internal-link if from Vault

##### Insert Image: with local URI or internal-link if from Vault

##### Insert Interactive-Frame: local URI or internal-link if from Vault

### Obsidian Internal Drag Action

In case none of the combinations apply the default action for this group is: Insert Link

##### Insert Link

##### Insert Interactive-Frame

##### Insert Image

##### Insert Image @100%

### Link click behavior

In case none of the combinations apply the default action for this group is: Open in a new tab

##### Open in current active window

##### Open in a new tab

##### Open in a new adjacent window

##### Open in a popout window

##### Show the Markdown image-properties dialog (only relevant if you have embedded a markdown document as an image)

# Links, transclusion and TODOs

In the 'Links, transclusion and TODOs' section of Excalidraw Settings, you can configure how Excalidraw handles links, transclusions, and TODO items. This includes options for opening links, managing panes, displaying links with brackets, customizing link prefixes, handling TODO items, and more.

CMD+CLICK on `[[Text Elements]]` to open them as links. If the selected text has more than one `[[valid Obsidian links]]`, only the first will be opened. If the text starts as a valid web link (i.e. `https://` or `http://`), then the plugin will open it in a browser. When Obsidian files change, the matching `[[link]]` in your drawings will also change. If you don't want text accidentally changing in your drawings use `[[links|with aliases]]`.

##### Show second-order links

Show links when clicking on a link in Excalidraw. Second-order link are backlinks pointing to the link being clicked. When using image icons to connect similar notes, second order links allow you to get to related notes in one click instead of two. See [YT Short](https://youtube.com/shorts/O_1ls9c6wBY?feature=share) to understand.

##### Reuse adjacent pane

When CMD+OPT clicking a link in Excalidraw, by default the plugin will open the link in a new pane. Turning this setting on, Excalidraw will first look for an existing pane, and try to open the link there. Excalidraw will look for the other workspace pane based on your focus/navigation history, i.e. the workpane that was active before you activated Excalidraw.

##### Focus on Existing Tab

When opening a link, Excalidraw will focus on the existing tab if the file is already open. Enabling this setting overrides 'Reuse Adjacent Pane' when the file is already open.

##### Open in main workspace

When CMD+OPT clicking a link in Excalidraw, by default the plugin will open the link in a new pane in the current active window. Turning this setting on, Excalidraw will open the link in an existing or new pane in the main workspace.

Show `[[brackets]]` around links

In PREVIEW mode, when parsing Text Elements, place brackets around links. You can override this setting for a specific drawing by adding `excalidraw-link-brackets: true/false` to the file's frontmatter.

##### Link prefix

In PREVIEW mode, if the Text Element contains a link, precede the text with these characters. You can override this setting for a specific drawing by adding `excalidraw-link-prefix: "📍 "` to the file's frontmatter.

##### URL prefix

In PREVIEW mode, if the Text Element contains a URL link, precede the text with these characters. You can override this setting for a specific drawing by adding `excalidraw-url-prefix: "🌐 "` to the file's frontmatter.

##### Parse todo

Convert '- [ ] ' and '- [x] ' to checkbox and tick in the box.

##### Open TODO icon

Icon to use for open TODO items

##### Completed TODO icon

Icon to use for completed TODO items

##### Opacity of link icon

Opacity of the link indicator icon in the top right corner of an element. 1 is opaque, 0 is transparent.

##### Hover preview without pressing the CMD key

**Toggle ON:** In Exalidraw view mode the hover preview for [[wiki links]] will be shown immediately, without the need to hold the CMD key. In Excalidraw normal mode, the preview will be shown immediately only when hovering the blue link icon in the top right of the element.  
**Toggle OFF:** Hover preview is shown only when you hold the CMD key while hovering the link.

##### CMD+CLICK on text with [[links]] or [](links) to open them

You can turn this feature off if it interferes with default Excalidraw features you want to use. If this is turned off, you can either use CMD + CTRL or the link indicator in the top right of the element to open links.

##### Overflow wrap behavior of transcluded text

`![[doc#^ref]]{number}` Number specifies the character count where the text should be wrapped. Set the text wrapping behavior of transcluded text. Turn this ON to force-wrap text (i.e. no overflow), or OFF to soft-wrap text (at the nearest whitespace).

##### Page transclusion max char count

The maximum number of characters to display from the page when transcluding an entire page with the `![[markdown page]]`  format.

##### Transclusion word wrap default

You can manually set/override word wrapping length using the `![[page#^block]]{NUMBER}` format. Normally you will not want to set a default, because if you transclude text inside a sticky note, then Excalidraw will automatically take care of word wrapping. Set this value to `0` if you do not want to set a default.

##### Quote translusion: remove leading '> ' from each line

Remove the leading '> ' from each line of the transclusion. This will improve readability of quotes in text only transclusions  
**Toggle ON:** Remove leading '> '  
**Toggle OFF:** Do not remove leading '> ' (note it will still be removed from the first row due to Obsidian API functionality)

##### Use iframely to resolve page title

Use the `http://iframely.server.crestify.com/iframely?url=` to get title of page when dropping a link into Excalidraw

# Embedding Excalidraw into your Notes and Exporting

In the "Embed & Export" settings, you can configure how images and Excalidraw drawings are embedded and exported within your documents. Key settings include choosing the image type for markdown preview (such as Native SVG or PNG), specifying the type of file to insert into the document (original Excalidraw, PNG, or SVG), and managing image caching for embedding in markdown. You can also control image sizing, whether to embed drawings using wiki links or markdown links, and adjust settings related to image themes, background colors, and Obsidian integration. Additionally, there are settings for auto-export, which automatically generates SVG and/or PNG files to match the title of your Excalidraw drawings, keeping them in sync with file renames and deletions.

##### Image type in markdown preview

**Native SVG**: High Image Quality. Embedded Websites, YouTube videos, Obsidian Links, and external images embedded via a URL will all work. Embedded Obsidian pages will not  
**SVG Image**: High Image Quality. Embedded elements and images embedded via URL only have placeholders, links don't work  
**PNG Image**: Lower Image Quality, but in some cases better performance with large drawings. Embedded elements and images embedded via URL only have placeholders, links don't work. Also some of the [image block referencing features](https://www.youtube.com/watch?v=yZQoJg2RCKI&t=633s) do not work with PNG embeds.

- PNG Image
- Native SVG
- SVG Image

##### Type of file to insert into the document

When you embed an image into a document using the command palette this setting will specify if Excalidraw should embed the original Excalidraw file or a PNG or an SVG copy. You need to enable [auto-export PNG / SVG](#Autoexport) (see below under Export Settings) for those image types to be available in the dropdown. For drawings that do not have a a corresponding PNG or SVG readily available the command palette action will insert a broken link. You need to open the original drawing and initiate export manually. This option will not autogenerate PNG/SVG files, but will simply reference the already existing files.

- excalidraw

##### Embed Drawing using Wiki link

**Toggle ON:** Excalidraw will embed a [[wiki link]].  
**Toggle OFF:** Excalidraw will embed a [markdown](link).

## Obsidian Canvas support

##### Immersive embedding

Hide canvas node border and background when embedding an Excalidraw drawing to Canvas. Note that for a full transparent background for your image, you will still need to configure Excalidraw to export images with transparent background.

## Image caching

##### Cache images for embedding in markdown

Cache images for embedding in markdown. This will speed up the embedding process, but in case you compose images of several sub-component drawings, the embedded image in Markdown won't update until you open the drawing and save it to trigger an update of the cache.

##### Cache nested Excalidraws in Scene

Cache nested Excalidraws in the Scene for faster scene rendering. This will speed up the rendering process, especially if you have deeply nested Excalidraws in your scene. Excalidraw will try to intelligently identify if any children of a nested Excalidraw have changed and will update the cache accordingly. You may want to turn this off, in case you are suspecting that the cache is not updating properly.

##### Purge Cache

##### Purge Backups

##### If found, use the already exported image for preview

This setting works in conjunction with the [Auto-export SVG/PNG](#Autoexport) setting. If an exported image that matches the file name of the drawing is available, use that image instead of generating a preview image on the fly. This will result in faster previews especially when you have many embedded objects in the drawing, however, it may happen that your latest changes are not displayed and that the image will not automatically match your Obsidian theme in case you have changed the Obsidian theme since the export was created. This setting only applies to embedding images into markdown documents. For a number of reasons, the same approach cannot be used to expedite the loading of drawings with many embedded objects. See demonstration [here](https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/1.6.23).

## Export Settings

Render the file as an image when exporting an Excalidraw file to PDF

This setting controls the behavior of Excalidraw when exporting an Excalidraw file to PDF in markdown view mode using Obsidian's **Export to PDF** feature.  

- When **enabled** the PDF will show the Excalidraw drawing only;
- When **disabled** the PDF will show the markdown side of the document.

See the other related setting for [Markdown Reading Mode](#MDReadingMode) under 'Appearnace and Behavior' further above.  
⚠️ Note, you must close the active excalidraw/markdown file and reopen for this change to take effect. ⚠️

##### Embed scene in exported image

Embed Excalidraw scene in exported image. Can be overridden at a file level by adding the `` excalidraw-export-embed-scene: true/false `frontmatter key. The setting only takes effect the next time you (re)open drawings.` ``

### Image sizing

##### Default width of embedded (transcluded) image

The default width of an embedded drawing. This applies to live preview edit and reading mode, as well as to hover previews. You can specify a custom width when embedding an image using the `![[drawing.excalidraw|100]]` or `[[drawing.excalidraw|100x100]]` format.

##### Default height of embedded (transcluded) image

The default height of an embedded drawing. This applies to live preview edit and reading mode, as well as to hover previews. You can specify a custom height when embedding an image using the `![[drawing.excalidraw|100]]` or `[[drawing.excalidraw|100x100]]` format.

##### PNG export image scale

The size-scale of the exported PNG image
##### Image Padding

The padding (in pixels) around the exported SVG or PNG image. Padding is set to 0 for clippedFrame references.If you have curved lines close to the edge of the image they might get cropped during image export. You can increase this value to avoid cropping. You can also override this setting at a file level by adding the `` excalidraw-export-padding: 5 `frontmatter key.` ``

### Image theme and background color

##### Export image with background

If turned off, the exported image will be transparent.

##### Export image with theme

Export the image matching the dark/light theme of your drawing. If turned off, drawings created in dark mode will appear as they would in light mode.

##### Excalidraw preview to match Obsidian theme

Image preview in documents should match the Obsidian theme. If enabled, when Obsidian is in dark mode, Excalidraw images will render in dark mode. When Obsidian is in light mode, Excalidraw will render light mode as well. You may want to switch 'Export image with background' off for a more Obsidian-integrated look and feel.

### Auto-export Settings

##### Keep the .SVG and/or .PNG filenames in sync with the drawing file

When turned on, the plugin will automatically update the filename of the .SVG and/or .PNG files when the drawing in the same folder (and same name) is renamed. The plugin will also automatically delete the .SVG and/or .PNG files when the drawing in the same folder (and same name) is deleted.

##### Auto-export SVG

Automatically create an SVG export of your drawing matching the title of your file. The plugin will save the *.SVG file in the same folder as the drawing. Embed the .svg file into your documents instead of Excalidraw making you embeds platform independent. While the auto-export switch is on, this file will get updated every time you edit the Excalidraw drawing with the matching name. You can override this setting on a file level by adding the `excalidraw-autoexport` frontmatter key. Valid values for this key are `none`,`both`,`svg`, and `png`.

##### Auto-export PNG

Same as the auto-export SVG, but for *.PNG

##### Export both dark- and light-themed image

When enabled, Excalidraw will export two files instead of one: filename.dark.png, filename.light.png and/or filename.dark.svg and filename.light.svg  
Double files will be exported both if auto-export SVG or PNG (or both) are enabled, as well as when clicking export on a single image.

# Embed files into Excalidraw

In the Embed Files section of Excalidraw Settings, you can configure how various files are embedded into Excalidraw. This includes options for embedding interactive markdown files, PDFs, and markdown files as images.

## PDF to Image

##### PDF to Image conversion scale

Sets the resolution of the image that is generated from the PDF page. Higher resolution will result in bigger images in memory and consequently a higher load on your system (slower performance), but sharper imagee. Additionally, if you want to copy PDF pages (as images) to Excalidraw.com, the bigger image size may result in exceeding the 2MB limit on Excalidraw.com.

## Interactive Markdown Files

##### Single click to edit embedded markdown

Single click on an embedded markdown file to edit it. When turned off, the markdown file will first open in preview mode, then switch to edit mode when you click on it again.

---

The below settings will only effect future embeds. Current embeds remain unchanged. The theme setting of embedded frames is under the "Excalidraw appearance and behavior" section.

##### Use Obsidian Defaults

##### Filename Visible

#### Embedded note background color

##### Match Element Background Color

##### Match Canvas Background Color

##### Background Opacity

Current opacity is **70%**

#### Embedded note border color

##### Match Element Border Color

##### Border Opacity

Current opacity is **0%**

## Embed markdown into Excalidraw as image

##### Default width of a transcluded markdown document

The width of the markdown page. This affects the word wrapping when transcluding longer paragraphs, and the width of the image element. You can override the default width of an embedded file using the `[[filename#heading|WIDTHxMAXHEIGHT]]` syntax in markdown view mode under embedded files.

##### Default maximum height of a transcluded markdown document

The embedded image will be as high as the markdown text requires, but not higher than this value. You can override this value by editing the embedded image link in markdown view mode with the following syntax `[[filename#^blockref|WIDTHxMAXHEIGHT]]`.

##### The default font typeface to use for embedded markdown files.

Set this value to "Virgil" or "Cascadia" or the filename of a valid `.ttf`, `.woff`, or `.woff2` font e.g. `MyFont.woff2` You can override this setting by adding the following frontmatter-key to the embedded markdown file: `excalidraw-font: font_or_filename`

- Virgil
- Cascadia
- Assistant
- RubikBeastly-Regular.ttf
- GreatVibes-Regular.ttf
- VT323-Regular.ttf
- LuckiestGuy-Regular.ttf
- Orbitron-Bold.ttf
- Starjedi.ttf
- PermanentMarker-Regular.ttf
- Gugi.ttf
- Courier New.ttf
- Gugi.woff2
- Courier New.woff2

##### The default font color to use for embedded markdown files.

Set this to any valid css color name e.g. "steelblue" ([color names](https://www.w3schools.com/colors/colors_names.asp)), or a valid hexadecimal color e.g. "#e67700", or any other valid css color string. You can override this setting by adding the following frontmatter-key to the embedded markdown file: `excalidraw-font-color: steelblue`

##### The default border color to use for embedded markdown files.

Set this to any valid css color name e.g. "steelblue" ([color names](https://www.w3schools.com/colors/colors_names.asp)), or a valid hexadecimal color e.g. "#e67700", or any other valid css color string. You can override this setting by adding the following frontmatter-key to the embedded markdown file: `excalidraw-border-color: gray`. Leave empty if you don't want a border.

##### CSS file

The filename of the CSS to apply to markdown embeds. Provide the filename with extension (e.g. 'md-embed.css'). The css file may also be a plain markdown file (e.g. 'md-embed-css.md'), just make sure the content is written using valid css syntax. If you need to look at the HTML code you are applying the CSS to, then open Obsidian Developer Console (CMD+OPT+i) and type in the following command: "ExcalidrawAutomate.mostRecentMarkdownSVG". This will display the most recent SVG generated by Excalidraw. Setting the font-family in the css is has limitations. By default only your operating system's standard fonts are available (see README for details). You can add one custom font beyond that using the setting above. You can override this css setting by adding the following frontmatter-key to the embedded markdown file: "excalidraw-css: css_file_in_vault|css-snippet".

# Non-Excalidraw.com supported features

These settings in the "Non-Excalidraw.com Supported Features" section provide customization options beyond the default Excalidraw.com features. These features are not available on excalidraw.com. When exporting the drawing to Excalidraw.com these features will appear different. You can configure the number of custom pens displayed next to the Obsidian Menu on the canvas, allowing you to choose from a range of options. Additionally, you can enable a local font option, which adds a local font to the list of fonts on the element properties panel for text elements.

## Rendering tweaks

##### Maximum image zoom in resolution

To save on memory and because Apple Safari (Obsidian on iOS) has some hard-coded limitations, Excalidraw.com limits the max resolution of images and large objects when zooming in. You can override this limitation using a multiplicator. This means you are multiplying the limit set by default in Excalidraw, the larger the multiplier the better the image zoom in resolution will be, and the more memory it will consume. I recommend playing with multiple values for this setting. You know you've hit the wall, when zooming in to a larger PNG image suddenly the image disappears from view. The default value is 1. The setting has no effect on iOS.

## Custom pens

##### Number of custom pens

You will see these pens next to the Obsidian Menu on the canvas. You can customize the pens on the canvas by long-pressing the pen button.

## Local font

##### Enable local font option

Enabling this option will add a local font to the font list in the properties panel for text elements. Be aware that using this local font may compromise platform independence. Files using the custom font might render differently when opened in a different vault or at a later time, depending on the font settings. Additionally, the 4th font will default to the system font on excalidraw.com or other Excalidraw versions.

##### Local font file

Select a .otf, .ttf, .woff, or .woff2 font file from your vault to use as the local font. If no file is selected, Excalidraw will default to the Virgil font. For optimal performance, it is recommended to use a .woff2 file, as Excalidraw will encode only the necessary glyphs when exporting images to SVG. Other font formats will embed the entire font in the exported file, potentially resulting in significantly larger file sizes.

# Miscellaneous features

These miscellaneous features in Excalidraw include options for setting default LaTeX formulas for new equations, enabling a Field Suggester for autocompletion, displaying type indicators for Excalidraw files, enabling immersive image embedding in live preview editing mode, and experimenting with Taskbone Optical Character Recognition for text extraction from images and drawings. Users can also enter a Taskbone API key for extended usage of the OCR service.

##### Default LaTeX formula for new equations

Leave empty if you don't want a default formula. You can add default formatting here such as `\color{white}`.

##### Display type (✏️) for excalidraw.md files in File Explorer

Excalidraw files will receive an indicator using the emoji or text defined in the next setting.

##### Set the type indicator for excalidraw.md files

The text or emoji to display as type indicator.

##### Immersive image embedding in live preview editing mode

Turn this on to support image embedding styles such as ![[drawing|width|style]] in live preview editing mode. The setting will not affect the currently open documents. You need close the open documents and re-open them for the change to take effect.

##### Fade out Excalidraw markup

In Markdown view mode, the section after the markdown comment %% fades out. The text is still there, but the visual clutter is reduced. Note, you can place the %% in the line right above # Text Elements, in this case the entire drawing markdown will fade out including # Text Elements. The side effect is you won't be able to block reference text in other markdown notes, that is after the %% comment section. This is seldom an issue. Should you want to edit the Excalidraw markdown script, simply switch to markdown view mode and temporarily remove the %% comment.

##### Load Excalidraw Properties into Obsidian Suggester

Toggle this setting to load Excalidraw document properties into Obsidian's property suggester at plugin startup. Enabling this feature simplifies the use of Excalidraw front matter properties, allowing you to leverage many powerful settings. If you prefer not to load these properties automatically, you can disable this feature, but you will need to manually remove any unwanted properties from the suggester. Note that turning on this setting requires restarting the plugin as properties are loaded at startup.

## Taskbone Optical Character Recogntion

This is an experimental integration of optical character recognition into Excalidraw. Please note, that taskbone is an independent external service not provided by Excalidraw, nor the Excalidraw-Obsidian plugin project. The OCR service will grab legible text from freedraw lines and embedded pictures on your canvas and place the recognized text in the frontmatter of your drawing as well as onto clipboard. Having the text in the frontmatter will enable you to search in Obsidian for the text contents of these. Note, that the process of extracting the text from the image is not done locally, but via an online API. The taskbone service stores the image on its servers only as long as necessary for the text extraction. However, if this is a dealbreaker, then please don't use this feature.

##### Enable Taskbone

By enabling this service your agree to the Taskbone [Terms and Conditions](https://www.taskbone.com/legal/terms/) and the [Privacy Policy](https://www.taskbone.com/legal/privacy/).

##### Taskbone API Key

Taskbone offers a free service with a reasonable number of scans per month. If you want to use this feature more frequently, or you want to supoprt the developer of Taskbone (as you can imagine, there is no such thing as 'free', providing this awesome OCR service costs some money to the developer of Taskbone), you can purchase a paid API key from [taskbone.com](https://www.taskbone.com/). In case you have purchased a key, simply overwrite this auto generated free-tier API-key with your paid key.

# Excalidraw Automate


ExcalidrawAutomate is a scripting and automation API for Excalidraw. Unfortunately, the documentation of the API is sparse. I recommend reading the [ExcalidrawAutomate.d.ts](https://github.com/zsviczian/obsidian-excalidraw-plugin/blob/master/docs/API/ExcalidrawAutomate.d.ts) file, visiting the [ExcalidrawAutomate How-to](https://zsviczian.github.io/obsidian-excalidraw-plugin/) page - though the information here has not been updated for a long while -, and finally to enable the field suggester below. The field suggester will show you the available functions, their parameters and short description as you type. The field suggester is the most up-to-date documentation of the API.


##### Enable Field Suggester

Field Suggester borrowed from Breadcrumbs and Templater plugins. The Field Suggester will show an autocomplete menu when you type `excalidraw-` or `ea.` with function description as hints on the individual items in the list.

##### Startup script

If set, excalidraw will execute the script at plugin startup. This is useful if you want to set any of the Excalidraw Automate hooks. The startup script is a markdown file that should contain the javascript code you want to execute when Excalidraw starts.

# Compatibility features

You should only enable these features if you have a strong reason for wanting to work with excalidraw.com files instead of markdown files. Many of the plugin features are not supported on legacy files. Typical usecase would be if you use set your vault up on top of a Visual Studio Code project folder and you have .excalidraw drawings you want to access from Visual Studio Code as well. Another usecase might be using Excalidraw in Logseq and Obsidian in parallel.

##### Linter compatibility

Excalidraw is sensitive to the file structure below `# Excalidraw Data`. Automatic linting of documents can create errors in Excalidraw Data. While I've made some effort to make the data loading resilient to lint changes, this solution is not foolproof.  
==The best is to avoid liniting or otherwise automatically changing Excalidraw documents using different plugins.==  
Use this setting if for good reasons you have decided to ignore my recommendation and configured linting of Excalidraw files.  
The `## Text Elements` section is sensitive to empty lines. A common linting approach is to add an empty line after section headings. In case of Excalidraw this will break/change the first text element in your drawing. To overcome this, you can enable this setting. When enabled, Excalidraw will add a dummy element to the beginning of `## Text Elements` that the linter can safely modify.

##### Zotero and Footnote compatibility

Preserve text after the ## Drawing section of the markdown file. This may have a very slight performance impact when saving very large drawings.

##### Sliding panes plugin support

Need to restart Obsidian for this change to take effect.  
If you use the [Sliding Panes plugin](https://github.com/deathau/sliding-panes-obsidian) you can enable this setting to make Excalidraw drawings work with the Sliding Panes plugin.  
Note, that Excalidraw Sliding Panes support causes compatibility issues with Obsidian Workspaces.  
Note also, that the 'Stack Tabs' feature is now available in Obsidian, providing native support for most of the Sliding Panes functionality.

##### New drawings as legacy files

⚠️ Enable this only if you know what you are doing. In 99.9% of the cases you DO NOT want this on. By enabling this feature drawings you create with the ribbon icon, the command palette actions, and the file explorer are going to be all legacy *.excalidraw files. This setting will also turn off the reminder message when you open a legacy file for editing.

##### Auto-export Excalidraw

Same as the auto-export SVG, but for *.Excalidraw

##### Sync *.excalidraw with *.md version of the same drawing

If the modified date of the *.excalidraw file is more recent than the modified date of the *.md file then update the drawing in the .md file based on the .excalidraw file

# Settings for installed Scripts

Some of the Excalidraw Automate Scripts include settings. Settings are organized by script. Settings will only become visible in this list after you have executed the newly downloaded script once.


%%
# Excalidraw Data
## Text Elements
## Drawing
```compressed-json
N4KAkARALgngDgUwgLgAQQQDwMYEMA2AlgCYBOuA7hADTgQBuCpAzoQPYB2KqATLZMzYBXUtiRoIACyhQ4zZAHoFAc0JRJQgEYA6bGwC2CgF7N6hbEcK4OCtptbErHALRY8RMpWdx8Q1TdIEfARcZgRmBShcZQUebQAWbQBGGjoghH0EDihmbgBtAF1+CFw4OABlKKhxVFAwSHUMmogiZWlU+oZCBAoAIVxsAGtlUmEOYgBhNnw2Um4IAGIAMRWA

NiWABg7IbBFA7IBJav1K0cGEKZm5iQWkhDu77Yhd0n2oI4z+oZGxyenZ+ZQcgcZhwXBvJ4vN4ffRLQj4fCVGDBeaCDyQvZZd7HU5sc4AdRI6m4fHAO0xhxxQLxCCRKIkaJIGNeWJhACVhG0OOFcmgkvxySzKRkAPJg7BqGDcJIbDYC54U7EZJacKBLXD6eFStAAVnlUNZxxV2XKhCMNR4crJCqFSv0ABUsFAAIKtLgSYIAMygzOhVPBLtebAokhC

xG4HCECP1iphAFFxs6gyGw/NwaMqDHbTCkxn7fBmqMhOMnsxsKMEQANbg6gActe0AHY9dayxX8ABNbjxACccRbnSMbAM3DqnXoBCENSSZIAvlm/RkOcXiNzmLz0EWS/KRiRTeaSVbOrviJUEHAazvSCQALJsYgIBO4TTBcNoT0EMJXkiXAFoMeQL00xvugyxLL0qy1jq2yQGyCDKFG4LzGBcZJBMEwQHO+r/KQAAKBAIDINQAc81gTswXzDFuIF5

GSnRAtYoLgliMGQC+AyDKxtH1DxiyrPEqw8KsKQCrxCy9DwvQbFJrGQAsta9LWPb1rJiwAMw8GpSRaaptw9kk+m1phPFgEUdFgNxJmLBMcYTAAIuhulxqszlxtBomdAsdnOt5dk9rpqw9qsjb8bpanxGpkU8MZPFmVZIZqEgHmWWJKxLOsWweXJaW9EsRlZYsaW1ks8S6XlqxqbKumNhMGlVeZcU8SlnnOXZPATCJ5nZWpcY9nGmVdYstl2SNnUm

XJPYhRVdm6fEvSRUkcYxfUjX1M1cnOks+mNvlg1eTVCm9LptXOhMPbOrpOp2fEtZqY2uk8HGPDxEkR0Ncle3NjqPYvcd8TOr0QW6c6O1JMJYUSW1Y1WbcdlgzKy2mR942LHWWlJNDYl2b1ak6u5e0+asGw8JjnntUktYbP5BW3ETEwbKV73metiw9j22PY8dNlLHGSy6fNrmrA9ca1iLS000kjbxFL91MyZLMLGptYAwDuk/Q5DmXUsEy9DruloT

qqyG7pGxPRJb0matFl7bKbNs7NdlpXzNOyksPBuybDPXTNLvE4JQty01NsbKsodCzTkVO576GOb7kWRZ7BkGYjVsK7K7Xtfr6xpZ7zobHnifCeHwfSdJKfIzDExLHZV34yjCxxo2cbOs3ul2b0/X9QFPCNhsvdhdpt1GYHa2fTdzrK/zPYTDqM9q42IMg2FzrxDqq/621GlqeXzN7TdgWBWrOu9CfAWA3bD0RTquP6yTzpJBdI/W/XPcCQJ1Vxr0

jZf7NimQcX9ckjxE0ppE298SbRSfmnZ0uMb40wihrDCEszpqR7NvF2OpXqvRNpVOyGwZpQL2isKSMkaYrDso2ChZVtbxAmKVGmdlKaygGvXVY9NmE73lkQpY19r7UOdOdam3Cm5N2Bj2ZhLCYZrwkZwoO9cVgyLIXlDYlNqHxAZpIsSTCOHwIkVsQh9dnR5x0dwvGeNqGKL2njSxL9jH1UthXMS/0bEwxWDwHU7j+a9xMS/HULixJJEtBwgxrjq5

zU0Z5FYzcqFKMdnQtutZBJVRpmwrS9jYqOMiUse+fDYn5yEfI8Ck1xYE3VskqxwCib6IcbvQpUtymFN6BPCJ2Utr1N0pTNSxjZobCSHg6pGTakwyMfEfp/D3F11CY2SqLTUYeKqQ9e+MzZGj3rv9EmDTQmJM8TTL+HjNliXcRjA5nlAkqPSStTJrS3KkO4W7GJ3DbLxIYUpGUsyFhsJuhcpGQzUrayNugx5XSCmhOuqImmAjGxvMuhFJhKzn6hKM

Sc1p11VFKNyuojpGxrHvPUZJb5qcCYgyCdQiYX1+FSXeXjVByLFg8Hvuw+FCt/ppPecQjxkyxJf0bOI95RzeW3w2IyhqdFVoYGCJkE01Jzj5HMtAYETEIQeQgOxIYXE9rm1Lh0xSyldr1y3tpUmckk6GQCgJISKQQliUFm5NuPkfIgrEgfEK9C9rhXjtFGmNl7KOSfhABK1R1WFPAnlaheUSplUScsmmNU6psrWJsJlRCep9XecNUa89Q5qR9nve

aWkSn11auTJN9cKETEOsdLpZ0Lo0yujdO6wtnrYIhVtSWw8alcPrnQgGQMIWg3BhHSGJMN7w3eV9H6lqO1yJhtjNB5iIV2SJsOmm5NKaOtOXTBml1boY0nYMztldua835j1FyACYaPVFqLfWMtpZq3ZnGTmVrPLqx9VrHWetkGG2Ni7M2kkwrKyaRbfd06nGOxzr7N2HtfajNGZ7ISQlPZ238s+uSkcIPBxjkg4O8dAX11lCaz2YcA5TtWTDMGUd

fZ5wLr7eG56xLMJIfBiYmdUNDSbi3Gte126d3eYJXu/cI6DyVsdautcS0w0BjPOeNNJqL3uhHFea9OWnM3qAmN49J5sYWNPE+p8Unn3tiuq+cC9qBIfg/WaiSgoodIwisSTcv4/3gX/RJ+tgFbzAeZz1e1X78RIyBsjTjs1vuQWgtBJtMG9GbTbXB+CwGwOgtp8hlCFPcLoc87j2i+PsNpWBEhAzLm/KyQIgR1CREFuGbyvL0ifGhN4dvZLyi0Xc

PUZimm2XcV6IscEuzCsVhmJU60/xnkcV5fpSNjadjCs/IPX89xOyNXePG34urASgl5ecb1wL9msnRLS4UuJrrS3bLy6k6FsTwkSb+Xgsr6LiliNGTVypeWVg5Ma317hTSWuFMmu1vanTum6L6a9pY9SZuEsKc6CZ5Xo1WPmeNpZeWRljKa9sobiw9kkpXZgi7ZnLRwvgdD6FTX7kHdCU847M7XlnboYTx5OoZJNbjMC6hYLKtiUhXj+ua8lag4mA

C67WTUXxoxe8ymOKen4vjUiiHVzCra3JUogGNXr4CpXQy5HxKCXy/yxyrxPKVsGTy2cxlRPWUp1FaJcVTRsiUR+CuWVVkGIgjBEquVqrOK681bc1h5qB0A51SpCOmlDX630qa7TNqMcLG9Q5bDpb7V+QCkFF1YUIpRXhf6yQiUg2hJDXq/PGUw3FSp6lKNeXY0kuSymruNMi0dScvZDNsmprZt/gtJa2my0VpbdtQvYkTrVsuqihtK6novWA0Vub

nlu2A3o55cdv0+21nhhDHgUMR3CTl8VuSs7cYx7Rru4Gi7iZGrpR1NdWchVbu0+hXmx7ZMPs5rs09zlhZXo56c29stPv11fZrBHIBqrLWtrLrEdF+kbAvnJKbJJP+tpqMpRsHMhp7FBj5vhl7HBr7AhgFtPqBp5OhisERmHNHDHJ7LhonBHkLsatnEQdgSxgnjDLKNRu8gRkXJ7KXFPrNvgXJI3M3K3F6mJjXG3B3KbHxj3H3O8lpErCJtplJrPD

HlLMrJPK3vJsvKvOvBLGph9jtgrLpnplZgfOunJKsIZsYXSiZjHuZvfI/H/jDI5t/OToclLP5r/Ikm5hLB5upjbOAoEtQYsAgqFj4YlvrCghFhglghAbFvgvFk1hQg8o0lqkohlmXp5IwpNnxLljvjPq0qVuYWBA1uVnwWIhkQsLVjrrvgrpTD9qEqUSsG1uLt1rojIk1oNsDNNj1qrqURNttngUFlkgtjHltnll/N0atibhttkTwQrvtmzldrEj

QgkkkjlhbnEfkvwkkLkl9g9hCmUlSi9lMf0a0t9vGuDtQn9o0V0ptr0qjnYX8tDvOkSk9qcXDjzgjnykjocbtq0ujrNMTiMc2Njr5rjhMecl8f1m4gkRTozvGpTgkvpLTl8uCUCnduloLpduCqUlCs9nzsiYdl8vwkDl9iVI0ZLrotLv4WBGSo8YYtrjLpSpdGrojmhBUTkQrr0PrubtzpJo2IbnypgurvjjfhDlbnRNAGwHALhOYIMBuABJAOkJ

KlAPbtRE7kXomvXqsG1I3k/hzF/nJHHrHINC7oqixH6gqViLiDKmgArEvufgsLKMRqpJ7sdMNIaSjMaW7qaXZqRBwORMqb8KqX8ulOqQTK2jtMxpnF6q6YwU6v7nuitHRLOFhNaAaFKmcAgGKFAOwCCBGFGPgPKJ6OQJkHBOMEwIQBwMoKOGKVkM+K+NwECFONbtgEQBeGgA2QgNbhwBqDUO2dbsIFAEQNyPWaQFOMmZ0HYAAFYIDYA5DlBdlwB3

gPhPgvgIAgQfj4BfjWgDBZmMD2jDj4BVm8SwCICojpAznZkwQKjMBQAGD5gnloCRjRhikzBDCrncDrmbm8T4ChAujnm7n7m5kIhzjgDzh0CejwjhCjhJmzhAA===
```
%%