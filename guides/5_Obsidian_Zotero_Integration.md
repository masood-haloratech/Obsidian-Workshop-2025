# Obsidian-Zotero Integration on Windows

This guide shows you how to connect Zotero and Obsidian, allowing you to seamlessly reference your research library within your notes.

## Integration Workflow Overview
![Workflow](./assets/drawing-20250820153930.excalidraw.svg)

The integration works through these key components:
- **Zotero with Better BibTeX plugin:** Exports your library to a JSON file whenever changes are made
- **Shared JSON file:** Acts as the bridge between both applications, storing all your reference data
- **Obsidian with Zotero Integration plugin:** Reads the JSON file to access your references within your notes

This setup allows you to maintain your research library in Zotero while seamlessly citing and referencing sources in your Obsidian notes.

## Prerequisites

Before starting, ensure you have both Zotero and Obsidian installed on your system.

## Step 1: Create Integration Folder

Create a dedicated folder to store the integration files:
- Create a new folder named `Integration`
- **Recommended location:** Place it near your Obsidian vault or Zotero folder for easy access
- This folder will contain the shared reference file between both applications

## Step 2: Install Better BibTeX Plugin for Zotero

### Download the Plugin

1. **Visit the official plugin page**
   - Go to [https://retorque.re/zotero-better-bibtex/installation/](https://retorque.re/zotero-better-bibtex/installation/index.html)

   ![Obsidian-zotero Integration Screen 01](./assets/Integration_Zotero_BetterBibText_Site.png)

2. **Download the plugin file**
   - Scroll to the bottom of the GitHub page
   - Download the `.xpi` plugin file

   ![Obsidian-zotero Integration Screen 02](./assets/Integration_Download_Zotero_BetterBibText_XPI.png)

### Install the Plugin in Zotero

3. **Open Plugin Manager**
   - In Zotero, navigate to `Tools > Plugins`

   ![Obsidian-zotero Integration Screen 03](./assets/Integration_Zotero_Plugins_Menu.png)

4. **Install from file**
   - Click the settings cog icon on the right
   - Choose `Install Plugin From File`
   - Select the downloaded `.xpi` file

   ![Obsidian-zotero Integration Screen 04](./assets/Integration_Install_Plugin_From_File.png)

5. **Enable the plugin**
   - Ensure the Better BibTeX plugin is enabled
   - Close the Plugin Manager

   ![Obsidian-zotero Integration Screen 05](./assets/Integration_Enable_BetterBibText_Plugin.png)

## Step 3: Configure Citation Keys

1. **Access Better BibTeX settings**
   - Navigate to `Edit > Settings` 
   - Find the Better BibTeX tab

2. **Review Citation Key format**
   - The Citation Key format defines the components of the unique key generated for each reference and gets carried across from Zotero into Obsidian
   - **Recommendation:** Keep the default format unless you have specific requirements
   - Other default settings work well for most users

   ![Obsidian-zotero Integration Screen 10](./assets/Integration_Configure_Citation_Key.png)

## Step 4: Export Zotero Library

This step creates the bridge file that connects Zotero to Obsidian.

> **Note:** This export only needs to be done once. Zotero will automatically update the file whenever you add or modify references.

1. **Start the export**
   - Right-click on `My Library` in Zotero
   - Select `Export Library...`

   ![Obsidian-zotero Integration Screen 11](./assets/Integration_Initial_Library_Export.png)

2. **Choose export location**
   - Navigate to the `Integration` folder you created earlier

   ![Obsidian-zotero Integration Screen 12](./assets/Integration_Select_Export_File_Location.png)

3. **Configure export settings**
   - **Format:** Select `Better BibTeX JSON`
   - **✓ Keep updated:** This ensures the file stays synchronized with your Zotero library
   - Click `OK` to complete the export

   ![Obsidian-zotero Integration Screen 13](./assets/Integration_Export_As_BetterBibTex_JSON.png.png)


## Step 5: Install Zotero Integration Plugin for Obsidian

### Enable Community Plugins in Obsidian

The following steps are performed in Obsidian.

1. **Access Obsidian settings**
   - Ensure Community Plugins are enabled in your Obsidian settings

   ![Obsidian-zotero Integration Screen 06](./assets/Integration_Enable_Community_Plugins.png)

### Install the Plugin

2. **Browse community plugins**
   - Navigate to `Community Plugins`
   - Click `Browse`

   ![Obsidian-zotero Integration Screen 07](./assets/Integration_Browse_Community_Plugins.png)

3. **Find Zotero Integration**
   - Search for `Zotero Integration` plugin

   ![Obsidian-zotero Integration Screen 08](./assets/Integration_Find_Zotero_Integration_Plugin.png)

4. **Install the plugin**
   - Click `Install` to add the plugin to Obsidian

   ![Obsidian-zotero Integration Screen 09](./assets/Integration_Install_Zotero_Integration_Plugin.png)

   - Next enable the Zotero Integration plugin

   ![Enable Zotero integration plugin](./assets/Integration_Enable_Zotero_Integration_Plugin.png)


## Step 6: Configure the Zotero Integration Plugin

### Create Supporting Structure

The Zotero integration plugin relies on templates to format imported literature notes, so we need to set up a template for this purpose:

1. **Create a literature note template**
   - Add a `New Literature Note` template to your `Templates` folder
   - Start with a blank template with only `{{title}}` (we'll enhance it later)

2. **Create a literature notes folder**
   - Create a folder called `Literature` to store all imported articles

   ![New Literature Note template](./assets/Integration_New_Literature_Note_Template.png)

### Configure Import Settings

1. **Access plugin settings**
   - Navigate to Zotero Integration plugin settings in Obsidian

2. **Add an import format**
   - Click "Add Import Format"

   ![Add Import Format](./assets/Integration_Add_Import_Format.png)

3. **Configure the import format**
   - **Name:** `Import Literature Note`
   - **Output Path:** `Literature/{{citekey}}.md` (sends all imports to Literature folder)
   - **Image Output Path:** `Attachments` (keeps images organized)
   - **Image Base Name:** `Image-zotero-{{citekey}}` (adds prefixes to imported images)
   - **Template File:** `Templates/New Literature Note.md` (the minimal template we created)
   - **Bibliography Style:** Choose your preferred citation style

   ![Fill out Import Format](./assets/Integration_Fill_Import_Format.png)

## Step 7: Test Your First Import

### Import a Literature Note

**Important:** Zotero MUST be running in the background for this to work!

1. **Start the import process**
   - Open Command Palette (`Ctrl+Shift+P` or `Cmd+Shift+P`)
   - Select `Zotero Integration: Import Literature note`

   ![First Literature Note Import](./assets/Integration_Invoke_Import_Literature_Note.png)

2. **Select your reference**
   - The reference selector will appear (sometimes it gets hidden behind other windows)
   - Type the title or author's name of the article you want to import
   - Select it and hit Enter

   ![Select article from reference picker](./assets/Integration_Select_Zotero_Reference.png)

3. **View the imported note**
   - The reference is now imported to your `Literature` folder
   - Currently, you'll only see the title since our template is basic

   ![View of the imported reference](./assets/Integration_View_Initial_Reference_Import.png)

## Step 8: Enhance Your Literature Template

### Discover Available Fields

To see what data you can import from Zotero:

1. **Open the Data Explorer**
   - Use Command Palette: `Zotero Integration: Data Explorer`

   ![Open Zotero Integration Data Explorer](./assets/Integration_Find_Zotero_Integration_Data_Explorer.png)

2. **Explore your reference**
   - Click `Prompt For Selection`
   - Find and select your article

   ![Select article for Data Explorer](./assets/Integration_View_Article_Data_Explorer.png)

   - The Data Explorer shows all available fields. This is how the `{{title}}` entry in the template is getting populated.

   ![Select article for Data Explorer](./assets/Integration_Test_Fields_New_Literature_Note_Template.png)

### Update Your Template

Add fields to your `New Literature Note` template. Here's a basic structure to start with:

```markdown
**Authors**:: {{authors}}
**Title**:: {{title}}  
**Year**:: {{date | format("YYYY")}}  
  
## Abstract
{{abstractNote}}
```

![Updated New Literature Note Template](./assets/Integration_Update_New_Literature_Note_Template.png)

### Test the Enhanced Template

Re-import the same article to see the populated fields:

![Updated view of imported article](./assets/Integration_Updated_Article_View.png)

## Step 9: Advanced Template Features

### Import Annotations and Images

You can create templates that import:
- Zotero annotations and highlights
- Screenshots and images
- Personal notes and comments

The template uses [Nunjucks](https://mozilla.github.io/nunjucks/templating.html) templating language for control logic.

**Full template example:** See [New Literature Note](../templates/New%20Literature%20Note.md) template for advanced features.

### Working with Annotations

1. **Create annotations in Zotero**
   - Add highlights, notes, and screenshots to your PDF

   ![Annotations in Zotero](./assets/Integration_Zotero_Annotations.png)

2. **Re-import to see changes**
   - Import the article again to pull in your annotations

   ![Updated Article View](./assets/Integration_Refined_Article_View.png)

