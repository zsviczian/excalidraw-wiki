---
excalidraw-plugin: parsed
tags:
  - excalidraw
excalidraw-autoexport: svg
excalidraw-open-md: true
excalidraw-export-transparent: true

---
# [[Excalidraw Markdown File Structure]]
[Downloadable storyboard on Excalidraw.com](https://excalidraw.com/#json=MSQ4UcwPcETmLdSaKFjD_,40CTKWiOAb-BvmtYYHyVHQ)

![Explaining Links, Transclusions and Embedding in Obsidian Excalidraw](https://youtu.be/CpSwwv1CPMM)

## Summary
In this video, I walk through the file structure of Excalidraw in Obsidian and explain why understanding it gives you more control over your visual thinking workflow. I highlight important changes in version 2.2.0 that improve support for hybrid notes but break backward compatibility, urging users to update the plugin across devices.

I focus primarily on the advantages of using `*.md` files over `*.excalidraw` files, such as Obsidian's ability to update links, add metadata, and enable backlinks. The `*.md` format allows for properties, back-of-the-card notes, and Excalidraw data to coexist in a structured way.

I also discuss file size management, JSON compression, and the handling of embedded files and images. Special attention is given to managing autosave settings to avoid sync conflicts across devices.

Finally, I offer practical tips for advanced features like block referencing, LaTeX integration, and SVG recoloring, wrapping up with advice on avoiding data loss when closing Obsidian.

## Timestamps
- [00:00](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=0s) Intro 
- [01:28](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=88s) Type of objects you can embed 
- [02:21](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=141s) Sources: From where can you embed? 
- [03:24](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=204s) Type of references: Links, Transclusions, Embedding 
- [03:40](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=220s) Links 
- [04:39](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=279s) Transclusion 
- [08:41](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=521s) Embedding 
- [12:32](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=752s) Examples of Linking 
- [19:46](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=1186s) Examples of Transclusion: An Image 
- [22:29](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=1349s) Transcluding (Nesting) Excalidraw Drawings (Deconstruction script) 
- [27:54](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=1674s) Embeddables: Embedding markdown. Limitations with nesting 
- [30:58](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=1858s) Transclude Markdown as Image (can be nested) 
- [33:28](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=2008s) Transclude Markdown as text (section and block references) 
- [34:57](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=2097s) Transclude a text element from the drawing, in the drawing 
- [39:58](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=2398s) Transclude a video from the Obsidian Vault 
- [41:05](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=2465s) Transclude from the Web 
- [44:11](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=2651s) Transclude from the local file system 
- [46:21](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=2781s) Embedding and export to Excalidraw.com 
- [48:19](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=2899s) Transcluding Animated GIFs 
- [50:01](https://www.youtube.com/watch?v=CpSwwv1CPMM&t=3001s) Summary & Closing remarks

## Video Transcript
Hey Everyone! Zsolt here. Welcome to Visual PKM!

Today we are going to learn about the File Structure of Excalidraw in Obsidian.

But you might by thinking right now... Why the heck would I want to know that?

Because, one key reason, for why Excalidraw in Obsidian is so much more than just an illustration tool, comes from its file structure. If you understand it, you have a superpower at your disposal.

There are a lot of things I want to show you, but don't worry, this is all easy stuff and we'll get through it very quickly. Trust me, you'll be much more powerful knowing all this, when it comes to visual thinking!

But there's another reason we need to talk. With the release of 2.2.0 I've made some important improvements to the file structure that will break backwards compatibility of your drawings. I made the changes to better support hybrid notes, i.e. notes that have a drawing on one side of the imaginary paper, and markdown text on the other... So make sure you update the plugin on all your devices to avoid surprises.

On a side note, if you are an Obsidian Insider, and have installed 1.6.0, then drawings larger than two megabytes will not open, because Obsidian stopped indexing large files. This has nothing to do with Excalidraw updates, and the Obsidian devs have already fixed this in 1.6.1. My hope is that the update will be made public soon. However, we'll touch on some file size related topics later in the video. 

So, why should you care about the file structure? Because then you'll have more control over your own data. You'll understand about compatibility with excalidraw.com, get access to power features, keep file sizes and Obsidian sync quota under control, avoid synchornization conflicts and create better Templater templates, to name a few.

When it comes to file formats, you have two options. `*.excalidraw` files or `*.md` files.

We will not spend too much time on `*.excalidraw` files. Related features support niche use cases. But the most basic use case for  `*.excalidraw` file support is compatibility with excalidraw.com.

If you download a drawing from Excalidraw.com, then drop that file into your Obsidian Vault, you'll be able to open it with the plugin. Note, however, the warning message that pops up. You should covert the imported file to markdown to get all the benefits of the plugin. You can convert it by right clicking the tab and selecting, "Convert to new format".

The `*.md` format comes with many benefits. Links in your drawings get updated by Obsidian. You get all the fancy backlink and outgoing link features. Document properties are available. You get to add tags and notes on the back of the drawing, plus block reference text from your drawing in all your notes.

Switching to markdown view mode you will observe three major parts of the note. Document properties at the top. Back-of-the-card notes right below properties, but above Excalidraw Data, and the Excalidraw Data section. Let's look at these one by one, starting with properties.

Depending on your Obsidian settings, properties may look different or be completely hidden. This is how properties look in source mode, 

and how they look in the properties editor.

Excalidraw comes with many predefined properties to choose from.
I'll share the link to this drawing in the video description, so you can come back to this list.

However, the benefit of editing properties in source mode is the popup suggester. For example, you can override the default theme of a drawing by applying the export-dark property. This will not only influence how the drawing gets rendered when embedding to markdown, but also how the drawing looks when you open it.

Now, lets talk about Excalidraw Data.

The Drawing section contains your drawing in JSON. This is the same format as in the `*.excalidraw` file, except that images are not embedded in the JSON. We'll talk about this in a moment.

I want to draw your attention to the two code-blocks. "compressed-json" and "json".

When in markdown view mode, you can use "Decompress current Excalidraw file" from the Command Palette to convert the compressed JSON into human readable format.  This is great when you manually want to tweak your JSON. The decompress feature is also available via script using Excalidraw Automate.

Compression is done using the open source LZ-String package. 

Starting from Excalidraw 2.2.0, compression is set as the default in Plugin Settings and converting compressed JSON to normal JSON when switching to markdown view mode is disabled by default. I recommend these settings for keeping your drawings data smaller.

The other feature we need to talk about is the markdown comment. By default the Drawing section is commented out to avoid it showing up in reading mode and when exporting to PDF or to the web.

You may move the comment to the line right before Excalidraw Data. This way Excalidraw Data will also be hidden in exports, 

BUT by doing so, block referencing text elements from your drawings will stop working because Obsidian does not index blocks in comments.

The Text Elements section is where all your text in the drawing is stored. When we block referenced the text in another note a moment ago, this was the block reference we were using.

Sometimes it is quicker to modify text in Text Elements in markdown view, rather than on the drawing. Modifications in the Text Elements section will take precedence over the Drawing JSON. All you need to pay attention to is to leave the block references at the end of the lines intact.

Back-of-the-card notes are simply markdown sections at the top of your Excalidraw file.

You may notice an extra hashtag appear above Excalidraw Data when adding a back-of-the-card note. This happens when you have Excalidraw Data commented out. The extra hashtag will not be visible in exports, 

but it is required for avoiding the commented section from appearing when editing the back of the note card. For the most part, you don't need to worry about this, I just wanted to share in case some of you were wondering.

The last part of the file I wanted to show you is the Embedded Files section.

Excalidraw in Obsidian does not save images to the Excalidraw JSON, but stores all the images separately in your Vault. This is great, because this way you can reference and reuse images. You can even use shared images to navigate between drawings. I will link two related videos in the description below should you want to explore this idea further.

One neat, but currently hard to use feature is how you can recolor embedded SVG and Excalidraw images by providing a color map.

The other power feature is how you can anchor the size of an embedded Excalidraw drawing to

100% of it's original size. I won't go into the many reasons why you might want to do that, but just note, that by adding a 100% following the pipe character you can enforce the size and disable resizing of the image in your scene.

Finally, if you embed LaTeX equations into your drawing, these will also show up under Embedded Files. Sometimes it may be more convenient to edit them here.

To complete our walkthrough, let's spend a minute to understand Autosave. First, when Obsidian terminates, it does not await plugins to finish saving. To avoid half saved files and synchronization conflicts, it is best to force save your drawing and closing the tab before exiting Obsidian. This is especially useful when you work on many devices, like I do. When I finish working on my Macbook at night, I make sure Excalidraw is closed and Obsidian syncs before going to sleep. This way, in the morning at my desktop or on my tablet I can safely continue working on the drawing.

In plugin settings, under Saving, you can define different autosave intervals for desktop and for mobile. Beyond the autosave interval Excalidraw will always save your drawing when switching tabs and when closing a drawing or switching to markdown view mode. Because Obsidian sync stores all the previous versions of your markdown files, having large drawings that save too frequently can quickly eat up your quota. I personally use the "Practically never"  setting on desktop, but a frequent autosave on mobile. This is because on a mobile it is easy to switch tasks, and you never know when iOS or Android will recycle the Obsidian process in the background.

So hopefully, you found this walkthrough helpful, and it also wasn't too painful. If you liked this video, subscribe and hit that like button, and if you want to support me, you can find a link to my ko-fi page in the description below. Thank you!


%%
# Excalidraw Data
## Text Elements
## Drawing
```compressed-json
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=
```
%%