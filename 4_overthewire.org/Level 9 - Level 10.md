
```bash
ssh bandit.labs.overthewire.org -p 2220 -l bandit9

bandit2@bandit.labs.overthewire.org's password: 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```
----
##### Level Goal

The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

##### Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

---

```bash
 strings data.txt | grep ==
```
```Output
}========== the
3JprD========== passwordi
~fDV3========== is
D9========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```
```bash
logout
```