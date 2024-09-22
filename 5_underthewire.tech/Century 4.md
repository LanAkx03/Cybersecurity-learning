The password for Century5 is the name of the file within a directory on the desktop that has spaces in its name.  
  
**NOTE:**  
– The password will be lowercase no matter how it appears on the screen.

```bash
ssh -p 22 century4@century.underthewire.tech
century1@century.underthewire.tech's password: 123
```


```bash
PS C:\users\century4> get-childitem .\desktop\ -Recurse


    Directory: C:\users\century4\desktop


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
d-----        2/14/2024   2:35 PM                Can You Open Me
d-----        9/12/2024   7:02 PM                test
-a----        8/22/2024   9:19 PM              0 files.txt
-a----        8/30/2024  12:52 AM           1290 output.txt


    Directory: C:\users\century4\desktop\Can You Open Me


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
-a----        2/14/2024   2:35 PM             24 34182

exit

```

==> 34182