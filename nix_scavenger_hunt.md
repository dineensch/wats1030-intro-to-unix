# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:*

Running the 'pwd' command:

```
dineen@laptop:/mnt/c/Users/dinee/Desktop/wats1030-intro-to-unix$ pwd
/mnt/c/Users/dinee/Desktop/wats1030-intro-to-unix
```

* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?*

Running the 'ls' command displayed all the files within this directory:

```
challenge_files  LICENSE  nix_scavenger_hunt.md  nix_scavenger_hunt_stretch.md  README.md  super_scavengers.md
```

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?*

Running the '-alh' options gave a listed output of the files in the directory and included more details:

```
total 16K
drwxrwxrwx 0 root root  512 Apr 15 16:05 .
drwxrwxrwx 0 root root  512 Apr 15 16:07 ..
drwxrwxrwx 0 root root  512 Apr 15 16:05 challenge_files
drwxrwxrwx 0 root root  512 Apr 15 17:18 .git
-rwxrwxrwx 1 root root 1.1K Apr 15 16:05 LICENSE
-rwxrwxrwx 1 root root 5.5K Apr 15 16:05 nix_scavenger_hunt.md
-rwxrwxrwx 1 root root  322 Apr 15 16:05 nix_scavenger_hunt_stretch.md
-rwxrwxrwx 1 root root 2.8K Apr 15 16:05 README.md
-rwxrwxrwx 1 root root  200 Apr 15 16:05 super_scavengers.md
```


* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://man.he.net/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?*

All:
```
-a -- outputs all the files and does not ignore entries starting with a period
```

Long Listing:
```
-l --use a long listing format which gives more details
```

Human-Readable:
```
-h --outputs are human-readable with -l and/or -s, print human readable sizes (e.g., 1K 234M 2G)
```

* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*

When running 'ls /' I received an output of directories.  These are based on the Linux Filesystem Hierarchy Standard.

```
bin  boot  dev  etc  home  init  lib  lib64  media  mnt  opt  proc  root  run  sbin  snap  srv  sys  tmp  usr  var
```

* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*

Using the 'cd /' command:

```
dineen@laptop:/mnt/c/Users/dinee/Desktop/wats1030-intro-to-unix$ cd /
dineen@laptop:/$
```

Using the 'pwd' command:

```
dineen@laptop:/$ pwd
/
```

* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*

Using the 'cd ~' command:

```
dineen@laptop:/$ cd ~
dineen@laptop:~$
```

Using the 'pwd' command:
```
dineen@laptop:~$ pwd
/home/dineen
```


* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?*

By using the 'ls *.demo' command, I found 3 files ending with '.demo':

``` 
dineen@laptop:/mnt/c/Users/dinee/Desktop/wats1030-intro-to-unix/challenge_files$ ls *.demo
2015_special_stuff.demo  cloaked-wookie.demo  scooter-double-mamba.demo
```

* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*

Using the 'cd ..' command brought me back to the main project folder: 

``
dineen@laptop:/mnt/c/Users/dinee/Desktop/wats1030-intro-to-unix/challenge_files$ cd ..
dineen@laptop:/mnt/c/Users/dinee/Desktop/wats1030-intro-to-unix$
``

* Press the up arrow on your keyboard. *What just happened?*

It repopulated the last command I used.

* Press the up arrow a few more times. *What do you see?*

It cycles through all the previous commands I have used.

* Run the `history` command. *What do you see?*

It shows ALL of the commands I have used (during this session I assume)

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*

'whoami' 

```
dineen@laptop:/mnt/c/Users/dinee/Desktop/wats1030-intro-to-unix$ whoami
dineen
```
I am logged in as user 'dineen'

* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*

No other users are using the system!

* How long has your system been running? Use `uptime` to see, and *paste the result here:*

The 'uptime' command shows current time, how long the system has been running, how many users are logged on, and the system load averages for the past 1, 5, and 15 minutes:

```
dineen@laptop:/mnt/c/Users/dinee/Desktop/wats1030-intro-to-unix$ uptime
 18:26:02 up  2:21,  0 users,  load average: 0.52, 0.58, 0.59
```

* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*

It seems that the 'ps aux' command puts out a little synopsis of your computer's performance, memory use and activity

```
dineen@laptop:/mnt/c/Users/dinee/Desktop/wats1030-intro-to-unix$ ps aux
USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root         1  0.0  0.0  10440   104 ?        Ss   16:04   0:00 /init
dineen       2  0.0  0.0  25800  2744 tty1     Ss   16:04   0:00 -bash
dineen     277  0.0  0.0  41468  1840 tty1     R    18:28   0:00 ps aux
```


* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?*

The 'top' command looks like a combination of the results I saw from the commands: 'who' 'uptime' and a more detailed 'ps aux' command.


### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?*

I found 2 files:

```
dineen@laptop:/mnt/c/Users/dinee/Desktop/wats1030-intro-to-unix/challenge_files$ ls *credit*
credit_cards2.txt  credit_cards.txt
```

* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?*

The file credit_cards.txt was last updated on 01-15-2015

* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*

'modi_laboriosam.text' is located in the 'tmp' folder:

```
dineen@laptop:/mnt/c/Users/dinee/Desktop/wats1030-intro-to-unix/challenge_files$ find . -name modi_laboriosam.txt
./tmp/modi_laboriosam.txt
```

* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*

I found 2 files containing 'WA'

```
dineen@laptop:/mnt/c/Users/dinee/Desktop/wats1030-intro-to-unix/challenge_files$ grep "WA" *.user
Britt-Erdman.user:O'Harachester, WA 37261
Lissie-Strosin.user:Jewessfurt, WA 00816-7241
```

* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*

```
dineen@laptop:/mnt/c/Users/dinee/Desktop/wats1030-intro-to-unix/challenge_files$ grep --color -r "Waldo" *
serial-numbers/eaque_molestiae.txt:Ut est maiores quia autem. Nisi modi Waldo sed corporis sit explicabo ut est. Et est placeat ea sunt sunt consectetur sunt incidunt. Explicabo vel esse blanditiis dolorem culpa non quia.
```

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*

A list of names ending with ".user" so I am assuming it is a list of users.

* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*

I'm given a shorten view of the overall list.  When I hit 'enter' the list populates a new line for viewing.

* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*

```
dineen@laptop:/mnt/c/Users/dinee/Desktop/wats1030-intro-to-unix/challenge_files$ ps aux | grep dineen
dineen       2  0.0  0.0  25800  2760 tty1     Ss   16:04   0:01 -bash
dineen     319  0.0  0.0  41468  1844 tty1     R    19:24   0:00 ps aux
dineen     320  0.0  0.0  38696  1104 tty1     S    19:24   0:00 grep --color=auto dineen
```