# Awesome-HTB-Journey
HTB Journey Starter List <br/>

A list for those who want to own boxes but don't know what to start. <br/>

You can also help me by making pull requests to add some more information

# Table of Contents
==========================================
* [Preparation](#-preparation)
* [Windows Cheatsheet](#windows-cheatsheet)
* [Linux Cheatsheet](#linux-cheatsheet)

## [↑](#table-of-contents) Preparation
==========================================

* [Linux Fundamentals Book](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&cad=rja&uact=8&ved=2ahUKEwie1PuhlJDnAhXZZSsKHQfLBioQFjAAegQIBhAB&url=http%3A%2F%2Flinux-training.be%2Flinuxfun.pdf&usg=AOvVaw1x8_hp3Va5GA-f7IGeY4vv) <br/>
        This is one of the best starter kits for everyone who wants to be familiar with linux

* [linuxzoo](https://linuxzoo.net/) <br/>
        To practice very basics
 
* [Python Programming](https://www.tutorialspoint.com/python/index.htm) <br/>
        Programming is the key in computer field and python make it easier :)
* [Damn Vulnerable Web Application (DVWA)](http://www.dvwa.co.uk/) <br/>
        Basic Web Attacks Will be Applied in most linux machines. Read tutorials how to exploit security flaws in DVWA

* [Basic Tmux Tutorial](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&cad=rja&uact=8&ved=2ahUKEwjV0vykk5DnAhWfgUsFHWMXDmAQyCkwAHoECAsQBA&url=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DLqehvpe_djs&usg=AOvVaw2loDz-oLBjGTTkISmE5d6G)
* [Overthewire: Wargames](https://overthewire.org/wargames/)

## [↑](#table-of-contents)Windows Cheatsheet
==========================================
### Enumeration
#### Basic Info Scan
* `nmap -sV -sC -o machine.nmap 10.10.x.x`
Users and Domain Enumeration
* `enum4linux ip`<br/>

#### Execute PS Command as another user
---
```powershell
$username = 'user';
$password = 'password';
$securePassword = ConverTo-SecureString $password -AsPlainText -Force;
$credential = New-Object System.Management.Automation.PsCredential("$env:WORKGROUP\$username",$securePassword);
$session = New-PSSession -Credential $credential;
Invoke-Command -Session $session -Script {whoami}
```
---
#### Active Directory
* `ldapsearch -h 10.10.10.x -x -b "DC=domain,DC=local" "(objectClass=User)"`
* [Impacket](https://gist.github.com/TarlogicSecurity/2f221924fef8c14a1d8e29f3cb5c5c4a)
#### File Systems

##### SMB Enumeration
* `smbmap.py -H 10.10.x.x`
* `mount -t cifs -o username='username',password='password' //10.10.10.182/Data /mnt`

<script src="https://www.hackthebox.eu/badge/4314"></script>

