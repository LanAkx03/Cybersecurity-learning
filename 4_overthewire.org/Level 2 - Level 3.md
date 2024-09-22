
```bash
ssh bandit.labs.overthewire.org -p 2220 -l bandit2

bandit2@bandit.labs.overthewire.org's password: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```

The password for the next level is stored in a file called **spaces in this filename** located in the home directory

---------------------------------------------

```bash
ls
spaces in this filename
cat spaces\ in\ this\ filename
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
#OU

cat "spaces in this filename"
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

logout
```
