**Created**:: [[2021-11-28 Sunday]]
**Link**:: https://youtu.be/K6qZkTz8GHs
**Duration**:: 5:04

![Advanced Styling of Markdown Embeds with Excalidraw Obsidian  (1.4.14)](https://youtu.be/K6qZkTz8GHs)

# Summary
In this video, Zsolt demonstrates advanced styling techniques for markdown embeds using Excalidraw in Obsidian. He explains how to use a custom CSS file to style markdown documents and introduces new features like front matter keys to enhance customization. The tutorial focuses on creating visually appealing markdown documents with unique styles and elements.

# Key Takeaways
- You can specify a custom CSS file for styling markdown embeds in Excalidraw.
- The new front matter key `xcolor draw css` allows you to set styles directly within your markdown files.
- Using the developer console to inspect elements helps in tailoring your CSS for better visual customization.

# Content
This video is about the advanced styling of markdown embeds. [* ](https://youtu.be/K6qZkTz8GHs)

First of all, I want to show you that in settings, I've added an additional setting. [* ](https://youtu.be/K6qZkTz8GHs)

That is right here, a CSS file, so you can now specify a CSS file that is going to be used for styling. The CSS file can be a normal markdown document or it can be a CSS document; the bottom line is it has to contain valid CSS code. [* ](https://youtu.be/K6qZkTz8GHs)

In this case, I created this file called `markdown css`, and I placed it in my fonts library, and that is the file that I'm referencing right here. You can see this is the `markdown css.md`, and within my `markdown css.md`, I have this styling. By the way, here's a trick that you can apply: you can see that I've placed in comments at the top of the code block, and with this, I get syntax highlighting in the editor. [* ](https://youtu.be/K6qZkTz8GHs)

So that's just a small trick. What you can see here is my styling for this document, and you can see a couple of things. First of all, the entire document is hosted in an element with the class `xcolidra mdhost`, and you can use this to do a couple of things. For now, I added some padding around the document, but we'll see later what else you can do. [* ](https://youtu.be/K6qZkTz8GHs)

Then you have the normal HTML components, and you can add your styling. For example, I did a bit of styling around the table, as well as I added styling so the anchors are underlined. Now, this is great, and if you do this setup, then this is going to apply to all of your markdown files. [* ](https://youtu.be/K6qZkTz8GHs)

I also added an option that there's a new front matter key called `x color draw css`, which can contain two types of values. If it contains a valid CSS snippet, like in this case, I'm setting the background color of my host element to white smoke. [* ](https://youtu.be/K6qZkTz8GHs)

If I now click here, then you can see that the updated element now has the white smoke color. Well, if I turn to the light mode, then you can see that's a very light color in the background. [* ](https://youtu.be/K6qZkTz8GHs)

I can also add a file name here, so I'm going to call this file `override css`. This override CSS is also in my vault. I'll show you in a second: if I use this and I click here, then you can see that a couple of things have changed because in my `override css`, I added a border around the markdown md host, as well as I did some styling for the table. [* ](https://youtu.be/K6qZkTz8GHs)

In this case, I can show you how the override CSS looks; it is actually the same CSS or very similar to the previous one but has a bit of additional settings here. [* ](https://youtu.be/K6qZkTz8GHs)

So that is how the CSS works. Now, if you're wondering what the elements and classes are, then you can come to the developer console, and you need to initiate `xcalidro automate`. Let me just zoom in here so you can see this slightly better. [* ](https://youtu.be/K6qZkTz8GHs)

On `xcalidro automate`, I'm always saving the most recent markdown SVG as a variable. So you can come here, and you can actually check out how that SVG looks like. First of all, you can see my CSS styling at the top, as well as if I open the foreign object, you can see my hosting element with the `xcalitro mdhost` class. [* ](https://youtu.be/K6qZkTz8GHs)

If I open this up, then you can see the rendered HTML version of the markdown document, and this can give you a bit of background information on how to edit your stylesheet. [* ](https://youtu.be/K6qZkTz8GHs)

So that's all I wanted to show you. I think this is a great new feature, and this is going to give you plenty of flexibility to customize your views in Excalidraw. Thank you. [* ](https://youtu.be/K6qZkTz8GHs)

# YouTube Details

## YouTube Description

Link to the markdown-css file used in the video: https://github.com/zsviczian/obsidian-excalidraw-plugin/discussions/281

I did not mention it in the video, but it is important to understand, that the font typeface of the embedded document can only be set using the Plugin settings and/or the front-matter key. The reason for this limitation is that the fonts must be embedded into the SVG document, otherwise, they won't be available at the time of display. Excalidraw displays all images on the canvas by embedding them into IMG elements, links to external resources such as links to external fonts are not available in this setup...

-------

If you find the plugin and/or my videos helpful, please say thanks by buying me a coffee: https://ko-fi.com/zsolt

If you'd like to request a feature or report a bug, please raise it on GitHub: https://github.com/zsviczian/obsidian-excalidraw-plugin

If you want to connect, you can reach me (@zsviczian) in the Obsidian Members Group (OMG) on Discord or on Twitter.

Links

---------

My Blog: https://zsolt.blog
Obsidian: https://obsidian.md
Excaldiraw: https://excalidraw.com

## YouTube Transcript

[this video is about the advanced styling](https://youtu.be/K6qZkTz8GHs?t=0) [of markdown embeds](https://youtu.be/K6qZkTz8GHs?t=3) [so first of all i want to show you that](https://youtu.be/K6qZkTz8GHs?t=5) [in settings i've added an additional](https://youtu.be/K6qZkTz8GHs?t=8) [setting](https://youtu.be/K6qZkTz8GHs?t=10) [and that is right here css file so you](https://youtu.be/K6qZkTz8GHs?t=11) [can now specify a css file that is going](https://youtu.be/K6qZkTz8GHs?t=15) [to be](https://youtu.be/K6qZkTz8GHs?t=19) [used for styling the css file can be a](https://youtu.be/K6qZkTz8GHs?t=20) [normal markdown document or it can be a](https://youtu.be/K6qZkTz8GHs?t=24) [css document bottom line is it has to](https://youtu.be/K6qZkTz8GHs?t=27) [contain valid css code](https://youtu.be/K6qZkTz8GHs?t=30) [and here in this case i created this](https://youtu.be/K6qZkTz8GHs?t=34) [file](https://youtu.be/K6qZkTz8GHs?t=37) [called markdown css and i placed it in](https://youtu.be/K6qZkTz8GHs?t=38) [my fonts library and that is the file](https://youtu.be/K6qZkTz8GHs?t=42) [that i'm referencing right here so you](https://youtu.be/K6qZkTz8GHs?t=45) [can see this is the markdown css.md](https://youtu.be/K6qZkTz8GHs?t=48) [and within my markdown css.md](https://youtu.be/K6qZkTz8GHs?t=52) [i have](https://youtu.be/K6qZkTz8GHs?t=55) [this styling by the way here's a trick](https://youtu.be/K6qZkTz8GHs?t=56) [that you can apply you can see that i've](https://youtu.be/K6qZkTz8GHs?t=59) [placed in comments](https://youtu.be/K6qZkTz8GHs?t=61) [the top of the code block and with this](https://youtu.be/K6qZkTz8GHs?t=63) [i get syntax highlighting in the editor](https://youtu.be/K6qZkTz8GHs?t=66) [so that's just a small trick what you](https://youtu.be/K6qZkTz8GHs?t=71) [can see here is my styling for this](https://youtu.be/K6qZkTz8GHs?t=73) [document and you can see couple of](https://youtu.be/K6qZkTz8GHs?t=76) [things so first of all the entire](https://youtu.be/K6qZkTz8GHs?t=79) [document is hosted in an element with](https://youtu.be/K6qZkTz8GHs?t=81) [the class xcolidra mdhost and you can](https://youtu.be/K6qZkTz8GHs?t=84) [use this to do a couple of things for](https://youtu.be/K6qZkTz8GHs?t=88) [now i added some padding around the](https://youtu.be/K6qZkTz8GHs?t=91) [document but we'll see later what else](https://youtu.be/K6qZkTz8GHs?t=94) [you can do](https://youtu.be/K6qZkTz8GHs?t=96) [then you have the normal html](https://youtu.be/K6qZkTz8GHs?t=98) [components and you can add your styling](https://youtu.be/K6qZkTz8GHs?t=101) [for example i did a bit of styling](https://youtu.be/K6qZkTz8GHs?t=103) [around the table as well as i added](https://youtu.be/K6qZkTz8GHs?t=106) [styling so the anchors](https://youtu.be/K6qZkTz8GHs?t=109) [are](https://youtu.be/K6qZkTz8GHs?t=112) [underlined](https://youtu.be/K6qZkTz8GHs?t=112) [now this is great](https://youtu.be/K6qZkTz8GHs?t=114) [and if you do this setup then this is](https://youtu.be/K6qZkTz8GHs?t=116) [going to apply to all of your markdown](https://youtu.be/K6qZkTz8GHs?t=119) [files i also added an option that](https://youtu.be/K6qZkTz8GHs?t=121) [there's a new front matter key called x](https://youtu.be/K6qZkTz8GHs?t=125) [color draw css which can contain](https://youtu.be/K6qZkTz8GHs?t=128) [two](https://youtu.be/K6qZkTz8GHs?t=131) [types of values](https://youtu.be/K6qZkTz8GHs?t=132) [if it contains a valid css snippet like](https://youtu.be/K6qZkTz8GHs?t=134) [in this case i'm setting the](https://youtu.be/K6qZkTz8GHs?t=139) [background color of my host element](https://youtu.be/K6qZkTz8GHs?t=142) [white smoke](https://youtu.be/K6qZkTz8GHs?t=146) [and if i now click here then you can see](https://youtu.be/K6qZkTz8GHs?t=148) [that the updated element now has the](https://youtu.be/K6qZkTz8GHs?t=150) [white smoke color well if i](https://youtu.be/K6qZkTz8GHs?t=153) [turn to the light mode then you can see](https://youtu.be/K6qZkTz8GHs?t=156) [that that's a very light color in the](https://youtu.be/K6qZkTz8GHs?t=158) [background](https://youtu.be/K6qZkTz8GHs?t=162) [i can also add a file name here so i'm](https://youtu.be/K6qZkTz8GHs?t=164) [going to call this file over](https://youtu.be/K6qZkTz8GHs?t=167) [ride](https://youtu.be/K6qZkTz8GHs?t=170) [css](https://youtu.be/K6qZkTz8GHs?t=172) [and this override css is also in my](https://youtu.be/K6qZkTz8GHs?t=173) [vault](https://youtu.be/K6qZkTz8GHs?t=178) [i'll show you in a second if i use this](https://youtu.be/K6qZkTz8GHs?t=179) [and i click here then you can see that](https://youtu.be/K6qZkTz8GHs?t=182) [there's a couple of things have changed](https://youtu.be/K6qZkTz8GHs?t=184) [because in my overwrite css i added a](https://youtu.be/K6qZkTz8GHs?t=186) [border](https://youtu.be/K6qZkTz8GHs?t=189) [around](https://youtu.be/K6qZkTz8GHs?t=190) [the](https://youtu.be/K6qZkTz8GHs?t=191) [markdown md host as well as i did some](https://youtu.be/K6qZkTz8GHs?t=192) [styling for the table](https://youtu.be/K6qZkTz8GHs?t=196) [and in this case i can show you so this](https://youtu.be/K6qZkTz8GHs?t=198) [is how the](https://youtu.be/K6qZkTz8GHs?t=201) [override](https://youtu.be/K6qZkTz8GHs?t=202) [css looks like](https://youtu.be/K6qZkTz8GHs?t=204) [it is actually the](https://youtu.be/K6qZkTz8GHs?t=206) [same css or a very similar css to the](https://youtu.be/K6qZkTz8GHs?t=208) [previous one but has a bit of additional](https://youtu.be/K6qZkTz8GHs?t=211) [settings here](https://youtu.be/K6qZkTz8GHs?t=214) [so that is how the css works now if](https://youtu.be/K6qZkTz8GHs?t=216) [you're wondering](https://youtu.be/K6qZkTz8GHs?t=220) [what are the elements and classes then](https://youtu.be/K6qZkTz8GHs?t=222) [you can come to](https://youtu.be/K6qZkTz8GHs?t=226) [the developer console and you need to](https://youtu.be/K6qZkTz8GHs?t=228) [initiate xcali draw automate let me just](https://youtu.be/K6qZkTz8GHs?t=232) [zoom in here so you can see this](https://youtu.be/K6qZkTz8GHs?t=235) [slightly better](https://youtu.be/K6qZkTz8GHs?t=238) [and on xcalidro automate](https://youtu.be/K6qZkTz8GHs?t=240) [i'm always saving the most recent](https://youtu.be/K6qZkTz8GHs?t=243) [markdown](https://youtu.be/K6qZkTz8GHs?t=246) [svg as a variable so you can come here](https://youtu.be/K6qZkTz8GHs?t=247) [and you can actually check out how that](https://youtu.be/K6qZkTz8GHs?t=251) [svg looks like so first of all you can](https://youtu.be/K6qZkTz8GHs?t=255) [see here](https://youtu.be/K6qZkTz8GHs?t=258) [my css styling at the top](https://youtu.be/K6qZkTz8GHs?t=259) [as well as if i open the foreign object](https://youtu.be/K6qZkTz8GHs?t=262) [you can see my hosting element with the](https://youtu.be/K6qZkTz8GHs?t=266) [xcalitro mdhost](https://youtu.be/K6qZkTz8GHs?t=270) [class](https://youtu.be/K6qZkTz8GHs?t=272) [as well as if i open this up then you](https://youtu.be/K6qZkTz8GHs?t=273) [can see the rendered html](https://youtu.be/K6qZkTz8GHs?t=276) [version of the markdown document and](https://youtu.be/K6qZkTz8GHs?t=279) [this can give you a bit of](https://youtu.be/K6qZkTz8GHs?t=281) [background information on how to edit](https://youtu.be/K6qZkTz8GHs?t=284) [your style sheet](https://youtu.be/K6qZkTz8GHs?t=287) [so that's all i wanted to show you i](https://youtu.be/K6qZkTz8GHs?t=289) [think this is a great new feature and](https://youtu.be/K6qZkTz8GHs?t=292) [this is going to give you plenty of](https://youtu.be/K6qZkTz8GHs?t=294) [flexibility to](https://youtu.be/K6qZkTz8GHs?t=296) [customize your](https://youtu.be/K6qZkTz8GHs?t=298) [views in x color draw thank you](https://youtu.be/K6qZkTz8GHs?t=300) 

