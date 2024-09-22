
```bash
ssh bandit.labs.overthewire.org -p 2220 -l bandit8

bandit2@bandit.labs.overthewire.org's password: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```
-----
#### Level Goal

The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

##### Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

##### Helpful Reading Material

- [Piping and Redirection](https://ryanstutorials.net/linuxtutorial/piping.php)
---
```bash
sort data.txt | uniq -u
```
- `sort data.txt`: Sorts the lines in `data.txt`.
- `uniq -u`: Filters and prints only the lines that appear exactly once.

```Output
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```
