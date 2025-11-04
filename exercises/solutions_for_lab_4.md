# EXERCISE 1

Navigate to your home folder and display all of its contents along with permissions information.

```
cd /home/
cd linux #my user name is linux, i need to write linux here
ls -la
```

# EXERCISE 2

Display the contents of the `/var/log` folder sorted by size (in more human-readable sizes - KB, MB, etc.) in ascending order.

```
cd /var/log
ls -l -a -S -h -r #or we can use it shortened version "ls -laShr"
```

> [!What's are these the flags?]
> -l = for long formatting
> -a = for see all files
> -S = for descenging
> -h = for human-readable size
> -r = for reverse 

# EXERCISE 3

Using the `nano` editor, write your name to the file `firstname.txt`.

```
nano firstname.txt
Fatih Yavuz
CTRL + S
CTRL + X
```

# EXERCISE 4

using the `echo` command, write your last name to the file `lastname.txt`.

```
echo GEZER > lastname.txt
```

# EXERCISE 5

Using the cat command, display the contents of both files.

```
cat firstname.txt lastname.txt
```

# EXERCISE 6

Using the cat command, add the contents of the file `lastname.txt` to the file `firstname.txt`.

```
cat lastname.txt >> firstname.txt
```

# EXERCISE 7

Write a list of folders from your home folder to the file with the name of your choice.

```
cd /home/linux
ls -d */ > allmyfolders.txt
```

# EXERCISE 8

Using the `find` tool, search for all empty files in the home folders of all the users.

```
find /home -type f -empty
# OR
cd /home
find -type f -empty
```

> [!What's are these the flags?]
> -type f = for only searching folders
> -empty = for only search empty files

# EXERCISE 9

Using the `find` tool, search for all regular files in your home folder and save the result of the command to the file `~/my_files.txt`.

```
find ~ -type f > ~/my_files.txt
```

# EXERCISE 10

Using `find` search all the files you own.

```
find ~ -type f -user linux # i gotta search like that because my user name is linux. or if you want to search dynamically, type $(whoami) [same as windows's %user% thing]
```

# EXERCISE 11

Using `find` search for all files in the `~` folder that have been modified in the last day.

```
find ~ -type f -mtime -1
```

# EXERCISE 12

Using `find`, find all files that have the word 'mozilla' in their name and are located in subdirectories of the `/usr` directory.

```
find /usr -type f -name '*mozilla*'
```

# EXERCISE 13

Using the `find` program, find all directories with the name bin that are located in the `/usr` directory.

```
find /usr -type d -name bin
```

# EXERCISE 14

Using the `ls` and `grep` command, display only files with the extension `txt`, which are located in the `/home` folder. Write the result to the file `txt_files.txt`.

```
ls -1 /home/ | grep '\.txt$' > txt_files.txt
```

# EXERCISE 15

Display all resources from the `/var/log` folder whose name begins with 'a' and the letter 't' is in the 3rd position.

```
find /var/log -name 'a?t*'
```

# EXERCISE 16

Display the first 3 lines of the file from exercise 14

```
head -n 3 txt_files.txt
```

# EXERCISE 17

Display on the console the number of words from the file from exercise 14.

```
wc -w txt_files.txt
```

# EXERCISE 18

Hide the file `txt_files.txt` using the shell commands you learned.

```
mv txt_files.txt .txt_files.txt
```

# EXERCISE 19

Check your own ID and the groups to which you belong.

```
id 
groups
```

# EXERCISE 20

Check who is currently logged into the system.

```
who
```

# EXERCISE 21

Review the description of the directory structure - the `man 7 hier` command.

# EXERCISE 22

Display the contents of the `/home` directory.

```
ls -la /home
```

# EXERCISE 23

View the contents of the basic directories on the system (e.g. `/dev, /etc, /home, /usr`).

```
ls /dev /etc /home /usr /var /bin /tmp
```

> [!What's are these files?]
> > /dev    = device files 
> /etc     = System configuration files
> /home = User home files
> /usr     = User programs 
> /var      = Variable datas
> /bin = Files commands required for the system to function
> /tmp = Temporary files

# EXERCISE 24

Create directory `cat1` in your home directory.

```
cd /home/linux
mkdir cat1
```

# EXERCISE 25

In the `cat1` directory, create the `cat2/cat3/cat4` directory structure with one command.

```
cd /home/linux/cat1
mkdir -p cat2/cat3/cat4
```

-p = for creating parent directories if they don't exist

# EXERCISE 26

Delete the entire `cat3/cat4` directory structure with one command.

```
cd /home/linux/cat1/cat2
rm -r cat3
```

-r = for remove directories and their contents recursively

# EXERCISE 27

Create two arbitrarily named files with `.txt` and `.c` extensions in your home directory.

```
cd ~
touch textfile.txt file.c
```

# EXERCISE 28

Copy all files from your home directory with `.txt` extensions to the `cat1` directory with one command.

```
cp ~/*.txt ~/cat1/
```

# EXERCISE 29

Copy with one command all files from your home directory with `.c` extension to `cat2` directory.
