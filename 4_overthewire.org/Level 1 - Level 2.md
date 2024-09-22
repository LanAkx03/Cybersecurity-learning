
```bash
ssh bandit.labs.overthewire.org -p 2220 -l bandit1

bandit2@bandit.labs.overthewire.org's password: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```

The password for the next level is stored in a file called **-** located in the home directory

---------------------------------------

```bash
ls
-

cat - 
///

```

> This type of approach has a lot of misunderstanding because using **-** as an argument refers to **STDIN/STDOUT** i.e **dev/stdin** or **dev/stdout** .So if you want to open this type of file you have to specify the full location of the file such as **./-** .For eg. , if you want to see what is in that file use **cat ./-** 

```bash
cat ./-

263JGJPfgU6LtdEvgfWU1XP5yac29mFx

logout
```

