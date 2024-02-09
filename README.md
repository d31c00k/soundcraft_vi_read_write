# So you want to make one of your Soundcraft Vi Show Files read only? You have about 3 different options.

- Option 1: Copy the show file to a USB drive, open it on a Windows computer and set the directory to be read only, and then copy the show file back onto the console.

- Option 2: Copy the show file to a USB drive, open the Windows backend (more on that later) and set the directory to be read only, and then copy the show file back onto the console.

# But what if you dont want to mess with the USB and copy files back and forth?

## Option 3: Use the batch scripts in this repository to automate the process on the console itself.

# How To:

- Select and download the batch scripts that matches your console to a USB drive.

- Upon booting your console, connect a mouse and keyboard via USB.
- Type 'showcursor' and hit Enter. A mouse cursor will appear on top of the Soundcraft GUI. This will make things easier going forward.
- Now type CTRL+SHIFT+ESC to bring up Task Manager. Type ALT+F+N to bring up the RUN command. 
- Type explorer. This will start Windows' GUI.
- Mouse down to the bottom right hand corner of the main screen and the Windows taskbar should appear. 
- From here you can click the right corner of the taskbar to show the Windows desktop instead of the Soundcraft GUI.
- Clicking the File Explorer icon on the taskbar will allow you to navigate to the show files you want to make read only.
- Show file directories can be found in F:/Data/Shows
- Place both scripts INSIDE the directory of your showfile. IT IS IMPORTANT THAT YOU ONLY PUT THEM INSIDE THE SHOWFILE YOU WANT TO AFFECT!
- Clicking on the batch script "!_READONLY_Vixxx.bat" will set the show file to Read Only Mode.
- Clicking on the batch script "!_WRITABLE_Vixxx.bat" will make the show file writable and allow you to save changes. Use this when you want to edit your default file.

# How does this work?
- Soundcraft Vi consoles show files are saved as directories.
- When copied from a console to a USB drive, only certain file in the show file directory are actually copied.
- These files can be set to "Read Only" mode.
- However, there are other files in the show file directory that CANNOT and SHOULD NOT be set to read only and do not travel with the directory when it is copied to a USB.
- I discovered this the hard way when I first made these scripts. I set those other files to read only and suddenly had a growing list of Error in the Error log of the console.
- So only set the files listed in the batch scripts to read only.
