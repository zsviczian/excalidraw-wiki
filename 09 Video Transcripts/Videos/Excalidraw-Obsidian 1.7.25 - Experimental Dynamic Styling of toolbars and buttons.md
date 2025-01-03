**Created**:: [[2022-10-16 Sunday]]
**Link**:: https://youtu.be/LtR04fNTKTM
**Duration**:: 4:14

![Excalidraw-Obsidian 1.7.25 - Experimental Dynamic Styling of toolbars and buttons](https://youtu.be/LtR04fNTKTM)

# Summary
In the video, the creator introduces experimental dynamic styling for toolbars and buttons in Excalidraw within Obsidian. This feature allows users to customize the toolbar color based on the background color of the image, enhancing visual coherence. The creator shares a script for users to implement this functionality, with an intention to possibly integrate it into the core product in the future.

# Key Takeaways
- Dynamic styling allows toolbars in Excalidraw to match the background color of images for improved aesthetics.
- Users will need basic programming skills to implement the experimental feature; a script is provided.
- The script must be placed in the startup scripts folder, and users should ensure Excalidraw is fully loaded for the script to work successfully.

# Content
Excalidraw-Obsidian 1.7.25 - Experimental Dynamic Styling of Toolbars and Buttons  
https://youtu.be/LtR04fNTKTM  

Emojis in Excalidraw dark mode simply don't look good; similarly, images on an iPad in dark mode are inverted. You could say that instead of using dark mode, you should use a dark background color, like in this case, and yes, the MOG looks perfect. However, the toolbar is simply too bright; it burns a hole in your eye. [* ](https://youtu.be/LtR04fNTKTM?t=0)  

In this release of Excalidraw Obsidian, I'm releasing some experimental functionality that allows you to programmatically customize the color of the tools panel depending on the background color of the image. See how this toolbar has a different color compared to this toolbar, or this, or this. In each case, the toolbar has a color that harmonizes well with the background color of the image. If it's dark, then it's dark; if it's light, it's light. [* ](https://youtu.be/LtR04fNTKTM?t=25)  

Right now, you need some minimal programming skills to get this implemented; it's not that difficult. I'm going to share the script you need in the video description, but you still need to do some setup yourself. Later on, I might add this to the core product, and then it's going to become simply a setting in the plug-in settings. But for now, you need to do two things: create a template or script and place it in a folder that is your startup script folder. This is the script you need to implement. [* ](https://youtu.be/LtR04fNTKTM?t=61)  

The script looks long, but most of it is just calculation of colors and then updating various stylesheet variables. The program implements the Excalidraw automate on-canvas color change hook which receives three variables: the Excalidraw automate object, the view for which you're updating the tools panel, and the color of the background of the image. I'm not going to talk you through the script; if you're interested, you can read through it. I'll be very interested if you make some changes to the colors. I would like to learn from you and then maybe take these learnings together and publish the final solution in the plug-in settings. [* ](https://youtu.be/LtR04fNTKTM?t=109)  

So, you need to create this script. I've placed this script under my template folder in a subfolder called startup, and here's the script itself. Then you need to go to the Templater settings, scroll down to the startup templates, and you need to select your startup script and click "Add New Startup Template." Once you're done, you need to restart Obsidian or simply restart Templater from Community plugins by scrolling down and clicking "Turn Off" and then "Turn On." When you do this, Templater will initiate the startup scripts. [* ](https://youtu.be/LtR04fNTKTM?t=150)  

The startup script is written in such a way that it will take five seconds and do a first attempt, and if it's unsuccessful, it will try again in 10 seconds; that is to give Excalidraw enough time to load and run. If it's not successful, in the developer console (Ctrl + Shift + I or Command + Shift + I on the Mac) you should see some messages. If it's successful, you will see "Installing Excalidraw style hook," and if it's unsuccessful, you will see an error message. [* ](https://youtu.be/LtR04fNTKTM?t=202)  

So that's all I wanted to share with you today. Look for the script in the description and let me know how you like it, and especially let me know if you modify the script; I'd like to learn from the styling that you're doing. Thank you. [* ](https://youtu.be/LtR04fNTKTM?t=236)

# YouTube Details

## YouTube Description

If you find the plugin and/or my videos helpful, please say thanks by buying me a coffee: https://ko-fi.com/zsolt

If you'd like to request a feature or report a bug, please raise it on GitHub: https://github.com/zsviczian/obsidian-excalidraw-plugin

If you want to connect, you can reach me (@zsviczian) in the Obsidian Members Group (OMG) on Discord or on Twitter. 

Links: 

---------

The onColorChangeHook script: https://gist.github.com/zsviczian/c7223c5b4af30d5c88a0cae05300305c
My blog: https://zsolt.blog/ 
Obsidian: https://obsidian.md
Excalidraw-Obsidian 1.7.25 release notes: https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/1.7.25

---------

Credits: 
The icon on the video thumbnail is created by Siipkan Creative - Flaticon (https://www.flaticon.com/free-icons/experiment)

## YouTube Transcript

[emojis in excalator dark mode simply](https://youtu.be/LtR04fNTKTM?t=0) [don't look good similarly images on an](https://youtu.be/LtR04fNTKTM?t=3) [iPad in dark mode are inverted](https://youtu.be/LtR04fNTKTM?t=6) [you could say that instead of using dark](https://youtu.be/LtR04fNTKTM?t=9) [mode you use a dark background color](https://youtu.be/LtR04fNTKTM?t=11) [like in this case and yes the MOG looks](https://youtu.be/LtR04fNTKTM?t=14) [perfect however the toolbar is simply](https://youtu.be/LtR04fNTKTM?t=18) [too bright it burns a hole in your eye](https://youtu.be/LtR04fNTKTM?t=21) [in this release of excalator obsidian](https://youtu.be/LtR04fNTKTM?t=25) [I'm releasing some experimental](https://youtu.be/LtR04fNTKTM?t=28) [functionality that allows you to](https://youtu.be/LtR04fNTKTM?t=31) [programmatically customize the color of](https://youtu.be/LtR04fNTKTM?t=34) [the tools panel depending on the](https://youtu.be/LtR04fNTKTM?t=37) [background color of the image see how](https://youtu.be/LtR04fNTKTM?t=40) [this toolbar has a different color](https://youtu.be/LtR04fNTKTM?t=42) [compared to this toolbar compared to](https://youtu.be/LtR04fNTKTM?t=45) [this or this or this in each case the](https://youtu.be/LtR04fNTKTM?t=48) [toolbar has a color that harmonizes well](https://youtu.be/LtR04fNTKTM?t=52) [with the background color of the image](https://youtu.be/LtR04fNTKTM?t=55) [if it's dark then it's dark if it's](https://youtu.be/LtR04fNTKTM?t=57) [light it's light](https://youtu.be/LtR04fNTKTM?t=60) [right now you need some minimal](https://youtu.be/LtR04fNTKTM?t=61) [programming skills to get this](https://youtu.be/LtR04fNTKTM?t=64) [implemented it's not that difficult I'm](https://youtu.be/LtR04fNTKTM?t=66) [going to share the script you need in](https://youtu.be/LtR04fNTKTM?t=69) [the video description but you still need](https://youtu.be/LtR04fNTKTM?t=72) [to do some setup yourself later on I](https://youtu.be/LtR04fNTKTM?t=74) [might add this to the core product and](https://youtu.be/LtR04fNTKTM?t=78) [then it's going to become simply a](https://youtu.be/LtR04fNTKTM?t=80) [setting in plug-in settings but for now](https://youtu.be/LtR04fNTKTM?t=82) [you need to do two things you need to](https://youtu.be/LtR04fNTKTM?t=85) [create a template or script and place it](https://youtu.be/LtR04fNTKTM?t=88) [in a folder that is your startup script](https://youtu.be/LtR04fNTKTM?t=92) [folder this is the script you need to](https://youtu.be/LtR04fNTKTM?t=95) [implement the script looks long but most](https://youtu.be/LtR04fNTKTM?t=98) [of it is just calculation of colors and](https://youtu.be/LtR04fNTKTM?t=101) [then update of various stylesheet](https://youtu.be/LtR04fNTKTM?t=105) [variables](https://youtu.be/LtR04fNTKTM?t=108) [the program implements the excalator](https://youtu.be/LtR04fNTKTM?t=109) [automate on canvas color change hook](https://youtu.be/LtR04fNTKTM?t=113) [which receives three variables the](https://youtu.be/LtR04fNTKTM?t=116) [excalator automate object the view for](https://youtu.be/LtR04fNTKTM?t=119) [which you're updating the tools panel](https://youtu.be/LtR04fNTKTM?t=122) [and the color of the background of the](https://youtu.be/LtR04fNTKTM?t=125) [image](https://youtu.be/LtR04fNTKTM?t=129) [I'm not going to talk you through the](https://youtu.be/LtR04fNTKTM?t=130) [script if you're interested you can read](https://youtu.be/LtR04fNTKTM?t=132) [through and I'll be very interested if](https://youtu.be/LtR04fNTKTM?t=134) [you make some changes to the colors I](https://youtu.be/LtR04fNTKTM?t=137) [would like to learn from you and then](https://youtu.be/LtR04fNTKTM?t=140) [maybe take these learnings together and](https://youtu.be/LtR04fNTKTM?t=143) [then publish the final solution in](https://youtu.be/LtR04fNTKTM?t=146) [plugin settings](https://youtu.be/LtR04fNTKTM?t=149) [so you need to create this script I've](https://youtu.be/LtR04fNTKTM?t=150) [placed this script under my template or](https://youtu.be/LtR04fNTKTM?t=153) [folder in a subfolder called startup and](https://youtu.be/LtR04fNTKTM?t=155) [here's the script itself and then you](https://youtu.be/LtR04fNTKTM?t=160) [need to go to the templator settings and](https://youtu.be/LtR04fNTKTM?t=163) [scroll down to the startup templates and](https://youtu.be/LtR04fNTKTM?t=166) [you need to select your startup script](https://youtu.be/LtR04fNTKTM?t=170) [and you need to click add new startup](https://youtu.be/LtR04fNTKTM?t=173) [template once you're done you need to](https://youtu.be/LtR04fNTKTM?t=177) [restart obsidian or just simply restart](https://youtu.be/LtR04fNTKTM?t=180) [templature from Community plugins by](https://youtu.be/LtR04fNTKTM?t=183) [scrolling down and clicking](https://youtu.be/LtR04fNTKTM?t=186) [turn off and turn on when you do this](https://youtu.be/LtR04fNTKTM?t=191) [templature will initiate the startup](https://youtu.be/LtR04fNTKTM?t=194) [scripts the startup script is written in](https://youtu.be/LtR04fNTKTM?t=197) [such a way that it will take five](https://youtu.be/LtR04fNTKTM?t=202) [seconds and do a first attempt and if](https://youtu.be/LtR04fNTKTM?t=205) [it's unsuccessful it will try again in](https://youtu.be/LtR04fNTKTM?t=208) [10 seconds that is to give X color draw](https://youtu.be/LtR04fNTKTM?t=211) [enough time to load and run](https://youtu.be/LtR04fNTKTM?t=215) [if it's not successful in developer](https://youtu.be/LtR04fNTKTM?t=218) [console Ctrl shift I or command shift I](https://youtu.be/LtR04fNTKTM?t=221) [on the Mac you should see some messages](https://youtu.be/LtR04fNTKTM?t=225) [if it's successful you will see](https://youtu.be/LtR04fNTKTM?t=228) [installing excalator style hook if it's](https://youtu.be/LtR04fNTKTM?t=230) [unsuccessful you will see an error](https://youtu.be/LtR04fNTKTM?t=233) [message](https://youtu.be/LtR04fNTKTM?t=235) [so that's all I wanted to share with you](https://youtu.be/LtR04fNTKTM?t=236) [today look for the script in the](https://youtu.be/LtR04fNTKTM?t=239) [description and let me know how you like](https://youtu.be/LtR04fNTKTM?t=241) [it and especially let me know if you](https://youtu.be/LtR04fNTKTM?t=245) [modify the script I'd like to learn from](https://youtu.be/LtR04fNTKTM?t=247) [The Styling that you're doing](https://youtu.be/LtR04fNTKTM?t=250) [thank you](https://youtu.be/LtR04fNTKTM?t=252) 

