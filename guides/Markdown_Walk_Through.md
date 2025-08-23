# Creating Notes with Markdown in Obsidian

This section covers the basics of creating and formatting notes using Markdown syntax.

## Starting Fresh

First, let's clean up the workspace:
1. **Delete the default Welcome note**
   - Right-click on the "Welcome" note
   - Choose **"Delete"** from the context menu
2. You now have a completely blank canvas to work with

## Creating New Notes

There are several ways to create a new note in Obsidian:

- **Toolbar:** Click the **"New note"** icon
- **Tab strip:** Click the **"+"** button and select **"Create new note"**
- **Command Palette:** Open with `Ctrl+Shift+P` (Windows) or `Cmd+Shift+P` (Mac), then find **"Create new note"**
- **Keyboard shortcut:** `Ctrl+N` (Windows) or `Cmd+N` (Mac)

## Understanding Note Names

When you create a new note, it's called "Untitled" by default. This filename appears in four places:

![Obsidian Notes Screen 00](./assets/Obsidian_Notes_00.png)

**Important:** If you change the text in any of these locations, the filename changes automatically.

### File Naming Best Practices
- Use typical file naming conventions
- Avoid special characters like quotes, slashes, or colons
- Keep names descriptive but concise

**For this workshop:** Let's name our first note **"Testing Markdown"**

## Basic Markdown Formatting

Now let's explore essential Markdown syntax:

### Headers
- `#` = Main heading (H1)
- `##` = Subheading (H2)  
- `###` = Sub-subheading (H3)
- Continue adding `#` symbols for deeper levels

### Text Formatting
- `**bold text**` = **bold text**
- `*italic text*` = *italic text*
- `***bold and italic***` = ***bold and italic***

### Useful Features
- **Code blocks:** Use three backticks ``` for code
- **Lists:** Use `-` or `*` for bullet points, numbers for ordered lists
- **Callouts:** Special boxes for highlighting information

### Learning Resources
- [**Markdown Cheat Sheet**](https://www.markdownguide.org/cheat-sheet/) - Complete reference
- [**Obsidian Callouts Guide**](https://help.obsidian.md/callouts) - Advanced callout formatting

## Viewing Your Work

Let's see how our note looks in both modes:

**Source Mode** (raw Markdown):

![Obsidian Notes Screen 01](./assets/Obsidian_Notes_01.png)

**Reading Mode**:

![Obsidian Notes Screen 02](./assets/Obsidian_Notes_02.png)

> **Workshop Tip:** Toggle between these views frequently to see how your formatting appears.

## Working with Attachments

### Adding Images

**Drag and Drop**
1. Switch to **Source mode**
2. Drag an image file into your note
3. Obsidian automatically:
   - Copies the image next to your note
   - Creates a link using `![[filename]]` syntax

![Obsidian Notes Screen 03](./assets/Obsidian_Notes_03.png)

**In Reading Mode, the image renders:**

![Obsidian Notes Screen 04](./assets/Obsidian_Notes_04.png)

### Understanding Link Syntax

- `![[filename]]` = **Embedded content** (images, PDFs show inline)
- `[[filename]]` = **Regular link** (clickable text only)

**Example of regular link** (without the `!`):

![Obsidian Notes Screen 05](./assets/Obsidian_Notes_05.png)

### Embedding YouTube Videos

Try this: Copy and paste this code into your note in Source mode:
> **Tip:** Remeber to delete any `code block` syntax after you paste the link 

```markdown
![Intro to neural networks from Andrej Karpathy](https://www.youtube.com/watch?v=VMj-3S1tku0)
```

Toggle to Reading view to see the embedded video player.

## Organizing Your Vault

### Creating Folder Structure

As your vault grows, organization becomes important. Let's create an **"Attachments"** folder:

- **Toolbar:** Click **"New folder"** icon
- Simply **drag and drop** the image file into the folder

![Obsidian Notes Screen 06](./assets/Obsidian_Notes_06.png)

**Important:** Notice that even after moving the image, the link in your note still works! Obsidian automatically updates internal links.

## Setting Default Attachment Behavior

Instead of manually organizing attachments each time, let's automate this:

### Configure Attachment Settings

1. Go to **Settings** ⚙️
2. Navigate to **"Files and links"**
3. Find **"Default location for new attachments"**
4. Select **"In the folder specified below"**
5. Set **"Attachment folder path"** to: `Attachments`

![Obsidian Notes Screen 07](./assets/Obsidian_Notes_07.png)

## Testing the New Setup

Let's verify our settings work with a PDF:

### Adding a PDF File

1. **Switch to Source mode**
2. **Drag and drop** a PDF file onto your note
3. **Observe:** 
   - File automatically goes to the Attachments folder
   - Link appears as `![[filename.pdf]]`

![Obsidian Notes Screen 08](./assets/Obsidian_Notes_08.png)

### Viewing the PDF

Switch to **Reading mode** to see the PDF rendered inline:

![Obsidian Notes Screen 09](./assets/Obsidian_Notes_09.png)

## What's Next

You now have the fundamentals for creating rich, well-organized notes in Obsidian. In the next section, we'll explore linking between notes to create a knowledge network.