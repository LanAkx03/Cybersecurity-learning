
```bash
ssh bandit.labs.overthewire.org -p 2220 -l bandit7

bandit2@bandit.labs.overthewire.org's password: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```

--------------
##### Level Goal

The password for the next level is stored in the file **data.txt** next to the word **millionth**

##### Commands you may need to solve this level

[man](https://manpages.ubuntu.com/manpages/noble/man1/man.1.html), grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

--------------

```bash
grep "millionth" data.txt
```
```Output
millionth       dfwvzFQi4mU0wfNbFOe9RoWskMLg7eE
```
```bash
logout
```

#OR

```bash
awk '/millionth/' data.txt
```
```Output 
millionth       dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc 
```
```bash
logout
```

U can use `'/millionth/ {print $2}'` too
- `{print $2}` prints the second field (assuming the password is next to "millionth").

