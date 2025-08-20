# Obsidian Zotero Integration on Windows

![Workflow](drawing-20250820153930.excalidraw.svg)

- First thing we want to do is create a folder to store our integration file `\Integration`. Recommend keeping it close to your obsidian vault or zotero folder.

### Install Zotero Plugin - Better BibTex for Zotero

- Navigate and download the Better BibTex for Zotero plugin from the official website https://retorque.re/zotero-better-bibtex/installation/index.html.

![Obsidian-zotero Integration Screen 01](./Integration_01.png)

- The plugin file (.xpi) file is located at the bottom of the github page.

![Obsidian-zotero Integration Screen 02](./Integration_02.png)

- Back in Zotero navigate to `Tools > Plugins` to open the Plugin Manager

![Obsidian-zotero Integration Screen 03](./Integration_03.png)

- From the right hand side click the settings cog and choose `Install Plugin From File`

![Obsidian-zotero Integration Screen 04](./Integration_04.png)

- Once the plugin is installed ensure it is enabled then close the Plugin Manager screen.

![Obsidian-zotero Integration Screen 05](./Integration_05.png)

### Configure Citation Key
- Navigate to `Edit > Settings` and locate the Better BibTex tab
- You can modify the Citation Key format from here which will be used as your primary key to link between Zotero and Obsidian. Recommend leaving it as is.
- No need to change any other settings unless you are having issues. The default values work pretty well.

![Obsidian-zotero Integration Screen 10](./Integration_06.png)

### Initial Export
- An initial export of the BibTex file is required. 
- You only need to do this step once, after that, Zotero will keep the reference file and keep it up to date with any additions or changes you make.
- Right click on the `My Libraray` node
- Pick `Export Library...`

![Obsidian-zotero Integration Screen 11](./Integration_07.png)

- Locate the integration folder set up at the begining of this guide.

![Obsidian-zotero Integration Screen 12](./Integration_08.png)

- Pick the format as `BetterBibTeX JSON`
- Tick `Keep updated` checkbox
- Click `OK`

![Obsidian-zotero Integration Screen 13](./Integration_09.png)

### Install Obsidian Plugin - Zotero Integration
- Navigate to settings and first ensure that community plugins are turned on 

![Obsidian-zotero Integration Screen 06](./Integration_10.png)

- Next navigate to `Community plugins` and click `Browse`

![Obsidian-zotero Integration Screen 07](./Integration_11.png)

- Locate the `Zotero Integration` plugin

![Obsidian-zotero Integration Screen 08](./Integration_12.png)

- Click `Install` to install the plugin

![Obsidian-zotero Integration Screen 09](./Integration_13.png)


