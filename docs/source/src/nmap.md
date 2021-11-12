# NMAP

Suffixes : 
* -sV : affiche la version des services existants sur les ports
* -sC : affiche les scripts par défaut qui sont activés sur les ports

Scan simple et rapide : 
* sudo nmap -sS -T5 <ip>

Exemples : 
* N°1 : TryHackMe -> [Ice Room](https://tryhackme.com/room/ice)

    ```$ sudo nmap -sS -Pn -sV 10.10.188.70```

* N°2 : TryHackMe -> [Ice Room](https://tryhackme.com/room/ice)

    ```$ sudo nmap -sS -sC 10.10.188.70```

* N°3 : TryHackMe -> [Kenobi Room](https://tryhackme.com/room/kenobi)

    ```nmap -p 445 --script=smb-enum-shares.nse,smb-enum-users.nse <ip>```
    ```nmap -p 139 --script=smb-enum-shares.nse,smb-enum-users.nse <ip>```

* N°4 : TryHackMe -> [Blue Room](https://tryhackme.com/room/blue)
    ```nmap -sV -vv --script vuln 10.10.186.248```

    PORT      STATE SERVICE            REASON  VERSION
    135/tcp   open  msrpc              syn-ack Microsoft Windows RPC
    139/tcp   open  netbios-ssn        syn-ack Microsoft Windows netbios-ssn
    445/tcp   open  microsoft-ds       syn-ack Microsoft Windows 7 - 10 microsoft-ds (workgroup: WORKGROUP)
    **3389/tcp  open  ssl/ms-wbt-server? syn-ack**
    |_ssl-ccs-injection: No reply from server (TIMEOUT)
    | rdp-vuln-ms12-020: 
    |   VULNERABLE:
    |   MS12-020 Remote Desktop Protocol Denial Of Service Vulnerability
    |     State: VULNERABLE
    |     IDs:  CVE:CVE-2012-0152
    |     Risk factor: Medium  CVSSv2: 4.3 (MEDIUM) (AV:N/AC:M/Au:N/C:N/I:N/A:P)
    |           Remote Desktop Protocol vulnerability that could allow remote attackers to cause a denial of service.
    |           
    |     Disclosure date: 2012-03-13
    |     References:
    |       http://technet.microsoft.com/en-us/security/bulletin/ms12-020
    |       https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0152
    |   
    |   MS12-020 Remote Desktop Protocol Remote Code Execution Vulnerability
    |     State: VULNERABLE
    |     IDs:  CVE:CVE-2012-0002
    |     Risk factor: High  CVSSv2: 9.3 (HIGH) (AV:N/AC:M/Au:N/C:C/I:C/A:C)
    |           Remote Desktop Protocol vulnerability that could allow remote attackers to execute arbitrary code on the targeted system.
    |           
    |     Disclosure date: 2012-03-13
    |     References:
    |       http://technet.microsoft.com/en-us/security/bulletin/ms12-020
    |_      https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0002
    49152/tcp open  msrpc              syn-ack Microsoft Windows RPC
    49153/tcp open  msrpc              syn-ack Microsoft Windows RPC
    49154/tcp open  msrpc              syn-ack Microsoft Windows RPC
    49158/tcp open  msrpc              syn-ack Microsoft Windows RPC
    49159/tcp open  msrpc              syn-ack Microsoft Windows RPC


