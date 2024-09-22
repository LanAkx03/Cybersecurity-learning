
```bash
ssh bandit.labs.overthewire.org -p 2220 -l bandit10

bandit2@bandit.labs.overthewire.org's password: FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```
----
##### Level Goal

The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

##### Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

##### Helpful Reading Material

- [Base64 on Wikipedia](https://en.wikipedia.org/wiki/Base64)
----
```bash
cat data.txt
```
```Output
VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==
```
```bash
base64 -d data.txt
```
```Output
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```
