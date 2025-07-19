# How to add new games?
## Step 1: Set up your envirement
- If your desired script does not contain a certain function, class or bunch of variables that can be globally used (e.g. stuff like a menu API, another sound manager etc) you can add it to the req folder and it automatically will be included. However, if you need something like the rotation or sound pool or anything else that is an nvgt default include but not included by the main script, please edit main.nvgt correspondingly instead of copying it too or including it in another minor script.
    * It does not matter what coding style the requirement uses, as long as it does not conflict with other variables, classes, functions etc of the code.
- Create a folder named the same way as your game in the games folder. It not should be to long. For example, if you create a hang man game the folder could be named hangman, but not "hang man - a game where you have to guess the word - version 7.24.81.1 build 67".

## Step 2: Write your game.
When writing your games, please consider these things:
- Your code style does not matter. Wether you write a function void test()\r\n{\r\nalert("hi","this is a test");\r\n} or void test () {\r\nalert("test", "this is a test");\r\n}, we do not mind as long as it is somewhat readable and especially executable.
- Please write your game as class titled in the long format of the game's name. So hang_man for example. Place the variables within, and set them to private unless it needs to be accessed from outside. This avoids that any other game could have a possible conflict with it, or generally just access it.
- Name the main function class::main(). This is the function which will be executed when entering the game.
- Ensure the game can be plaied multiple times. Thus, any important variables should be reset upon launching the game, or possibly be re-inicialized in the function itself if they aren't being needed in other functions.
- Do not use exit or show_window statements, and if you expect errors catch them and thread them properly instead of letting the game crash.
- If you need to access and safe settings, instead of creating your own code please use the declared sd (settings) class. It is documented, but you can use functions like string sd.read_string(string string_name, string efault_return_value).
    * Notice. The variables are not named this way, just an example for showcase.
- You are allowed to use multiple files and name them after your desires. For a clear codebase, do not place any other files than these which will be compiled inside the directory (e.g. just NVGT scripts without a void main function in no class, so class::main is fine) unless urgently required or wanted (such as documentation to complex functions where it would be to long text which would interrupt the code flow). However, if you need extra assets and sounds, place them in docs/, misc/<gamename> and packsounds for the sounds in any format which should be packed.
- If possible, use packs instead of sound files. Place the compiled pack in sounds, and the corresponding sounds as above explained.
- Use return and break statements instead of re-running previous functions to avoid a large stack. This makes it easier to debug the application.

## Step 3: Linking
If you are done writing your game, please do the following to integrate your game into the launcher.
* Open main.nvgt in the root directory, and add your game as the last new element on the games array.
* Open games/games.nvgt, and add a new line at the end of the file: ```#include"<your game name>/*.nvgt"```
* Lastly, open misc/launch.nvgt. Before the line that says "bool run_game(string game)" init a new instance of your class. Write: ```<your class in long format> <a very short letter code without numbers (e.g. hm for hangman>;```
* Now insert an if statement before the line that says mainmenu(). ```if(game=="<the name of your game in the array>") <short letter instance>.main();```
That should be done. I know, it sounds more complex than it actually is. If you dind't understand something, please look into the other files for showcase, since they are multiple games which are already there and you can learn from how to integrate.

## Step 4: Documentation
Document your game unless it's really an obvious one like guess the number. Create a file called docs/games/<your game>.txt. The name of the .txt file should be the same as in step 3.1 (this is required for the documentation parser to understand). Write down your description in readable normal text (without marcdown or html tags). You also should create a changelog entry, however this is optional. If you do not which is fine, one will be created by one of the contributors.

## Step 5: Testing and submitting
Please, before you submit, perform at least one to three test runs while you play your game. It should be possible to play it without any errors and it should be idiot-safe (e.g. you can't break it by doing something which is actually not really common sense). After that you can submit a new pull request and you should receive feedback within a few hours to days. This most likely also can depends on game complexity and the way the code has been written.