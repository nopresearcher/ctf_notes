# nmap enumeration
nmap -sV -Pn -vv -p 22 --script=ssh2-enum-algos,ssh-hostkey,ssh-auth-methods -oA <ip> <ip>


# metasploit
msfconsole 
use modules/auxiliary/scanner/ssh/ssh_enumusers 
set RHOSTS 192.168.10.59
set THREADS 10 
set USER_FILE /usr/share/wordlists/metasploit/unix_users.txt 
run 