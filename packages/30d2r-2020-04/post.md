---
layout: post
title: "30D2R - April: Windows Exploitation Basics"
date: 2020-08-25
categories: ['30D2R']
---
This post is a part of my [30 Days 2 Root](https://dev.to/sshad0w/30-days-to-root-challenge-introduction-3idp) challenge series.
Essentially, I am trying to learn the basics of a different facet of cybersecurity each month. [Click here](https://dev.to/sshad0w/30-days-to-root-challenge-introduction-3idp) to learn about how the challenge works, or tell me what I should study next!


Windows. There's literally no way you've never heard of the operating system before. Over a billion systems worldwide run Windows. This includes everything from Everyday devices like personal computers and phones, to business infrastructure like coca cola freestyle machines and point of sales machines like card readers, all the way to critical infrastructure like power grids and water filtration center infrastructure. 

Point is, the world is dominated by this operating system, so it'd better be secure.

This is why I decided to pull back the pane on Windows in April. 

### File sharing

When it comes to Windows, there are a multitude of options available for sharing files over a network. Some of the most common ways are FTP and SMB. Although there are many other ways, learning the basics of these two protocols will help you understand more complex services like SAMBA and CIFS.

### File Transfer Protocol

The File Transfer Protocol or FTP is a simple client/server architecture that allows one computer to stand up a server with files while other computers with the protocol client infrastructure installed can interact with this server. Although FTP is on both *nix systems and Windows systems, it is still a very common way to share files on a LAN or WAN. 

There is a feature called "anonymous login" which is colloquially referred to as "FTP anon". This allows anyone who has access to the  

### Server Message Block

Server Message Block is a versatile and powerful windows 
staple when it comes to file sharing. SMB can be used to print, send files within networks, and editing files as a group. This is done by using trusts between computers within networks. These trusts can be abused to exploit the relationships between these computers, leak information, and possibly escalate privileges. Tools like Smbmap and Smbclient can help facilitate leveraging this protocol.


### Remote control without shells

Often times, these tools aren't even special "Hacker tools". These are the same tools being used by administrators that the hackers just use to their advantage. These types of things are much harder to detect.

Windows remote functionality is no different. 

Once the hacker penetrates the network and gains the credentials needed to to authenticate, the hacker uses RDP to watch the computers silently in the background, and possibly control them when no one is watching. This is why there should always be strong password and extensive logging if the service needs to be used. If the service isn't required in the organization, turn the feature off and make sure the port remains closed.

### Remote Desktop Protocol

Imagine you're a manager in an corporate enterprise. No matter what your business is, some part of your enterprise will consist of a department that many people have to be on computers in. 

You'd need to know who's doing what, like who's actually doing work, who's following security protocols, and who has been away from their desk for too long. The IT help desk may even need to see the screens of the employees 

These same tools can be used and leveraged by the attacker.
When the attacker uses RDP, they may pretend to be an administrator, or simply misuse this function for nefarious purposes. Mitigation is much more difficult because it typically means a human has to verify the validity of each RDP session, because the organization may use RDP for legitimate purposes.


### Remote Procedure Call

Much like RDP, RPC is a client server feature in Windows machines that allow one computer to call a procedure in another machine. This is another tool that is typically used by Sysadmins but hijacked by hackers. It doesn't have a complete GUI like RDP, but it is just as powerful and can be abused by people with malicious intent.

### Evil Winrm 

Windows also has a remote management protocol that functions very similarly to SSH. Even though windows does support SSH, this is another tool designed for server administrators that is often abused by attackers

This is known as [WinRM](https://docs.microsoft.com/en-us/windows/win32/winrm/portal) (Windows remote management). In July of 2014, OscarAkaElvis released [EvilWinRM](https://github.com/Hackplayers/evil-winrm) on Github. This easily allowed pentesters to abuse this feature to remotely connect and control computers using the same protocol that SysAdmins do.



### Powershell

Powershell is the native scripting language of the Windows operating system. Powershell is the Windows version of Bash. This language can do anything so becoming well versed in this language would be a powerful skill that would make anyone an extremely effective Windows hacker. Not only this, but learning this language means that no outside tools based on python or ruby have to be put on the computer if the attacker can build them in Powershell. This allows the attacker to be much more stealthy. 

### Privesc 

There are [countless ways to skin the cat that is Windows privilege escalation.](https://book.hacktricks.xyz/windows/windows-local-privilege-escalation) The most common ways are using [syskey](https://krebsonsecurity.com/tag/syskey/) attacks, [getsystem](https://powersploit.readthedocs.io/en/latest/Privesc/Get-System/), or exploiting executable files. More advanced techniques are things like [DLL hijacking](https://trustfoundry.net/what-is-dll-hijacking/), [Binary path escalation](https://owasp.org/www-community/attacks/Binary_planting) or deploying a [Kernel exploit](https://kakyouim.hatenablog.com/entry/2020/05/27/010807).


As you can see, most if not all of Windows hacking techniques  are simply using its functionality against itself. Most of the tools and techniques I showed you today did not involve a special method that only hackers use, I showed you the same tools and protocols used by Blue teamers and regular users of Windows use every single day. The only thing that changed was the intent on how they were used. Once again, this goes to show that [hacking is a mentality, not a skill](https://www.instagram.com/p/CAod9wkjduf/). 





