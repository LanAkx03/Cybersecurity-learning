

```bash
ssh bandit.labs.overthewire.org -p 2220 -l bandit5

bandit2@bandit.labs.overthewire.org's password: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```

The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable
-------------------------------------------------------
```bash
ls
inhere
cd inhere

ls -l
total 80K
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere00
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere01
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere02
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere03
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere04
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere05
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere06
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere07
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere08
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere09
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere10
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere11
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere12
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere13
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere14
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere15
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere16
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere17
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere18
drwxr-x--- 2 root bandit5 4.0K Sep 19 07:08 maybehere19

```

```bash
du -b -a | awk '$1 == 1033 {print "\033[1;31m" $0 "\033[0m"; next} {print}'
[...]
8261    ./maybehere11/.file3
38333   ./maybehere11
3065    ./maybehere07/.file1
3663    ./maybehere07/-file1
4130    ./maybehere07/spaces file1
3362    ./maybehere07/-file3
2488    ./maybehere07/-file2
```
   <span style="color:red">1033    ./maybehere07/.file2</span>
```bash
1022    ./maybehere07/spaces file3
9064    ./maybehere07/spaces file2
1997    ./maybehere07/.file3
29824   ./maybehere07
3427    ./maybehere14/.file1
4282    ./maybehere14/-file1
[...]
```

#OU

```bash
du -b -a | grep 1033
1033    ./maybehere07/.file2
```


### ET ENFIN 

```bash
cat ./maybehere07/.file2
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

logout
```

#OU

```bash
cd maybehere07
ls -a --all

.  ..  -file1  .file1  -file2  .file2  -file3  .file3  spaces file1  spaces file2  spaces file3

cat .file2 
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

logout
```
