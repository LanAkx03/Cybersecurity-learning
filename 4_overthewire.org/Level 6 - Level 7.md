
```bash
ssh bandit.labs.overthewire.org -p 2220 -l bandit6

bandit2@bandit.labs.overthewire.org's password: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```

The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size
-------------------------------------------------------
```bash
bandit6@bandit:~$ ls -a -l
```
```bash
total 20
drwxr-xr-x  2 root root 4096 Sep 19 07:08 .
drwxr-xr-x 70 root root 4096 Sep 19 07:09 ..
-rw-r--r--  1 root root  220 Mar 31 08:41 .bash_logout
-rw-r--r--  1 root root 3771 Mar 31 08:41 .bashrc
-rw-r--r--  1 root root  807 Mar 31 08:41 .profile
```

```bash
du -b -a
```
```bash
807     ./.profile
3771    ./.bashrc
220     ./.bash_logout
4798    .
```

We use the `find` command with the following options:

- `-type f`, because we are looking for a file
- `-user bandit7`, to find files owned by the ‘bandit7’ user
- `-group bandit6`, to find files owned by the ‘bandit6’ group
- `-size 33c`, to find files of size 33 bytes

We need to run the command from the root directory to search the whole system. Running the command `find / -type f -user bandit7 -group bandit6 -size 33c` will,

```bash
find / -type f -user bandit7 -group bandit6 -size 33c
```
```bash
find: ‘/var/cache/private’: Permission denied
find: ‘/var/cache/apparmor/2425d902.0’: Permission denied
find: ‘/var/cache/apparmor/baad73a1.0’: Permission denied
find: ‘/var/lib/polkit-1’: Permission denied
find: ‘/var/lib/amazon’: Permission denied
**/var/lib/dpkg/info/bandit7.password**
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/chrony’: Permission denied
find: ‘/var/lib/snapd/void’: Permission denied
find: ‘/var/lib/snapd/cookie’: Permission denied
find: ‘/var/lib/private’: Permission denied
```

However, also print a `Permission denied` error for files that we do not have permission. We can append `2>/dev/null`, which will ‘hide’ all error messages [1](https://stackoverflow.com/questions/762348/how-can-i-exclude-all-permission-denied-messages-from-find).

```bash
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
```
```bash
/var/lib/dpkg/info/bandit7.password
```

And we got the file and can read the next password.

```bash
cat /var/lib/dpkg/info/bandit7.password
```
```bash
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```
