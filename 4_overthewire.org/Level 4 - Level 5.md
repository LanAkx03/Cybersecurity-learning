
```bash
ssh bandit.labs.overthewire.org -p 2220 -l bandit4

bandit2@bandit.labs.overthewire.org's password: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```

The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

---------------------------------------------

```bash
cd inhere
ls inhere
-file00 -file01 -file02 -file03 -file04 -file05 -file06 -file07 -file08 -file09

cat./file00
[...]
cat ./-file07
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

logout
```

