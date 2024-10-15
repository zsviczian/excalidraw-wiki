---
aliases:
  - wiki/images
---
[[#Block Reference Images]]
[[#Image Fragments]]

# Type of references
- Area reference: `![[drawing#^area=<<element_id>>]]`
- Group reference: `![[drawing#^group=<<element_id>>]]`
- Frame reference: `![[drawing#^frame=<<element_id|frame_name>>]]`
- Clipped frame: `![[drawing#^clippedframe=<<element_id|frame_name>>]]`

# Block Reference Images

![Block reference parts of images just like text with Obsidian Excalidraw](https://youtu.be/yZQoJg2RCKI)

## Summary
In this video, I introduce the image referencing feature in the Obsidian Excalidraw Plugin, which allows you to reference and embed specific sections of images into your markdown documents. I demonstrate how to highlight parts of an image, assign reference IDs, and embed only those sections. When clicked, these references take you back to the original image, showing the specific part in context.

I cover various embedding options, including text, area, and group references, and explain how to create and use these in your documents. I also discuss the differences between embedding SVG and PNG files, along with potential issues when referencing non-text elements.

Finally, I share three techniques I used while working with a painting by Pieter Bruegel, focusing on resizing the image, locking it to prevent movement, and making text elements transparent. These tips can help enhance your visual linking between images and notes.

## Timestamps
- [00:00](https://www.youtube.com/watch?v=yZQoJg2RCKI&t=0s) Intro
- [01:18](https://www.youtube.com/watch?v=yZQoJg2RCKI&t=78s) Overview of image referencing options
- [02:49](https://www.youtube.com/watch?v=yZQoJg2RCKI&t=169s) Zettelkasten example
- [05:18](https://www.youtube.com/watch?v=yZQoJg2RCKI&t=318s) Reference types and the copy markdown link function
- [10:33](https://www.youtube.com/watch?v=yZQoJg2RCKI&t=633s) SVG vs. PNG
- [11:42](https://www.youtube.com/watch?v=yZQoJg2RCKI&t=702s) Block referencing non-text elements
- [13:04](https://www.youtube.com/watch?v=yZQoJg2RCKI&t=784s) 3 tricks I used on the Bruegel painting
- [15:35](https://www.youtube.com/watch?v=yZQoJg2RCKI&t=935s) Closing remarks
## Video Transcript
### Intro

Imagine creating a document similar to a Wikipedia page about Pieter Bruegel's painting _Children's Games_. You might want to show the big picture and zoom into different sections. Typically, you’d paste the full image into your document, then manually crop and paste different parts for detailed views.

However, this method doesn’t link the parts to the original image. You'd need to spend time finding where those cropped sections came from.

I have a better solution. With the new version of Obsidian Excalidraw, you can highlight a part of an image, give it a reference ID, and embed just that section in your document. When clicked, it takes you back to the original image and highlights the referenced section.

Let me show you how it works.

### Overview of Image Referencing Options

We all love options, but too many can be overwhelming. Here's an overview of the ways you can embed an image in a markdown document:

1. **Text Embed**: This embeds the text content of a referenced element.
2. **Area Embed**: This embeds the text element and a surrounding area.
3. **Group Embed**: This embeds the group to which the text element belongs, but nothing else.

There are two types of references: **block references** and **section references**. Excalidraw also offers two ways to embed drawings into markdown: **SVG files** (the default) or **PNG files**. Some features, however, won’t work with PNG files.

### Zettelkasten Example

Let’s look at an example from my Zettelkasten. I have a note referencing the idea, _"Open tasks tend to occupy short-term memory"_. If I click on this reference, it takes me directly to the relevant text element in the Book-on-a-Page sketch, zooming in on the text.

Using Excalidraw’s new feature, I can add `area=` to the block reference, which will include the image area around the text. If I replace `area` with `group`, the block reference will display all elements in the same group as the text.

This gives you three display options:

1. **Group Selector**: Embeds all elements in the group.
2. **Area Selector**: Cuts out the section around the text element.
3. **Text Element**: Displays only the text element itself.

### Reference Types and the Copy Markdown Link Function

Here’s another example, where we look at an agenda in the image. The agenda is a single text element, with background coloring created using rectangles.

Let’s embed different references:

- **Text Reference**: Embeds just the agenda as bullet points.
- **Area Reference**: Embeds the text with some padding around it.
- **Group Reference**: Embeds the entire agenda, including background rectangles.

You can create these references using the Obsidian menu in Excalidraw. Clicking the _Copy Markdown Link_ button offers modifiers:

- **Control/Command-click**: Copies a group reference.
- **Shift-click**: Copies an area reference.
- **Click**: Copies a block reference.

### SVG vs. PNG

Now, let’s see what happens when switching from SVG to PNG. This can be done in the plugin settings under the embed and export section. When using PNG, area references don’t work, and instead, the entire image is transcluded. For text or group references, PNG works similarly to SVG.

### Block Referencing Non-Text Elements

Be careful when referencing non-text elements like shapes. If you copy a block reference for a rectangle, for example, Obsidian will throw an error since it can’t find the block reference. To fix this, use a group reference.

Switching between SVG and PNG changes the behavior of group and area transclusions.

### 3 Tricks I Used on the Bruegel Painting

Here are three tricks I used while working with the Bruegel painting in the intro:

1. **Change Image Dimensions**: I used the _Set Dimensions_ script to adjust the size of the image for better text label fitting.
2. **Lock the Image**: This prevents accidental movement of the image while placing sticky notes on top.
3. **Set Labels to Transparent**: When finished, I selected all labels and set their stroke color to transparent, which can be easily reversed.

### Closing Remarks

I’m excited about this new feature in Obsidian Excalidraw. I hope you find it useful and that it enhances your ability to link images to your notes. Thank you!

# Image Fragments

![Excalidraw-Obsidian 2.2.10: Image Fragments](https://youtu.be/sjZfdqpxqsg)

## Summary
In this video, I introduce Obsidian-Excalidraw Image Fragments and compare them with Image Deconstruction using a Double Bubble Map. I demonstrate how you can reference specific parts of an image using new features like frame and clipped-frame references. These allow users to insert portions of drawings into markdown documents with or without frame boundaries, making it easier to focus on specific elements.

I also showcase a bonus feature that lets users quickly copy an embed link for the entire drawing. Finally, I compare Image Fragments and Deconstruction, explaining that while both methods break down visuals, deconstruction creates reusable icons, whereas image fragments retain the context of the original image. The video concludes with a recommendation to join Cohort 10 of the Visual Thinking Workshop.

## Timestamps
- [00:00](https://www.youtube.com/watch?v=sjZfdqpxqsg&t=0s) Intro
- [00:19](https://www.youtube.com/watch?v=sjZfdqpxqsg&t=19s) Feature demonstration
- [02:54](https://www.youtube.com/watch?v=sjZfdqpxqsg&t=174s) Comparing Frame reference to Clipped-Frame reference
- [04:03](https://www.youtube.com/watch?v=sjZfdqpxqsg&t=243s) Referencing the frame title (name)
- [05:42](https://www.youtube.com/watch?v=sjZfdqpxqsg&t=342s) Bonus feature: Copy `![[embe link]` for this drawing
- [06:51](https://www.youtube.com/watch?v=sjZfdqpxqsg&t=411s) Comparing Decomposition with Image Fragments
- [11:18](https://www.youtube.com/watch?v=sjZfdqpxqsg&t=678s) Closing thoughts

## Video Transcript
### Intro
 I have a special feature to share today—one that many of you have requested numerous times. I finally decided to build it! This feature builds on block references for images, but takes it a step further. Let’s dive into the demonstration.

### Feature Demonstration

Let’s start with something that should already be familiar. Imagine I have this drawing with a group of elements. These are grouped into an Excal group. If I right-click on the group, I can select "copy link for selected elements." A dialog box pops up where I can copy a link, an area, or a group reference. You can refer to the video linked in the description for more details on the area and group references.

Now, if I copy the group reference and paste it into a Markdown document, a portion of the larger image appears. Long-clicking on this portion zooms into the original drawing, showing only the selected element. This is super useful!

The new feature allows you to do the same with Excalidraw drawings. I can paste the image section into a new location, just as before. Now, I want to show you some additional features.

### Comparing Frame Reference to Clipped-Frame Reference

Let’s take this house drawing inside a frame. If I right-click the frame and copy the link, I see two new buttons: "frame" and "clipped frame." If I copy the frame and paste it elsewhere, all elements inside the frame are included, even if some, like this cart, didn’t fully fit. This functionality was available earlier but only for Markdown documents.

Now, let’s explore the clipped-frame reference. When pasted, it inserts only what’s inside the frame’s boundaries, clipping out excess elements like the cart. You’ll also notice there’s no padding—clipped frames come without it by default.

### Referencing the Frame Title (Name)

Next, take note of the frame titles—this one is labeled "cart," and the other is "house." Each reference includes a long ID, but I can change this to reference frames by name. If I modify the reference to “house,” it will display the elements in the house frame. I can do the same for clipped frames. Additionally, you can change references directly in Markdown view by editing embedded file references.

### Bonus Feature: Copy `![[Embed Link]]` for Drawings

A small but useful bonus feature is the ability to copy an embed link for the entire drawing. If no elements are selected, I can click the background and select "copy embed link for this drawing." This allows for quick embedding into other documents. You can also set this function as a hotkey in the command palette for convenience.

### Comparing Deconstruction with Image Fragments

Now that we’ve explored the feature, let’s compare deconstruction with image fragments using a double bubble map. I’ll include a link to my video on double bubble maps in the description, but let’s dive into the similarities and differences.

Both deconstruction and image fragments allow you to break down complex visuals into more manageable components, enhancing focus on specific elements while linking and reusing them in different drawings. However, there are key differences:

- **Deconstruction** creates reusable icons for repeated use, while **image fragments** reference specific parts of a larger illustration—perfect for infographics or detailed visuals.
- **Deconstructed elements** become context-neutral, suitable for reuse across multiple contexts, whereas **image fragments** retain the context of the source image.
- **Deconstruction** is more robust, as isolated elements are stored in dedicated files, while **image fragments** are fragile—regrouping elements can break links.
- Finally, **deconstruction** allows for further breaking down elements into smaller parts, whereas **image fragments** reference whole sections without further decomposition.

### Closing Thoughts

That’s all I wanted to share today. If you're interested in learning more about my visual thinking workflows, Excalidraw, and becoming a power user of visual thinking in Obsidian, check out Cohort 10 of the Visual Thinking Workshop, starting at the end of August. Thank you!