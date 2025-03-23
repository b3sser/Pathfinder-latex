# Pathfinder 2e LaTeX Character Sheet Template
LaTeX template for typesetting Pathfinder 2e Character Sheets

## IMPORTANT: This is a work in progress. So far, only the first page ist supported.

## Features
- 4-page Character Sheet
- Automatic calculation of Modifiers, Proficiency and other Derived Stats
- Player input via custom commands for a clean and compact tex file
- Example character to illustrate usage

## Usage
#### TL;DR
1. Copy ```empty.tex```
2. Fill commands with your values and text
3. Compile with XeLaTeX

Look at ```example-character.tex``` for guidance

#### Tips & Tricks
- Each stat has a custom command, listed and sorted in the empty sheet. The names of the commands should tell you, what Stat goes in there. If there are options, multiple arguments or other things special to a command, they will be explained in a comment.
- For Skills and Weapons, if you want to leave a line completely blank, you can just delete it for a cleaner tex-file and everything should still work as expected. If it doesn't, please open an issue.

- Some fields have automatic line-wrap, for others use ```\\``` where needed
- All fields have a default font size to fit with a normal amount of input. You can change the size for selected fields by adding a size command before your actual input.
    - Sizes: ```\Huge```, ```\huge```, ```\LARGE```, ```\Large```, ```\large```, ```\normalsize```, ```\small```, ```\footnotsize```, ```\scriptsize```, ```\tiny```

- If you need to overwrite the auto-calculated values, you can often do so, by using ```\renewcommand``` *after* the command it is associated with. *E.g. using ```\renewcommand{\ACtotal}{20}``` after the ```\AC{}{}{}``` command.* You can find out, what the values are called by checking the respective ```commands.tex``` for the page. If you have trouble with this, feel free to contact me for advice and custom solutions any time.

## Compilation & Dependencies
This Template is designed to be compiled with **XeLaTeX**. XeTeX may also work but is not explicitely tested.

*Personally, I opened the folder in VSCodium with LaTeX Workshop Extension and ran ```Recipe: latexmk (xelatex)```*

If you are encountering issues, please make sure you have ```xetex-pstricks``` installed.

## Credits
This package was created based on the standard Paizo Inc. PDF character sheet template and uses it as background image. Pathfinder, and the Pathfinder logo are registered trademarks of Paizo Inc.

The basic code structure and several concepts were adapted from matsavages great [DnD 5e LaTeX Character Sheet Template](https://github.com/matsavage/DND-5e-LaTeX-Character-Sheet-Template), with his permission.

## Feedback & Bugs
I appreciate any feedback and bug reports on this project.
Please open an issue on github, describing the bug and adding code snippets, screenshots (if needed) and information about your compiler.
