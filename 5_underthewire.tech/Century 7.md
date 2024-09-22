The password for Century8 is in a readme file somewhere within the contacts, desktop, documents, downloads, favorites, music, or videos folder in the user’s profile.  
  
**NOTE:**  
– The password will be lowercase no matter how it appears on the screen.

---
```bash
ssh -p 22 century7@century.underthewire.tech
century1@century.underthewire.tech's password: 197
```

```bash
PS C:\users\century7\desktop> ls
PS C:\users\century7\desktop> cd ..
PS C:\users\century7> ls


    Directory: C:\users\century7


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
d-r---        7/16/2016   1:23 PM                Desktop
d-r---        8/30/2018   3:10 AM                Documents
d-----        9/10/2024  12:06 PM                Downloads
d-r---        7/16/2016   1:23 PM                Favorites
d-r---        7/16/2016   1:23 PM                Links
d-r---        7/16/2016   1:23 PM                Music
d-r---        7/16/2016   1:23 PM                Pictures
d-----        7/16/2016   1:23 PM                Saved Games
d-r---        7/16/2016   1:23 PM                Videos


PS C:\users\century7> cd Documents
PS C:\users\century7\Documents> ls
PS C:\users\century7\Documents> cd ..
PS C:\users\century7> cd Downloads
PS C:\users\century7\Downloads> ls


    Directory: C:\users\century7\Downloads


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
-a----        2/26/2024  10:10 PM              0 ABLA321
-a----        8/30/2018   3:29 AM              7 ABLA321.txt
-a----         3/4/2024   1:50 PM          87054 Alias.txt
-a----         3/4/2024   1:50 PM        1251758 Command.txt
-a----        2/25/2022  10:18 PM             17 LineNumbers.txt
-a----        5/20/2024   6:35 PM             20 MikeWasHere.txt
-a----        8/30/2018   3:29 AM              7 Readme.txt
-a----        9/10/2024  12:06 PM              0 test
-a----        8/20/2024  10:32 AM             17 This is not the password.txt
-a----        8/30/2018   3:29 AM              7 TREMPETTE3221.txt

```

#OR 

```bash
PS C:\users\century7> get-childitem ./ -Include *readme* -Recurse


    Directory: C:\users\century7\Downloads


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
-a----        8/30/2018   3:29 AM              7 Readme.txt

```

```bash
PS C:\users\century7> Get-Content ./Downloads/Readme.txt
7points
```

==> 7points
