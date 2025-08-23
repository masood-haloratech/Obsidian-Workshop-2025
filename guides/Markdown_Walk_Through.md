- Let's start by deleteing the default `Welcome` note by right clicking and choosing `Delete` from the context menu.
- Now we have a completly blank canvas to start with.
- Lets create a new note. 
- There is a couple of ways to create new notes. 
  - You hit the new notes icon on the tool bar
  - Click the + on the tab strip and click `Create new note`
  - Open the command pallet, find and click `Create new note`
  - Or go with the keyboard short cut Ctrl + N on windows

- When a new note is created by default it is called Untitled. This is literally the file name and is reflected in four places on the screen.

![Obsidian Notes Screen 00](./assets/Obsidian_Notes_00.png)
  
- If you change the text in any of these places the file name changes.
- Stick to typical file naming conventions and avoid characters such as quotes and special characters.
- We'll call this first note "Testing Markdown" and go through a few basic `Markdown` commands.
- To create a heading we use the `#` symbol. Two hashes is a subheading three is a sub-subheading etc.
- Next lets add the date 
- Add some text. Putting double astrix `**` around a word makes it bold. Single astrix makes it italic.
- Handy features include code block, lists, call outs
- Here is a handy  [**Markdown** cheat sheet](https://www.markdownguide.org/cheat-sheet/)
- More information on [**Callouts** here](https://help.obsidian.md/callouts)

- In source mode

![Obsidian Notes Screen 01](./assets/Obsidian_Notes_01.png)

- In read only mode

![Obsidian Notes Screen 02](./assets/Obsidian_Notes_02.png)

- Now we can embed pictures and other documents into the note.
- You can drag and drop the file in the source mode and it will copy the image next to your note and then it will create a link inside your note to the image.
- Links are created using `[[]]` double square brackets.
- Putting an `!` mark at the start of the double square brackets tells obsidian to render the link. 

![alt text](./assets/Obsidian_Notes_03.png)

- If you are now enter reading view you can see the rendered image.

![alt text](./assets/Obsidian_Notes_04.png)

- If you remove the leading `!` mark it will render as a normal link

![alt text](./assets/Obsidian_Notes_05.png)

- Now we can also do this with links to Youtube videos.
- Try cutting and pasting the following link into your note.
- Now toggle between the `Reading view` and `Source mode` to see the view rendered.

```Markdown
![Intro to neural networks from Andrej Karpathy](https://www.youtube.com/watch?v=VMj-3S1tku0)
```

- Obsidian is unopinionated about how you structure your notes and attachements into folders. But it is always nice to put some structure around your vault just to remove the clutter. As your vault grows you will end up with lots of attachments that you may not always want to see.
- So we are going to create a folder called `Attachments`
- You can do this by clicking on the `New Folder` icon on the tool bar or through the right click context menu or from the command pallet.

![alt text](./assets/Obsidian_Notes_06.png)

- Now lets move our image into the `Attachments` directory by simply draging it in. (You can also do this through the command pallet)

- Click back on your note and notice that even if we moved the image the link to the image still works.

- No we don't want to do this everytime we want to attach a file to our note.
- Lets change the default behavior so that all new attachments end up in the attachments folder.
- Navigate to `Settings > Files and links` find `Default location for new attachments` and set it to `In the folder specified below` then set the `Attachment folder path` to `Attachments`

![alt text](./assets/Obsidian_Notes_07.png)

- Lets try attaching another file but this time with a `PDF`.
- Enter the `Source mode` then drag and drop it on to our note. 
- Notice that the file now ends up in the right folder and we have a link in our note with `![[ ]]`

![alt text](./assets/Obsidian_Notes_08.png)

- When you enter `Reading view` the `PDF` file is rendered.

![alt text](./assets/Obsidian_Notes_09.png)


