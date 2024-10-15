---
aliases:
  - wiki/troubleshooting
---
# Troubleshooting Excalidraw Performance Issues

While I continuously work on optimizing Excalidraw with regular updates and improvements, I recognize that the plugin can be resource-intensive. If you notice that Excalidraw is affecting Obsidian's performance or experiencing lag, here are some steps you can take to improve the situation:

## Test in an Empty Vault with Only Excalidraw Installed

In most cases, performance issues stem from compatibility problems with other plugins, themes, or CSS snippets. One of Obsidian.md's greatest strengths is its extensive customization options through plugins and themes. However, this flexibility can sometimes come at a cost. Many plugins are created by enthusiastic developers, myself included, who may not have the resources or time to fine-tune their code. Additionally, Obsidian's cross-platform nature and its constant evolution make it challenging to perform robust integration tests across all possible configurations.

Personally, I use very few plugins, minimal CSS, and the Gruvbox theme. As a heavy Excalidraw user, I can attest that it runs smoothly on all my devices, including an older iPad I use for testing. By choice, I do not address compatibility issues with other plugins because it's nearly impossible to cover all cases. However, you can troubleshoot these issues on your end.

### Test in an Empty Vault

1. Create a new, empty Vault in Obsidian.
2. Install only Excalidraw—no other plugins, themes, or snippets.
3. Test if the performance issue persists.

- **If the issue is resolved:** Return to your main Vault and start eliminating potential conflicts. Revert to the default Obsidian theme, disable CSS snippets, and turn off other plugins. Restart Obsidian, then re-enable plugins and themes one by one, checking performance each time. When you identify the culprit, you can either raise the issue with the relevant plugin developer or decide which plugin is more essential for your workflow—Excalidraw or the conflicting one.
  - **Common culprits:** The Metadata Menu plugin, Templater's "Syntax highlighting on desktop" feature, Minimal Theme, and a few other themes.

## Adjust Autosave Settings
![[Picture - Excalidraw Autosave settings.png]]

You can improve performance by reducing the frequency of autosaves. Setting autosave to every 15 minutes is usually safe on a PC, as Excalidraw also saves automatically when you switch tabs or navigate within Obsidian. Just avoid closing Obsidian abruptly. As a best practice, press `CTRL+S` (this is CTRL on Mac too, not CMD) before quitting Obsidian.

On mobile devices, the situation is different. When switching apps, Android and iOS might recycle Obsidian in the background. If you've set autosave to "rare" or "practically never," make sure to save manually. You can do this using the save option in Excalidraw’s Obsidian Toolbar or by enabling "Show tab title bar" in Obsidian's Appearance settings.

Less frequent autosave will also reduce the memory consumption in your Obsidian Sync account.

## Use Compressed JSON

Excalidraw compresses drawing data by default within the markdown file. While this compression is resource-intensive — contributing to the performance impact of autosave — it offers several benefits. Compression keeps file sizes manageable, which in turn improves Obsidian's indexing performance and prevents Excalidraw JSON data from cluttering your search results.

If you need to manually edit the Excalidraw JSON file, you can easily decompress it using the Command Palette: "Excalidraw: Decompress current Excalidraw file" when in Markdown view mode.

I set compression as the default after Obsidian 1.6.0 introduced a limitation on indexing files larger than 2MB, which affected Excalidraw files. Although this limitation was removed in Obsidian 1.6.3, compression still offers clear advantages by reducing file size — especially for users who take handwritten notes, where file sizes can drop from 10+MB to around 1MB.

While I don’t recommend turning off compression due to its benefits, you can change this setting in the Plugin settings under "Saving" if needed.

## Excalidraw is a Desktop Illustration Tool

Excalidraw is primarily designed as a desktop illustration tool. While it can handle handwritten notes, it's not optimized for extensive handwritten note-taking. As such, some performance limitations may remain unaddressed. However, you can experiment with custom pens in Excalidraw. I recommend trying the "Finetip pen" for handwriting, which offers a smoother experience than the default pen.

![[Picture - Excalidraw Settings custom pens.png]]

Additionally, I suggest exploring handwriting recognition tools. I've had good experiences with Apple Scribble and a similar feature on my Samsung S23 Ultra. Besides improving performance, handwriting recognition makes text in your drawings searchable. You might also want to try the "Scribble Helper" script available in the Excalidraw script store for enhanced handwriting support.

![Scribble Helper Video](https://youtu.be/BvYkOaly-QM)
