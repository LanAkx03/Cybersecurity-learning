The password for Century2 is the **build version** of the instance of PowerShell installed on this system.  
  
**NOTE:**  
– The format is as follows: ****.*.*****.******  
– Include all periods  
– Be sure to look for build version and NOT PowerShell version  
  
  
**IMPORTANT:**  
Once you feel you have completed the Century1 challenge, start a new connection to the server, and log in with the username of Century2 and this password will be the answer from Century1. If successful, close out the Century1 connection and begin to solve the Century2 challenge. This concept is repeated over and over until you reach the end of the game.

---
```PuTTY
Hostname : century.underthewire.tech
port : 22
```

```PowerShell
login as: century1
century1@century.underthewire.tech's password: century1
```

```PowerShell
Windows PowerShell
Copyright (C) 2016 Microsoft Corporation. All rights reserved.

Under the Wire... PowerShell Training for the People!
PS C:\users\century1\desktop>
```

```PowerShell
$PSVersionTable
```
```Output
Name                           Value
----                           -----
PSVersion                      5.1.14393.7254
PSEdition                      Desktop
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0...}
BuildVersion                   10.0.14393.7254
CLRVersion                     4.0.30319.42000
WSManStackVersion              3.0
PSRemotingProtocolVersion      2.3
SerializationVersion           1.1.0.1

```

==> 10.0.14393.7254

