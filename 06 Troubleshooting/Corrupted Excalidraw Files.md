# Corrupted Excalidraw Files

## Most Frequent Causes of Excalidraw File Corruption

If files become corrupted, turning off other plugins will not resolve the issue. Once a file is corrupted, it will remain corrupted even if the original cause is resolved. The most common causes for file corruption are:

1. **Plugins Writing Files in the Background**  
   Plugins that automatically modify files (e.g., adding timestamps, linting) can disrupt Excalidraw’s save logic.  
   Check out my list of [[Compatibility Issues - Plugins to Watch Out For]]. While this list is not comprehensive (there are over 2,000 plugins in Obsidian), it highlights common conflicts. As a best practice, I recommend limiting the number of plugins you use. Many plugins are created by hobby developers and may not be tested for compatibility with others. Using fewer plugins reduces the risk of conflicts, especially with complex plugins like Excalidraw.

2. **Unexpected Termination of Obsidian**  
   Force-closing Obsidian—such as swiping it away on a tablet or phone—interrupts the save process and may cause file corruption.

3. **Sync Service Interruptions**  
   Sync services, including Obsidian Sync, can occasionally disrupt file integrity. This happens when Sync tries to merge two versions of the same file corrupting the Excalidraw Data section in the process. However, with a little attention—such as ensuring files are saved and closed before switching devices—these issues can typically be avoided.

## Tips for Stability

For most users, file corruption should be a rare occurrence. I have nearly 4,000 drawings and encounter a corrupted file only occasionally, often due to sync conflicts. If corruption happens frequently for you, one of the causes listed above is likely responsible. Taking steps to manage plugins and sync behavior should minimize these problems.

### Use Sync or Backup Services  
Services like Obsidian Sync, Google Drive, Dropbox, OneDrive, and iCloud often provide version history for files. If a file becomes corrupted, you can right-click on the file in your cloud storage and restore a previous version. I highly recommend using a sync or backup service—not just for occasional Excalidraw file issues, but as protection against hard drive failures, ransomware attacks, and other potential data loss.

## Avoid Compatibility Mode

I strongly advise against using **Legacy Compatibility Mode** in Excalidraw. This feature has not been updated or reviewed in over two years, and I cannot guarantee what side effects it might introduce. Unless you have a very specific use case, such as managing your Obsidian Vault alongside a Visual Studio Code project with illustrations, it’s best to avoid enabling compatibility mode.