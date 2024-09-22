```PuTTY
Hostname : century.underthewire.tech
port : 22
```

```PowerShell
login as: century2
century1@century.underthewire.tech's password: 10.0.14393.7254
```

#OU 

Dans GitBash
```bash
ssh -p 22 century2@century.underthewire.tech
century1@century.underthewire.tech's password: 10.0.14393.7254
```

```bash
dir
 Directory: C:\users\century2\desktop


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
-a----        8/30/2018   3:29 AM            693 443

exit
```

```bash
 Get-Help wget

NAME
    Invoke-WebRequest

SYNOPSIS
    Gets content from a web page on the Internet.


SYNTAX
    Invoke-WebRequest [-Uri] <Uri> [-Body <Object>] [-Certificate <X509Certificate>] [-CertificateThumbprint <String>]
    [-ContentType <String>] [-Credential <PSCredential>] [-DisableKeepAlive] [-Headers <IDictionary>] [-InFile <String>]
    [-MaximumRedirection <Int32>] [-Method {Default | Get | Head | Post | Put | Delete | Trace | Options | Merge | Patch}]
    [-OutFile <String>] [-PassThru] [-Proxy <Uri>] [-ProxyCredential <PSCredential>] [-ProxyUseDefaultCredentials]
    [-SessionVariable <String>] [-TimeoutSec <Int32>] [-TransferEncoding {chunked | compress | deflate | gzip | identity}]
    [-UseBasicParsing] [-UseDefaultCredentials] [-UserAgent <String>] [-WebSession <WebRequestSession>] [<CommonParameters>]


DESCRIPTION
    The Invoke-WebRequest cmdlet sends HTTP, HTTPS, FTP, and FILE requests to a web page or web service. It parses the
    response and returns collections of forms, links, images, and other significant HTML elements.

    This cmdlet was introduced in Windows PowerShell 3.0.


RELATED LINKS
    Online Version: http://go.microsoft.com/fwlink/?LinkId=821826
    Invoke-RestMethod
    ConvertFrom-Json
    ConvertTo-Json

REMARKS
    To see the examples, type: "get-help Invoke-WebRequest -examples".
    For more information, type: "get-help Invoke-WebRequest -detailed".
    For technical information, type: "get-help Invoke-WebRequest -full".
    For online help, type: "get-help Invoke-WebRequest -online"
```

==> invoke-webrequest443
