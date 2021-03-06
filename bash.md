# The Unix Shell
## January 16-17, 2020
https://columbiaswc.github.io/2020-01-16-columbia-section-1/

contact: rob lane / rob@cs.columbia.edu

unix helpers: axinia radeva / ar2667@columbia.edu, alan crosswell / alan@columbia.edu, rahim hashim / rahim.hashim@columbia.edu, and teddy thomas / tthoma24@columbia.edu

Special thanks to https://twitter.com/mariinyrop for this notebook layout, as well as the slides that I reuse shamelessly. -Teddy

### Table of Contents

+ [Introducing the Shell](#introducing-the-shell)
+ [Navigating Files and Directories](#navigating-files-and-directories)
+ [Working with Files and Directories](#working-with-files-and-directories)
+ [Pipes and Filters](#pipes-and-filters)
+ [Loops](#loops)

## Introducing the Shell

#### Notes:

- Graphical User Interface (GUI) versus Command Line Interface (CLI)
- Read-evaluate-print-loop (REPL)
- Command, flag, argument
- Flexibility and automation
- Mac users: macOS 10.15 now uses a different shell, zsh, as the default. You want to use bash with this workshop. More details at https://support.apple.com/en-us/HT208050


#### Try

- [ ] `pwd`
- [ ] `ls`
- [ ] `ls -F`
- [ ] `ls -F Desktop`


#### Slides
- [Command Syntax](https://slides.com/marii/cul-swc-python/#/0/1)
- [Commands](https://slides.com/marii/cul-swc-python/#/0/2)



## Navigating Files and Directories


#### Notes:
- File system hierarchy
- Current working directory
- Root directory
- Home directory
- `man` and `--help`
- Abosulute vs Relative path

#### Try:

- [ ] `ls`
- [ ] `ls -F`

Either --help OR man will work
- [ ] `ls --help`
- [ ] `man ls`

Try different flags
- [ ] `ls -j`# will fail
- [ ] `ls -l` # 'long'
- [ ] `ls -R`# 'recursive'

Revisit
- [ ] `ls -F Desktop`
- [ ] `pwd`

Change directories
- [ ] `cd desktop` or `cd Desktop`
- [ ] `cd swc-materials`
- [ ] `cd data-shell`
- [ ] `cd data`

Move up
- [ ] `cd ..`

Move absolutely vs relatively
- [ ] `cd ~/Desktop/swc-materials/data-shell/data`
- [ ] `cd /`
- [ ] `cd ~`
- [ ] `cd -` # like the back button

#### Activity:

- [ ] move into `data-shell` directory
- [ ] enter the command `ls north-pacific-gyre/2012-07-03/` using tab completion

### Working With Files and Directories

### Notes
- Naming conventions for files and directories
- The Nano text editor
- Deleting with `rm` is forever

### Try
- [ ] Go back to `data-shell` by checking where you are `pwd`and using `cd`
- [ ] Check what's in `data shell` with `ls -F`

Make a directory
- [ ] Make a new directory called 'thesis' `mkdir thesis`

- [ ] Check what's in the directory again `ls -F`
- [ ] Nothing is in `thesis` because it's brand new. Check with `ls -F thesis`
- [ ] Move into `thesis` with `cd thesis`

Make a file with nano
- [ ] Use Nano to add and edit a file `nano draft.txt`. Add some lines of text, then use __Ctrl-X__ to exit.

Make a file with touch
- [ ] Make a file using touch. `touch my_file.txt`
- [ ] Use `ls -l` to inspect the files. How large is`my_file.txt`? Why?

Remove a file
- [ ] Remove the draft file with rm `rm draft.txt` using tab completion. But be careful!
- [ ] Run `ls` to see if the file is still there.

Try removing a directory
- [ ] Move back into `data-shell` with `cd ..`
- [ ] Try removing `thesis` with `rm thesis`. What happens?
- [ ] Type out `rm -r thesis` for removing the directory recursively. But don't hit enter! We're not ready to delete it yet.
- [ ] Instead try removing the directory safely with `rm -r -i thesis`. Type `y` for each file to delete.


- [ ] Make the `thesis` directory in `data-shell` again by checking where you are `pwd`and using `mkdir thesis`
- [ ] Remake the file `draft.txt` with nano `nano thesis/draft.txt`

Rename a file
- [ ] Change the filename of `draft.txt` to `quotes.txt` using `mv thesis/draft.txt thesis/quotes.txt`
- [ ] Check what happened with `ls thesis`

Move a file
- [ ] Move `quotes.txt` into the current working directory with `mv thesis/quotes.txt .`
- [ ] See what's in `thesis` with `ls thesis`
- [ ] Find `quotes.txt` in the current working directory with `ls`






## Pipes and Filters


#### Questions:
- How can I combine existing commands to do new things?

#### Try
- [ ] Go back to `data-shell` by checking where you are `pwd`and using `cd`
- [ ] Use the grep command to look for all .pdb files from ls -la output (Hint: Use a pipe `|`)


## Loops

#### Questions:
- How can I perform the same actions on many different files?

#### Notes:
We covered this very quickly, but we can do loops like we do in Python. For example

`for x in basilisk.dat minotaur.dat unicorn.dat
  do
      head -n 2 $x | tail -n 1
 done`
 
 
 ## Further Resources
 - https://swcarpentry.github.io/shell-novice/reference/
 - https://linuxconfig.org/bash-scripting-tutorial-for-beginners
 - https://www.tldp.org/LDP/Bash-Beginners-Guide/html/
 - https://dev.to/awwsmm/101-bash-commands-and-tips-for-beginners-to-experts-30je



> __Full Tutorial:__ <https://swcarpentry.github.io/shell-novice/>
