# Intro to the Command Line

## Goal of the class
Our goal today is to get everyone to a point where they feel comfortable opening the command line, navigating files, and learning something new. There are a lot of command line tools you can learn to use at NICAR, but those can be super intimidating if you have never used it before. My goal is that everyone is going to leave class today ready, willing, and able to use the command line and learn new command line tools.

In the class today, we are going to receive some leaked data, make a home for our reporting on our computer, inspect the data, and do some very minor changes to it. We are first going to do all this the way that we all know how, using the computer's graphical interface. Then we are going to do everything using the command line!

[Slides](https://docs.google.com/presentation/d/1oL0rNS2DYkMhfaYe6mosHkYFBm69ypuLtqqkqXHiHPc/edit?usp=sharing)

[Data](https://drive.google.com/drive/folders/13iIKLBNqXgSqbW6rd7dR7ehrdsKBUOaZ?usp=sharing)


## Class Notes
Class will follow the [slides](https://docs.google.com/presentation/d/1oL0rNS2DYkMhfaYe6mosHkYFBm69ypuLtqqkqXHiHPc/edit?usp=sharing). Here are the notes for the session.
- Intro
  - Will Craft, data reporter for APM Reports and the podcast In The Dark
  - Goal of the class: get you familiar with the command line. I am NOT going to teach you everything you ever need to know, but you’ll leave the class knowing how to use the command line to learn other things. There are thousands of tools you can use from the command line
    - examples: removing duplicates from a dataset, moving thousands of files with a few keystrokes, uploading data to databases.

- Agenda
  - Making a home for a project using familiar tools
  - Making a home for a project using unfamiliar tools
    - What is the command line? Some useful definitions
    - How to read and write stuff on the command line
    - Useful commands
    - Making a home for the project

- Someone leaked us some data!

- Make a home for the project using Finder
  - Steps:
    1. Make a folder for the project and make folders for data
      - open Finder (the mac GUI)
    2. Download the Data to Downloads (or find it in Downloads)
    3. Inspect the files
      - use space bar to inspect the contents
    4. Move the data into new folders
      - create new folders

- Now we'll do the same using the command line! But first... What is the command line?

- Text-based video games
  - maybe you've played an old video game where you typed commands to your character and they do something. Basically this is what we do with the command line

- definition of CLI, GUI
    - GUI - graphical user interface. We interact with graphical representations of things to manipulate the computer and give it commands. Windows and the little mouse and all that on the computer is the GUI
    - CLI - command line interface. Text-based way of giving commands to the computer. When we are talking about the command line, we are talking about the command line interface. Everyone has a program on their computer called Terminal. If you hit command-space and type "Terminal", your computer GUI should show you the program

- famous command lines throughout history

- How to read and write on the command line 1
  - screenshot of the terminal, diagrammed. Also called the shell. The program that allows you to type commadns to the computer
  - prompt - The prompt is a bit of information that is displayed on the command line, literally prompting you to input information. It usually separates from the space you type from the info with a `$`. On my computer, it just shows the user and the directory I am in (me, `wcraft`, and the home folder `~`, which is `Users/wcraft`). It will be different for you.
  - command line, where you type

- How to read and write on the command line 2
  - screenshot of the terminal, with a command
  - utility - utility is the proper name for the tools & commands that we use on the command line. This is `ls`, which __l__ i __s__ ts the contents.
  - flag - flags change how the utility operates. There are a lot of different flags for pretty much every utility. `ls` with `-G` displays in color, `ls` without `-G` displays in the normal text color
  - arguments - arguments are the things that you want the utility to operate on. Not every utility needs arguments, but most do. This command is saying list the stuff that is inside the folder `apm_reports/training_and_guides`

- introduce commands
    - pwd - print working directory, tells you where you are in the computer. The space where the terminal prints stuff out to is called the standard output.
    - mv - command to move
    - ls - list the contents of a file
    - cd - change directory, move to a new directory
    - mkdir -  make a new directory
    - cat - short for concatinate, prints the contents of a file
    - introduce shortcuts/tricks
      - tab completion - hit tab to auto-complete long stuff and show you what might fit.
      - go back through old commands with the up-arrow
      - no argument - usually means, do the operation on the current directory
      - `cd ..` - go up the directory
      - `man` + utility name - brings up a helpful page with information on the utility, includes details on every flag.
      - `clear` - clears the terminal of all outputs

- Make a home for the project using Terminal
  - Steps:
    - Open the command line - Terminal
    - Where are we on the computer? What's there?
      - `pwd`
      - `ls`
    - Go into the Downloads folder and look around for the secret data folder. What's there?
      - `cd Downloads`
      - `ls`
      - `ls SECERT_DATA_DO_NOT_SHARE`
    - Make a folder for the project and make folders for data
      - `cd ~`
      - `mkdir secret-data-project`
      - `cd secret-data-project`
      - `mkdir data`
      - `mkdir data/source`
      - `mkdir data/processed`
    - Move the data from downloads into our project folders
      - `mv ~/Downloads/SECRET_DATA_DO_NOT_SHARE/` (then hit tab twice to see files)
      - `mv ~/Downloads/SECRET_DATA_DO_NOT_SHARE/Janmeownary_Bribes.csv data/source/`
      - `ls data/source/`
      - `mv ~/Downloads/SECRET_DATA_DO_NOT_SHARE/Febmeownary_Bribes.csv data/source/`
      - `ls data/source/`
    - Inspect the file locations (ls & cat/head)
      -  `cat data/source/Janmeownary_Bribes.csv`
    - Learn a new utility: csvkit
      - Using `cat` on the data sucks, it does not make inspecting spreadsheets on the command line easy at all. So lets learn a new utility, `csvlook`, which is part of the csvkit set of tools for working with CSVs.
      - [csvlook](https://csvkit.readthedocs.io/en/latest/scripts/csvlook.html)

- Advanced (if we have time)
  - csvkit (practice how to read instructions from the web, deal with failure)
  - other useful commands (pbcopy, pipes)


## Terminology
GUI - graphical user interface
CLI - command line interface, or the command line.
STDIN -
STDOUT -


## Other Classes here at NICAR22
Finding needles in haystacks with fuzzy matching
Advanced PDF processing with OCR and command-line tools
Intro to R or Intro to Python.

## Other Online Resources
- [Getting to Know the Command Line](https://www.davidbaumgold.com/tutorials/command-line/)
- [Ryan Murphy's Favorite Command Line Tools](https://gist.github.com/rdmurphy/d027bbe7bf6f8e6bbb5a0ad3c2194b86)
- [Taking Command of the Command Line](https://github.com/chrislkeller/nicar15-command-line-basics)
- [100+ Command Line Tools for Data Visualization](https://observablehq.com/@asg017/100-command-line-tools-for-data-viz)
 - [Art of the Command Line](https://github.com/jlevy/the-art-of-command-line)
