# NVGT mini games
Greetings and welcome to NVGT mini games, an evergrowing amount of mini games such as hangman or a simple guess the number game. It aims to provide fun and a good resource for [nvgt](https://github.com/samtupy/nvgt) learners.

Please note: While this is a quite well maintained and structured code base, this by no means is supposed to be a template to code after. Some of the requirements are straight over converted from bgt, and thus are not really optimized. Therefore you surely can take this repository to learn NVGT, however if you see a function or class that looks suspicious you rather should research on your own on how to implement it the best rather than taking a solution which may not works as expected or just in a limited way.

You can read the changes [here](docs/changelog.md) and download the releases [here](https://github.com/garo-pro/nvgt-minigames/releases/).

## Building
### Downloading NVGT
To be able to build the games, you must download NVGT. To download, click [this link](https://nvgt.gg/downloads/). Be sure to download the latest version, which at the time of this writing is version 0.89.1.
Please note that if the script does not compile and gives compilation errors, rather than submitting an issue you should test first wether you also cannot compile with the newest NVGT custom build. IN order to optain such a build, fork your own copy of the [NVGT repository](https://github.com/samtupy/nvgt) to your GitHub account. Then, run the release action and wait aproxemately 10 minutes, before downloading the Windows release. There are two Windows related files, so make sure you get the right one where in unzipping it says NVGT0.xx.x.exe or similar. Install NVGT and test again.
After you'Ve downloaded NVGT, you can compile the script. Follow this guide:
- Go to the context menu when you'Ve selected the main script.
- Press right arrow or enter on the compile submenu.
- Press w to go to the Windows option, and press enter or w, depending wether you want a debug or normal release..
If the compilation process succeeded, a dialog will appear, telling you that the executable was saved. A .zip file should be in the current directory, containing all required assets, e.g. documentation, libraries and the executable itself.
Notice: Currently, it's not possible to compile from the command line or for other platforms than Windows. It may work, but is unsupported.

## Documentation
Documentation for the mini games itself should be contained in the docs/games directory.