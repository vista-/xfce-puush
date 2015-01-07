# xfce-puush
A puush client utilizing xfce's xfce4-screenshooter application.

See [sunmockyang's repo](<https://github.com/sunmockyang/puush-linux) for directions. 
# How does it differ from the original script?
The script has been rewritten to use xfce4-screenshooter instead of gnome-screenshot, which is not compatible with XFCE. Because of the lack of a "save as filename" switch, a workaround is used to save the file without opening the "Save As" dialog window - the -o switch is used to "open" the picture in another application (in this case, "true", which returns true), the file is saved with the default name (Screenshot - date - time.png) in the /tmp/ directory.

Another hack-ish attribute of the script is that it puush-es the most recently modified file in /tmp/ (which is hopefully your screenshot - those with applications that write into /tmp/ quite frequently, be wary of possible mis-puushes!) - those who wish to make sure that the file about to be puush'd is the correct file can try with some regex magic (if you do do this, please send a pull request, I'd be more than happy to include your change)!
