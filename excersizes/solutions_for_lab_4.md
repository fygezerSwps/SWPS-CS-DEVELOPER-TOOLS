# EXCERSIZE 1

Navigate to your home folder and display all of its contents along with permissions information.

```
cd /home/
cd linux #my user name is linux, i need to write linux here
ls -la
```

# EXCERSIZE 2

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

# EXCERSIZE 3

Using the `nano` editor, write your name to the file `firstname.txt`.

```
nano firstname.txt
Fatih Yavuz
CTRL + S
CTRL + X
```

# EXCERSIZE 4

using the `echo` command, write your last name to the file `lastname.txt`.

```
echo GEZER > lastname.txt
```

# EXCERSIZE 5

Using the cat command, display the contents of both files.

```
cat firstname.txt lastname.txt
```

# EXCERSIZE 6

Using the cat command, add the contents of the file `lastname.txt` to the file `firstname.txt`.

```
cat lastname.txt >> firstname.txt
```

# EXCERSIZE 7

Write a list of folders from your home folder to the file with the name of your choice.

```
cd /home/linux
ls -d */ > allmyfolders.txt
```

# EXCERSIZE 8

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

# EXCERSIZE 9

Using the `find` tool, search for all regular files in your home folder and save the result of the command to the file `~/my_files.txt`.

```
find ~ -type f > ~/my_files.txt
```

# EXCERSIZE 10

Using `find` search all the files you own.

```
find ~ -type f -user linux # i gotta search like that because my user name is linux. or if you want to search dynamically, type $(whoami) [same as windows's %user% thing]
```

# EXCERSIZE 11

Using `find` search for all files in the `~` folder that have been modified in the last day.

```
find ~ -type f -mtime -1
```
