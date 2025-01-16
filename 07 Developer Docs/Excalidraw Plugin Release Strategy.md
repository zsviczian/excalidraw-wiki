---
excalidraw-plugin: parsed
tags:
  - excalidraw
excalidraw-export-dark: false
excalidraw-autoexport: svg
excalidraw-export-transparent: true
aliases:
  - WIKI/07+Developer+Docs/Excalidraw+Plugin+Release+Strategy
permalink: releases
---
**Created**:: [[2024-08-04 Sunday]]
**Link**:: https://youtu.be/2poSS-Z91lY
**Duration**:: 8:22

You can explore the [[Excalidraw Release Notes|Excalidraw-Obsidian Release Notes]] here.


![Which release channel is the right for you?](https://youtu.be/2poSS-Z91lY)


# Summary
In this video, Zsolt explains the updated release channels for the Obsidian Excalidraw plugin, aiming to alleviate the concerns of users experiencing change fatigue due to frequent updates. He introduces a dedicated beta testing channel alongside normal updates, outlining the frequency and significance of each release. The video also details how users can install and manage updates through the Brat plugin, ensuring a smoother experience for both beta testers and stable release users.

![[Excalidraw Plugin Release Strategy.svg]]
# Key Takeaways
- The Obsidian Excalidraw plugin will have a new structured release system that includes a dedicated beta testing channel.
- Normal updates will occur approximately once a month and be available in the Obsidian Community plugins store.
- Users can manage beta installations and updates through the Brat plugin, which allows for on-going testing of the latest features while maintaining access to stable versions.

# Content
Hey everyone, it's Zsolt here. I wanted to grab a few minutes of your time to explain how the releases of the Obsidian Excalidraw plugin are changing. Essentially, some of you have asked to have less frequent releases because too frequent releases create change fatigue and maybe some anxiety for some of you. So, in this video, I'm going to walk you through that process. From now on, we are going to have a dedicated beta testing channel using the Brat plugin, and we're going to have the normal updates. [* ](https://youtu.be/2poSS-Z91lY?t=0)

Let's start with the normal updates. First of all, they're going to be available via the Obsidian Community plugins store, as until now, they will include a release description in the plugin release notes. I'm going to be targeting roughly one release per month, and this is going to happen unless there's some high-impact bugs that surface that need to be addressed mid-month. The plugin will notify you when there's an update available, but of course, you can also go to community plugins to see the updates. The normal monthly update will end typically with a zero in the release number, so your release number will be 2.3.0, 2.4.0, etc. If I have an interim bug fix release, I will bump the minor release number, so it would be 2.3.1 or 2.4.1 for a bug fix release that I need to issue mid-month, and any breaking changes that are not backward compatible will receive a new major version number, meaning 3.0.0 is in some way not compatible with 2.3.0. [* ](https://youtu.be/2poSS-Z91lY?t=45)

Now looking at the other side, this is the beta testing side. This is going to be available via the Brat plugin. Updates are going to be announced in the Visual Thinking Workshop Discord beta channel. I recommend that you join that; you will find the link to join Discord in the splash screen when you create a new Excalidraw drawing. Updates are going to be more frequent, or rather say they're going to be as until now—so typically weekly, or sometimes even multiple times during a week. If I have a beta release, it will carry the release number of the upcoming release with "Beta 1", "Beta 2", etc., to denote the beta releases. [* ](https://youtu.be/2poSS-Z91lY?t=116)

So, how does this all look like? Right now, I'm going to be releasing version 2.3.0; it's going to be released for both the Brat beta testing channel and, as this is the beginning of the month, it's going to be published in the normal channel. Then I will start to work on 2.4.0, and I'm going to be releasing Beta 1, Beta 2, etc. By the end of the month, I will release version 2.5.0. Now, there's a bit of a technical nuance here that you need to understand if you're a beta tester. If you're just following the normal channel, you don't need to understand this. If you're a beta tester, then you need to know that if you're doing beta testing, you will need to install the stable releases with Brat as well, and that's because Obsidian will not recognize 2.5.0 as more recent than 2.5.0-D beta 2. It is only Brat that allows you this feature. [* ](https://youtu.be/2poSS-Z91lY?t=210)

Now, there are various sources of changes that you need to understand. Some of them are in my control, and some of them are outside my control. Sometimes, changes that are outside my control—or maybe bug fixes that could be urgent but are in my control—can drive a situation where I have urgent bug fixes that need to be deployed. These are typically fixes that I believe may lead to data loss or some severe degradation of plugin features, and maybe some breaking changes that could be introduced by a new Obsidian release. So, if this is the case, that's when I'm going to be issuing a bug fix release mid-month to the normal channel as well. Hopefully, with this, you get a good understanding of how the new release structure is going to work. You will find this visual in the README of the plugin. [* ](https://youtu.be/2poSS-Z91lY?t=292)

Now let me show you how you can use Brat. To install Brat, you need to come over to Obsidian settings and, in community plugins, you need to click "Browse" and type in Brat, and then you can just simply install and enable Brat like this. Now, before I'm going to do anything with Brat, I'm going to head back to this list of plugins and click on Excalidraw. I'm going to click on the repository link because we are going to need the repository address to register the plugin in Brat. I'm just going to copy this to the clipboard and head back to Obsidian. Then, in Obsidian, I'm going to start the command palette and type in "Brat add a beta plugin for testing". I'm going to click on this command, paste the repository link here, and once I've pasted it, I can press "Add Plugin" in the top right. I’m going to see a message that the plugin was added, and now if I check here, you can already see that the plugin automatically updated to the latest beta version. [* ](https://youtu.be/2poSS-Z91lY?t=355)

Now, if later on I want to check for a new beta version of the plugin, I can just simply start the command palette, type in "Brat", and I can choose here to choose a single plugin version to update. When I click this, I can choose which plugin I want to test. Currently, I only have Obsidian Excalidraw on my beta plugin list. I then click that, and Brat will check and, here you can see that right now I have the latest beta version. If you decide to be a beta tester for Excalidraw and you want to continue receiving weekly or even more frequent updates with the shiny new things that come from Excalidraw.com and new features that I'm building, then you need to install Brat. With Brat, you will need to install the stable version as well as the interim versions. All you need to do is use the command palette and update a single plugin version as I just showed you, and with that, Brat is going to update the plugin for you. That's all I wanted to share with you today. Hopefully, this will release some of the anxiety for those of you who don't like too frequent updates while still retaining the flexibility for those of you who like to play with the shiny new things. Let me know how it works. Thank you! [* ](https://youtu.be/2poSS-Z91lY?t=487)

# YouTube Details

## YouTube Description

The release strategy from this video: https://excalidraw-obsidian.online/Hobbies/Excalidraw+Blog/Excalidraw+Plugin+Release+Strategy

----

✏️ Sign up for the Visual Thinking Workshop: https://www.visual-thinking-workshop.com/ 
🚀 Cohort 10 starts on 24 August 2024. 📔 We will process Simple Marketing for Smart People into a Book on a Page

-----

If you find  my videos helpful, please say thanks by buying me a coffee: https://ko-fi.com/zsolt

📩 If you want to connect, you can reach me: (@zsviczian) on the Obsidian Members Group (OMG) on Discord, or on 🐦 Twitter: https://twitter.com/zsviczian

-----

The video explains my new release approach for the Exclidraw plugin. If you want to continue to receive frequent updates join the beta tester community and get frequent updates via BRAT. If you're happy with monthly updates, then simply update the plugin via Obsidian Community Plugins whenever an update is available.

-----

Timestamps:
[00:00](https://youtu.be/2poSS-Z91lY?t=0) Intro
[00:23](https://youtu.be/2poSS-Z91lY?t=23) Release approach bird's eye view
[00:39](https://youtu.be/2poSS-Z91lY?t=39) Normal updates
[02:04](https://youtu.be/2poSS-Z91lY?t=124) Beta updates via BRAT
[04:15](https://youtu.be/2poSS-Z91lY?t=255) Interim (emergency) releases
[05:30](https://youtu.be/2poSS-Z91lY?t=330) Installing BRAT and configuring Excalidraw
[08:01](https://youtu.be/2poSS-Z91lY?t=481) Closing thoughts

-------

🍿Watch next: 
📽️ The Excalidraw-Obsidian Showcase: 57 key features in just 17 minutes https://youtu.be/P_Q6avJGoWI
📽️ Getting Started with Excalidraw https://youtu.be/QKnQgSjJVuc
📽️ Getting Started with ExcaliBrain https://youtu.be/8LE_QdYQZVk
📽️ The Playful PKM Castle: A Whirlwind Tour of Zsolt's Visual Thinking World! https://youtu.be/X0AmZGQ_7z4
📽️ Idea Mixer https://youtu.be/ItV8PEaPorE
📽️ 6 Strategies for Linking Visual Thoughts https://youtu.be/qiKuqMcNWgU
📽️ Visually Connect Ideas https://youtu.be/mvMQcz401yo
📽️ How are these related? https://youtu.be/N6EFydv0tug

📽️ Deconstruct Elements Script: https://youtu.be/HRtaaD34Zzg
📽️ Knowledge Discovery Using Icons https://youtu.be/_OEljzZ33H8
📽️ Block Reference Images https://youtu.be/yZQoJg2RCKI
📽️ Double Bubble Map https://youtu.be/Hm4En13TDjs
📽️Visual Tools for Transforming Information Into Knowledge https://youtu.be/i5J5pzICrho

---------

Visual Thinking Workshop: https://www.visual-thinking-workshop.com/
My blog: https://zsolt.blog/ 
Obsidian: https://obsidian.md
Excalidraw-Obsidian: https://github.com/zsviczian/obsidian-excalidraw-plugin/

## YouTube Transcript

[hey everyone it's jolt here I wanted to](https://youtu.be/2poSS-Z91lY?t=0) [grab a few minutes of your time to](https://youtu.be/2poSS-Z91lY?t=3) [explain to you how the releases of the](https://youtu.be/2poSS-Z91lY?t=5) [obsidian excal plugin are changing](https://youtu.be/2poSS-Z91lY?t=8) [essentially some of you have asked to](https://youtu.be/2poSS-Z91lY?t=11) [have less frequent releases because two](https://youtu.be/2poSS-Z91lY?t=14) [frequent releases create change fatigue](https://youtu.be/2poSS-Z91lY?t=17) [and maybe some anxiety for some of you](https://youtu.be/2poSS-Z91lY?t=20) [so in this video I'm going to walk you](https://youtu.be/2poSS-Z91lY?t=23) [through that process from now on we are](https://youtu.be/2poSS-Z91lY?t=25) [going to have a dedic ated beta testing](https://youtu.be/2poSS-Z91lY?t=28) [Channel using the brat plugin and we're](https://youtu.be/2poSS-Z91lY?t=31) [going to have the normal updates so](https://youtu.be/2poSS-Z91lY?t=34) [let's start with the normal updates now](https://youtu.be/2poSS-Z91lY?t=37) [first of all they're going to be](https://youtu.be/2poSS-Z91lY?t=40) [available via the obsidian Community](https://youtu.be/2poSS-Z91lY?t=42) [plugins store as until now they will](https://youtu.be/2poSS-Z91lY?t=44) [include a release description in the](https://youtu.be/2poSS-Z91lY?t=48) [plug-in release notes I'm going to be](https://youtu.be/2poSS-Z91lY?t=51) [targeting roughly One release per month](https://youtu.be/2poSS-Z91lY?t=54) [and this is going to to happen unless](https://youtu.be/2poSS-Z91lY?t=58) [there's some high impact bugs that](https://youtu.be/2poSS-Z91lY?t=61) [surface that need to be addressed mid](https://youtu.be/2poSS-Z91lY?t=63) [Monon the plugin will notify you when](https://youtu.be/2poSS-Z91lY?t=66) [there's an update available but of](https://youtu.be/2poSS-Z91lY?t=69) [course you can also go to community](https://youtu.be/2poSS-Z91lY?t=71) [plugins to see the update the normal](https://youtu.be/2poSS-Z91lY?t=73) [monthly update will end typically with a](https://youtu.be/2poSS-Z91lY?t=77) [zero the release number so your release](https://youtu.be/2poSS-Z91lY?t=81) [number will be](https://youtu.be/2poSS-Z91lY?t=84) [2.3.0](https://youtu.be/2poSS-Z91lY?t=86) [2.4.0 Etc](https://youtu.be/2poSS-Z91lY?t=88) [if I have an interim Buck fix release I](https://youtu.be/2poSS-Z91lY?t=91) [will bump the minor release number so it](https://youtu.be/2poSS-Z91lY?t=95) [would be](https://youtu.be/2poSS-Z91lY?t=98) [2.3.1 or](https://youtu.be/2poSS-Z91lY?t=99) [2.4.1 for a buck fix release that I need](https://youtu.be/2poSS-Z91lY?t=101) [to issue mid Monon and any breaking](https://youtu.be/2poSS-Z91lY?t=105) [changes that are not Backward Compatible](https://youtu.be/2poSS-Z91lY?t=108) [we receive a new major version number](https://youtu.be/2poSS-Z91lY?t=112) [meaning](https://youtu.be/2poSS-Z91lY?t=115) [3.0.0 is](https://youtu.be/2poSS-Z91lY?t=118) [in some way not compatible with](https://youtu.be/2poSS-Z91lY?t=120) [2.3.0 now looking at the other side so](https://youtu.be/2poSS-Z91lY?t=124) [this is the beta testing side this is](https://youtu.be/2poSS-Z91lY?t=127) [going to be available via the brat](https://youtu.be/2poSS-Z91lY?t=130) [plug-in updates are going to be](https://youtu.be/2poSS-Z91lY?t=133) [announced in the visual thinking](https://youtu.be/2poSS-Z91lY?t=136) [Workshop Discord beta Channel I](https://youtu.be/2poSS-Z91lY?t=138) [recommend that you join that you will](https://youtu.be/2poSS-Z91lY?t=141) [find the link to join Discord in the](https://youtu.be/2poSS-Z91lY?t=144) [splash screen when you create a new](https://youtu.be/2poSS-Z91lY?t=148) [escalator](https://youtu.be/2poSS-Z91lY?t=150) [drawing updates are going to be more](https://youtu.be/2poSS-Z91lY?t=151) [frequent or rather say they're going to](https://youtu.be/2poSS-Z91lY?t=154) [be as until now so typically weekly is](https://youtu.be/2poSS-Z91lY?t=157) [sometime even multiple times during a](https://youtu.be/2poSS-Z91lY?t=160) [week if I have a Beta release it will](https://youtu.be/2poSS-Z91lY?t=162) [carry the release number of the upcoming](https://youtu.be/2poSS-Z91lY?t=167) [release with Dash beta 1 beta 2 Etc to](https://youtu.be/2poSS-Z91lY?t=170) [denote the beta releases so how does](https://youtu.be/2poSS-Z91lY?t=176) [this all look like like right now I'm](https://youtu.be/2poSS-Z91lY?t=179) [going to be releasing](https://youtu.be/2poSS-Z91lY?t=181) [2.3.0 it's going to be released for both](https://youtu.be/2poSS-Z91lY?t=184) [the brat beta testing Channel and as](https://youtu.be/2poSS-Z91lY?t=188) [this is the beginning of the month it's](https://youtu.be/2poSS-Z91lY?t=191) [going to be published in the normal](https://youtu.be/2poSS-Z91lY?t=193) [Channel then I will start to work on](https://youtu.be/2poSS-Z91lY?t=196) [2.4.0 and I'm going to be releasing beta](https://youtu.be/2poSS-Z91lY?t=200) [1 beta 2](https://youtu.be/2poSS-Z91lY?t=203) [Etc and when the end of the month comes](https://youtu.be/2poSS-Z91lY?t=205) [then I'm going to be releasing](https://youtu.be/2poSS-Z91lY?t=209) [[Music]](https://youtu.be/2poSS-Z91lY?t=212) [2.5.0 now there's a bit of a technical](https://youtu.be/2poSS-Z91lY?t=213) [Nuance here that you need to understand](https://youtu.be/2poSS-Z91lY?t=216) [if you're a beta tester so if you're](https://youtu.be/2poSS-Z91lY?t=220) [just following the normal Channel you](https://youtu.be/2poSS-Z91lY?t=222) [don't need to understand this if you're](https://youtu.be/2poSS-Z91lY?t=225) [a beta tester then you need to know that](https://youtu.be/2poSS-Z91lY?t=227) [if you're doing beta testing you will](https://youtu.be/2poSS-Z91lY?t=231) [need to install the stable releases with](https://youtu.be/2poSS-Z91lY?t=233) [brat as well and that's because obsidian](https://youtu.be/2poSS-Z91lY?t=236) [will not recognize](https://youtu.be/2poSS-Z91lY?t=240) [2.5.0 as more recent than](https://youtu.be/2poSS-Z91lY?t=243) [2.5.0 D beta 2 it is only brat that](https://youtu.be/2poSS-Z91lY?t=246) [allows you this](https://youtu.be/2poSS-Z91lY?t=251) [feature now there are various sources of](https://youtu.be/2poSS-Z91lY?t=253) [changes that you need to understand some](https://youtu.be/2poSS-Z91lY?t=258) [of them are in my control and some of](https://youtu.be/2poSS-Z91lY?t=262) [them are outside my control and](https://youtu.be/2poSS-Z91lY?t=264) [sometimes changes that are outside my](https://youtu.be/2poSS-Z91lY?t=268) [control or maybe bug fixes that could be](https://youtu.be/2poSS-Z91lY?t=271) [urgent but they are in my control can](https://youtu.be/2poSS-Z91lY?t=275) [drive a situation that I have urgent bug](https://youtu.be/2poSS-Z91lY?t=279) [fixes that need to be deployed these are](https://youtu.be/2poSS-Z91lY?t=282) [typically fixes that I](https://youtu.be/2poSS-Z91lY?t=285) [believe may lead to data loss or some](https://youtu.be/2poSS-Z91lY?t=288) [severe degradation of plug-in features](https://youtu.be/2poSS-Z91lY?t=292) [and maybe some breaking changes that](https://youtu.be/2poSS-Z91lY?t=295) [could be in introduced by a new obsidian](https://youtu.be/2poSS-Z91lY?t=298) [release so if this is the case that's](https://youtu.be/2poSS-Z91lY?t=301) [when I'm going to be issuing a bug fix](https://youtu.be/2poSS-Z91lY?t=304) [release mid Monon to the normal Channel](https://youtu.be/2poSS-Z91lY?t=309) [as well so hopefully with this you get a](https://youtu.be/2poSS-Z91lY?t=313) [good understanding of how the new](https://youtu.be/2poSS-Z91lY?t=317) [release structure is going to work you](https://youtu.be/2poSS-Z91lY?t=320) [will find this visual in the read me of](https://youtu.be/2poSS-Z91lY?t=322) [the plug-in and now let me show you how](https://youtu.be/2poSS-Z91lY?t=326) [you can use brat to install brat you](https://youtu.be/2poSS-Z91lY?t=329) [need to come over to obsidian settings](https://youtu.be/2poSS-Z91lY?t=332) [and in community plugins you need to](https://youtu.be/2poSS-Z91lY?t=335) [click browse and type in brat and then](https://youtu.be/2poSS-Z91lY?t=337) [you can just simply install and then](https://youtu.be/2poSS-Z91lY?t=341) [enable brat like this now before I'm](https://youtu.be/2poSS-Z91lY?t=344) [going to do anything with brat I'm going](https://youtu.be/2poSS-Z91lY?t=348) [to head back to this list of plugins and](https://youtu.be/2poSS-Z91lY?t=351) [click on excetra and I'm going to click](https://youtu.be/2poSS-Z91lY?t=354) [here on the repository link link because](https://youtu.be/2poSS-Z91lY?t=357) [we are going to need the repository](https://youtu.be/2poSS-Z91lY?t=360) [address to register the plug-in in brat](https://youtu.be/2poSS-Z91lY?t=362) [so I'm just going to copy this to the](https://youtu.be/2poSS-Z91lY?t=366) [clipboard and head back to obsidian and](https://youtu.be/2poSS-Z91lY?t=368) [then in obsidian I'm going to start the](https://youtu.be/2poSS-Z91lY?t=372) [command pallet and type in brat add a](https://youtu.be/2poSS-Z91lY?t=374) [beta plugin for testing I'm going to](https://youtu.be/2poSS-Z91lY?t=379) [click on this command and I'm going to](https://youtu.be/2poSS-Z91lY?t=382) [paste the repository link here and once](https://youtu.be/2poSS-Z91lY?t=385) [I've pasted it I can press add plugin in](https://youtu.be/2poSS-Z91lY?t=389) [the top right I'm going to see a message](https://youtu.be/2poSS-Z91lY?t=393) [that the plugin was added and now if I](https://youtu.be/2poSS-Z91lY?t=395) [check here then you can already see that](https://youtu.be/2poSS-Z91lY?t=399) [the plug-in automatically updated to the](https://youtu.be/2poSS-Z91lY?t=402) [latest beta version now if later on I](https://youtu.be/2poSS-Z91lY?t=406) [want to check for a new beta version of](https://youtu.be/2poSS-Z91lY?t=410) [the plugin I can just simply start the](https://youtu.be/2poSS-Z91lY?t=413) [common pallet type in brat and I can](https://youtu.be/2poSS-Z91lY?t=415) [choose here to choose a single plugin](https://youtu.be/2poSS-Z91lY?t=420) [version to update and when I click this](https://youtu.be/2poSS-Z91lY?t=423) [I can choose which plugin I want to test](https://youtu.be/2poSS-Z91lY?t=426) [currently I only have obsidian X colit](https://youtu.be/2poSS-Z91lY?t=430) [Raw on my Beta plugin list and then I](https://youtu.be/2poSS-Z91lY?t=432) [click that then brat will check and here](https://youtu.be/2poSS-Z91lY?t=436) [you can see that right now I have the](https://youtu.be/2poSS-Z91lY?t=438) [latest beta version if you decide to be](https://youtu.be/2poSS-Z91lY?t=441) [a beta tester for exol draw and you want](https://youtu.be/2poSS-Z91lY?t=445) [to continue to receive](https://youtu.be/2poSS-Z91lY?t=447) [weekly or even more frequent update with](https://youtu.be/2poSS-Z91lY?t=450) [the shiny new things that come from](https://youtu.be/2poSS-Z91lY?t=453) [exit.com and new features that I'm](https://youtu.be/2poSS-Z91lY?t=456) [building then you need to install brat](https://youtu.be/2poSS-Z91lY?t=458) [and with brat you will need to install](https://youtu.be/2poSS-Z91lY?t=461) [the stable version as well as the](https://youtu.be/2poSS-Z91lY?t=464) [interim versions all you need to do is](https://youtu.be/2poSS-Z91lY?t=467) [to use the common pallet and update a](https://youtu.be/2poSS-Z91lY?t=469) [single plug-in version as I just showed](https://youtu.be/2poSS-Z91lY?t=472) [you and with that brat is going to](https://youtu.be/2poSS-Z91lY?t=475) [update the plugin for you that's all I](https://youtu.be/2poSS-Z91lY?t=479) [wanted to share with you today hopefully](https://youtu.be/2poSS-Z91lY?t=482) [this will release some of the anxiety](https://youtu.be/2poSS-Z91lY?t=484) [for those of you who don't like too](https://youtu.be/2poSS-Z91lY?t=487) [frequent updates and at the same time](https://youtu.be/2poSS-Z91lY?t=489) [still retain the flexibility for those](https://youtu.be/2poSS-Z91lY?t=492) [of you who like to play with the shiny](https://youtu.be/2poSS-Z91lY?t=495) [new things let me know how it works](https://youtu.be/2poSS-Z91lY?t=497) [thank you](https://youtu.be/2poSS-Z91lY?t=501) 


%%
# Excalidraw Data

## Text Elements
Plugin bug-fixes ^4mXk3cWY

Normal ^dv3QmQdb

Sources of change ^evdWLKaE

Breaking changes that are not backward compatible will receive a new major version number (e.g. 3.0.0) ^mnaglhP6

BRAT ^jLSQva9h

Interim beta updates carry the release number of the upcoming release with "-beta-1", "-2", "-3" to denote beta releases ^YHuRQstq

Available via plugin update in Obsidian Community Plugins ^NJn6ctfL

Includes release description in Plugin Release Notes ^1pPsr24w

Targeting one release per month, unless high-impact bugs surface ^yceZPmMw

Plugin notifies user when an update is available ^VzCRSZe7

Updates are available via the Obsidian BRAT plugin ^ZXO3ADJL

Updates are announced on the Visual Thinking Workshop Discord Beta Channel ^6RzvDOrR

Updates are more frequent (as until now) ^u3nGgrsG

Within
my control ^LHZtlxXZ

May be
urgent ^oBH8cpzE

Can
wait ^KQEmKLHt

Continuous excalidraw.com releases ^eO2iPvB2

Obsidian-Excalidraw Plugin
Release Channels ^4i2Xn1tB

Continuous Obsidian releases ^maj2ATpY

2.5.1 ^hInL4Abf

Out of
my control ^i1vLExNh

2.6.0-beta-4 ^iu0OGGzw

2.6.0 ^rXGuCEsp

Beginning of the month ^jafRJwif

Whenever relevant ^328FSk5J

Plugin Enhancements ^6E89W3Gg

2.3.0 ^XQY8Wy25

2.4.0-beta-1 ^RhpZX0RZ

2.4.0-beta-2 ^3ILbjvcQ

2.5.0-beta-1 ^yT6hI6jr

2.5.0-beta-2 ^3ZES93Pr

2.5.0 ^4zqKhSL3

2.6.0-beta-1 ^TvaEkztC

2.6.0-beta-2 ^tLI42wO2

2.6.0-beta-3 ^1a5zyt9U

Beginning of the month ^cAe73qoE

Interim bugfix releases end with a bump in minor release (e.g.: 2.3.1; 2.4.1;...) ^blxERLF6

Beginning of the month ^N5M5IFgT

Urgent fixes that
risk data loss or severe degradation
of plugin features...
and breaking changes
introduced by a new Obsidian release



 ^1HsRVb1q

Normal monthly update release numbers end with .0 (e.g. 2.3.0; 2.4.0; ...) ^VW2AZsA0

One new feature was developed during the month ^NZr7U1Qr

Two new features were develop during the month ^AsYuRSuT

An urgent bugfix for 2.5.0 ^YWJeswoF

2.5.0 ^xKnyxO9i

Because Obsidian will not list 2.5.0 as an upgrade to 2.5.0-beta-2...

Beta testers get stable releases also via BRAT ^9whtfWhZ

If you are a beta tester you always update via BRAT even for stable versions ^dcRQ2Gu9

2.5.1 ^g2JeCOGE

2.6.0 ^n7HOP8MI

BRAT ^qjIfvlkg

Normal ^FCsuQeRB

2.3.0 ^jDZ4KtKL

new feature 2 ^hA2rQ4hE

new feature 1 ^jHW1qAx8

## Embedded Files
35f8dc1191ff4cf9004f33dca7f2ca0e3c4d363b: [[Digital Workshop Discord Logo]]

e9655c24af0061edd0ecbe6b42dc440132f83260: [[Logo - Discord - Flaticon.svg]]

bfe81d78b9937bd7832aafc637e5fc30d5828a5f: [[Icon - attention, significance - flaticon.svg]]

## Drawing
```compressed-json
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

4CAAA===
```
%%
