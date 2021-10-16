# hack-the-box-strategies
Strategies for HackTheBox / Red Teaming

## Recon

### All Platforms

* nmap (Typically using the following flags `sudo nmap -sS -sV -sC -A -Pn -p- hostname`)

### Linux
Note these are based on common vulnerabilities found within HTB machines. Experience has shown that foothold for linux boxes is highly variable compared to windows counterparts and thus enumeration often needs to be much more thorough.

* Port 22 SSH
	* ssh-user-enum (msfconsole)
* Port 80/8080/443/8443 Web Server
	* nikto
	* dirsearch
	* source code review (if running a web service with retrievable JS/HTML)

* Port 111 / 2049 NFS
	* showmount
	* smb-enum

### Windows

* Port 135 / 445 RPC
	* unauthenticated RPC test
	* test to enumerate environment with valid creds
## Exploitation / Foothold

### All Platforms
* searchsploit
* msfconsole search function
* sploitus

## Useful tools
* nc/netcat/socat - tunneling
* GTFObins - tunneling / shell exploitation
* linPEAS - Privesc
* LES - Privesc
* Traitor - Privesc
* chisel - tunneling w/ ability to port forward easily
* plink - like chisel except for windows
* crackmapexec - password spraying and user enumeration for AD. Can be used to execute remote commands as well.
* https://rahmatnurfauzi.medium.com/windows-privilege-escalation-scripts-techniques-30fa37bd194#:~:text=Windows%2Dprivesc%2Dcheck%20is%20standalone,local%20apps%20(e.g.%20databases)

https://github.com/Hackplayers/evil-winrm