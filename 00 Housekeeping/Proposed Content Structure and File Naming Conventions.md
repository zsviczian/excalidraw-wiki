# [[Proposed Content Structure and File Naming Conventions]]

## File Naming Conventions
Image and other resource files follow the `type - keywords - source` generic structure.

Types are:
- Illustration: Excalidraw drawings used to illustrate a point e.g.: [[Illustration - joining Discord community.svg]]
- Picture: Typically an AI generated image or other non-photo from the Internet. e.g.: [[Picture - man writing at PC - midjourney.png]]
- Photo: A real photo e.g. None as yet.
- Screenshot: e.g. [[Screenshot - Excalidraw splash screen.png]]

Each page in the Wiki is an Excalidraw file, even if the drawing features are not always utilized. When you create a new note in the Vault, Templater automatically generates an Excalidraw template file with the correct document properties, along with a blank SVG file. When naming your files, use clear and descriptive titles that naturally reflect the content of the note. Feel free to use spaces and capital letters to ensure the title is as user-friendly and understandable as possible.​

## Proposed Content Structure
This structure is only recommended. This was generated with ChatGPT to give us a starting structure.

```
Excalidraw Community Wiki
│
├── 00 Housekeeping
│   ├── Contribution Guidelines.md
│   ├── Code of Conduct.md
│   ├── How to Get Started.md
│   └── FAQ.md
│
├── 01 Getting Started
│   ├── Introduction to Excalidraw.md
│   ├── Installation Guide.md
│   └── Basic Tutorial.md
│
├── 02 Basic Usage
│   ├── Drawing Tools.md
│   ├── Shortcuts and Tips.md
│   └── Exporting Files.md
│
├── 03 Advanced Usage
│   ├── Image References.md
│   ├── Image Cropping.md
│   └── Back-of-the-note.md
│
├── 04 Script Library
│   ├── Getting Started With Scripts.md
│   ├── Script Group 1.md
│   ├── Script Group 2.md
│   ├── Script Group 3.md
│   ├── Making Your Own Script.md
│   └── Publishing Your Script.md
│
├── 05 Examples and Templates
│   ├── Mind Maps.md
│   ├── Flowcharts.md
│   ├── Wireframes.md
│   └── Lesson Plans.md
│
├── 06 Troubleshooting
│
└── 07 Developer Docs
    ├── API Documentation.md
    ├── Scripting and Integrations.md    
    ├── Contributing Code.md
    ├── Plugin Development.md
    ├── Version History.md
    ├── Architecture Overview.md
    └── Roadmap.md
```

## The Engine Room and the Resources folders
The `Engine Room` folder contains all files that are not intended for publication. This includes templates and attachments, such as icons and images, used in Excalidraw illustrations within the Wiki. When using Obsidian Publish, only the Excalidraw files and their corresponding .svg files should be published; the contents of the Engine Room folder should remain unpublished. 

If you include illustrations, such as screenshots, that are not part of an Excalidraw .svg, those files should be placed in the `Resources` folder.