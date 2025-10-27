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

> What's are these the parameters?
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
