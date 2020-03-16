
## Enumeration

### TCP

```
```

### UDP

```
```

### Nikto

```
```

### Dirb\GoBuster

```
```

### WebDav

```
```

### CMS

```
```

### SMB

```
```

### SNMP

```
```

### DB

```
```

### Other

```
```

- - - -

## Exploitation

* Service Exploited: 
	* 
* Vulnerability Type:
	* 
* Exploit POC:
	* 

**Description:** 


**Discovery of Vulnerability**


**Exploit Code Used**

```
```

**Proof\Local.txt File**

		- [ ] Screenshot with ifconfig\ipconfig
		- [ ] Submit proof

- - - -

## Post Exploitation

### Script Results

```
```

### Host Information

* Operating System
	* 
* Architecture
	* 
* Domain
	* 
* Installed Updates
	* 

### File System

**Writeable Files\Directories**



**Directory List**


### Running Process List


### Installed Applications


### Users


### Groups


### Network

**IPConfig\IFConfig**

```
```

**Network Processes**

```
```

**ARP**

```
```

**DNS**

```
```

**Route**

```
```


### Scheduled Jobs


- - - -

## Priv Escalation

* Service Exploited: 
	* 
* Vulnerability Type:
	* 
* Exploit POC:
	* 

**Description:** 


**Discovery of Vulnerability**


**Exploit Code Used**

```
```

**Proof\Local.txt File**

		- [ ] Screenshot with ifconfig\ipconfig
		- [ ] Submit proof

- - - -

## Goodies

### Hashes


### Passwords


### Proof \ Flags \ Other


## Software Versions

**Software Versions**


**Potential Exploits**


## Log Book


- - - -

## Methodology

#### Network Scanning

		- [ ]  nmap -sn 10.11.1.*
		- [ ]  nmap -sL 10.11.1.*
		- [ ]  nbtscan -r 10.11.1.0/24
		- [ ]  smbtree

#### Individual Host Scanning

		- [ ]  nmap  --top-ports 20 --open -iL iplist.txt
		- [ ]  nmap -sS -A -sV -O -p- ipaddress
		- [ ]  nmap -sU ipaddress

#### Service Scanning

    **WebApp**
			- [ ]   Nikto
			- [ ]   dirb
			- [ ]   dirbuster
			- [ ]   wpscan
			- [ ]   dotdotpwn
			- [ ]   view source 
			- [ ]   davtest\cadevar
			- [ ]   droopscan
			- [ ]   joomscan
			- [ ]   LFI\RFI Test
      
    **Linux\Windows**
			- [ ]   snmpwalk -c public -v1 ipaddress 1
			- [ ]   smbclient -L //ipaddress
			- [ ]   showmount -e ipaddress port
			- [ ]   rpcinfo
			- [ ]   Enum4Linux
    
    **Anything Else**
			- [ ]   nmap scripts (locate *nse* | grep servicename)
			- [ ]   hydra
			- [ ]   MSF Aux Modules
			- [ ]   Download the software

#### Exploitation

		- [ ]   Gather Version Numbes
		- [ ]   Searchsploit
		- [ ]   Default Creds
		- [ ]   Creds Previously Gathered
		- [ ]   Download the software

#### Post Exploitation

    **Linux**
			- [ ]   linux-local-enum.sh
			- [ ]   linuxprivchecker.py
			- [ ]   linux-exploit-suggestor.sh
			- [ ]   unix-privesc-check.py

    **Windows**
			- [ ]   wpc.exe
			- [ ]   windows-exploit-suggestor.py
			- [ ]   windows_privesc_check.py
			- [ ]  	windows-privesc-check2.exe

#### Priv Escalation
    - [ ]  acesss internal services (portfwd)
    - [ ]  add account

**Windows**
    - [ ]  List of exploits

**Linux**
    - [ ]  sudo su 
    - [ ]  KernelDB
    - [ ]  Searchsploit

#### Final
    - [ ]  Screenshot of IPConfig\WhoamI
    - [ ]  Copy proof.txt
    - [ ]  Dump hashes 
    - [ ]  Dump SSH Keys
    - [ ]  Delete files

- - - -