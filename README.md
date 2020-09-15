# Exercises of MIT Missing Semester 2020

### [01. Course overview + the shell](https://github.com/laiyenju/MIT-Missing-Semester-exercises/blob/master/01-course-overview-shell.md)

- [x] 1. Check if it says something like `/bin/bash` or `/usr/bin/zsh`, that means you’re running the right program.
- [x] 2. Create a new directory called `missing` under `/tmp`.
- [x] 3. Look up the `touch` program. The man program is your friend.
- [x] 4. Use `touch` to create a new file called `semester` in `missing`.
- [ ] 5. Write the following into that file, one line at a time:

```bash
#!/bin/sh
curl --head --silent https://missing.csail.mit.edu
```

- [ ] 6. Try to execute the file, i.e. type the path to the script (`./semester`) into your shell and press enter.
- [ ] 7. Run the command by explicitly starting the sh interpreter, and giving it the file `semester` as the first argument, i.e. `sh semester`. Why does this work, while `./semester` didn’t?
- [ ] 8. Look up the `chmod` program (e.g. use `man chmod`).
- [ ] 9. Use `chmod` to make it possible to run the command `./semester` rather than having to type `sh semester`.
- [ ] 10. Use `|` and `>` to write the “last modified” date output by `semester` into a file called `last-modified.txt` in your home directory.
- [ ] 11. Write a command that reads out your laptop battery’s power level or your desktop machine’s CPU temperature from `/sys`. 

### [02. Shell Tools and Scripting](https://missing.csail.mit.edu/2020/course-shell/)

- [ ] 1. Read `man ls` and write an `ls` command that lists files in the following manner
- [ ] 2. Write bash functions marco and polo that do the following.
- [ ] 3. Write a bash script that runs the following script until it fails and captures its standard output and error streams to files and prints everything at the end. 
- [ ] 4. write a command that recursively finds all HTML files in the folder and makes a zip with them. Note that your command should work even if the files have spaces (hint: check -d flag for xargs)
- [ ] 5. (Advanced) Write a command or script to recursively find the most recently modified file in a directory. More generally, can you list all files by recency?

### [03. Editors (Vim)](https://github.com/laiyenju/MIT-Missing-Semester-exercises/blob/master/03-editor-vim-note.md)

- [x] 1. Complete `vimtutor`. Note: it looks best in a [80x24](https://en.wikipedia.org/wiki/VT100) (80 columns by 24 lines) terminal window.
- [x] 2. Download our [basic vimrc](https://missing.csail.mit.edu/2020/files/vimrc) and save it to `~/.vimrc`. Read through the well-commented file (using Vim!), and observe how Vim looks and behaves slightly differently with the new config.
- [x] 3. Install and configure a plugin: [ctrlp.vim](https://github.com/ctrlpvim/ctrlp.vim). (and the other detail steps)
- [x] 4. To practice using Vim, re-do the Demo from lecture on your own machine.
- [x] 5. Use Vim for all your text editing for the next month.
- [x] 6. Configure your other tools to use Vim bindings (see instructions above).
- [x] 7. Further customize your `~/.vimrc` and install more plugins.
- [x] 8. (Advanced) Convert XML to JSON ([example file](https://missing.csail.mit.edu/2020/files/example-data.xml)) using Vim macros. 

### [04. Data Wrangling]()

- [ ] 1. Take this [short interactive regex tutorial](https://regexone.com/).
- [ ] 2. Find the number of words (in `/usr/share/dict/words`) that contain at least three `a`s and don’t have a `'s` ending. 
- [ ] 3. To do in-place substitution it is quite tempting to do something like `sed s/REGEX/SUBSTITUTION/ input.txt > input.txt`.
- [ ] 4. Find your average, median, and max system boot time over the last ten boots.
- [ ] 5. Look for boot messages that are not shared between your past three reboots (see `journalctl`’s `-b` flag). 
- [ ] 6. Find an online data set like [this one](https://stats.wikimedia.org/EN/TablesWikipediaZZ.htm), [this one](https://ucr.fbi.gov/crime-in-the-u.s/2016/crime-in-the-u.s.-2016/topic-pages/tables/table-1). or maybe one [from here](https://www.springboard.com/blog/free-public-data-sets-data-science-project/). Fetch it using `curl` and extract out just two columns of numerical data.

### [05. Command-line Environment](https://missing.csail.mit.edu/2020/command-line/)

### [06. Version Control(Git)](https://missing.csail.mit.edu/2020/version-control/)

### [07. Debugging and Profiling]()

### [08. Metaprogramming]()

### [09. Security and Cryptography]()

### [10. Potpourri]()
