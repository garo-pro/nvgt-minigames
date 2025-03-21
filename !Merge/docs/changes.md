# New in 0.6, build 3:
As of this version - build 3 - releases are being kept in a progress bar format (y.xx), where y is the main version and xx is the progress to the next version. This allows us to show when we think changes are large enough for an entire version upgrade and does not limit us with just 100 possible progress versions, while still allowing to see the estimated progress for everyone. Thus, the progress for version 1 is currently 60 percent. Builds are still being kept. The changelog is marc down formated now, since the file ending always has been .md
In this update, several new mini games have been added with their corresponding documentation:
The whole repository has been given a massive overhaul! IN short, migrations to NVGT 0.89.1 have been completed, many of the scripts and documentation have been changed, and there is now a better building system.
The launcher - now the entry point of the application - has been rewritten nearly entirely. Now, basically the entire mini games have been bundled into one big program, in such a way that updating and adding new minigames is easier than ever. This also means we no longer need to fight around with 1000 conflicting includes for each minigame which just needs additional space. From now on, we just can hit one button to generate a Windows package instead of needing to write our own scripts or manually insert everything correctly. Unfortunately this means that the well-served include written by contributor Harry is no longer required, but thanks for creating it!
The menu class now has been replaced through a form based self-made bunch of functions. Due this, the API for developers has changed noticeable.
The entire code should now be indented properly.
Due an internal backend change, an internet connection is now required for pack updates.
Changes to the following minigames have been made:
Guess the number: Using more up to date form metods and changed internal components. Should not affect gameplay. Spelling errors also have been fixed.

Notice: All changelog entries from build 1 and 2 are rather ruck, and just have been kept for archivating purposes. Additionally, the entries are incomplete since they mainly just have been written by Garo from Git commit logs.

# New in build 2:
Fixed the launcher, thanks Jonathans859!
A few changes to the launcher: Debugging is now false by default. The debug menu close button can now be access with alt + c. Now, if you press escape in the debug viewer menu, it will return back to the main menu. Instead of first adding the programs and then the debug log, it does it changed by order.
Fixed typo in the readme.
NVGT in the readme updated from version 0.86.0 to 0.87.2. You can expect a new windows release in the next week.
The launcher has been documented in the readme.md file and will soon be documented as documentation within the documentation viewer.
Once again the todo has been emptied.

# New in build 1:
The readme has been updated. Aria2c was, and probably won't be, needed.
Finally! We have a launcher. Currently it is broken though.
The documentation viewer no longer imports speech.nvgt doubled.
Two developers added in the readme.
Guess the number game has been moved into an extra folder.
Documentation for number sort has been added.
Guess the number now uses form dialogs.
Documentation updated. Index updated to let it look not that ugly at start, and a documentation documentation added.
When the button d12 which closes the document reader is pressed after a document has been read, which is forcefully the case when an user wants to exit the documentation viewer, the form now resets before exiting. This don'T really needs to be done, but still.
A new todo (todo.md) has been added.
Readme updated so the version of nvgt is actually 0.86.0 instead of 0.86.1
Fixed two typos in the changelog.
The documentation of blackjack has been converted to plaintext and put into the documentation folder.
Fixed some spelling error at the readme.md
Documentation script has been updated.
Changes created.