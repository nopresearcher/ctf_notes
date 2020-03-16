# linux privesc
https://blog.g0tmi1k.com/2011/08/basic-linux-privilege-escalation/

## What's the distribution type? What version?
```
cat /etc/issue
cat /etc/*-release
  cat /etc/lsb-release      # Debian based
  cat /etc/redhat-release   # Redhat based
```
## What's the kernel version? Is it 64-bit?
```
cat /proc/version
uname -a
uname -mrs
rpm -q kernel
dmesg | grep Linux
ls /boot | grep vmlinuz-
```
## What can be learnt from the environmental variables?
```
cat /etc/profile
cat /etc/bashrc
cat ~/.bash_profile
cat ~/.bashrc
cat ~/.bash_logout
env
set
```
## Is there a printer?
```
lpstat -a
```
## Applications & Services
### What services are running? Which service has which user privilege?
```
ps aux
ps -ef
top
cat /etc/services
```
### Which service(s) are been running by root? Of these services, which are vulnerable - it's worth a double check!
```
ps aux | grep root
ps -ef | grep root
```
### What applications are installed? What version are they? Are they currently running?
```
ls -alh /usr/bin/
ls -alh /sbin/
dpkg -l
rpm -qa
ls -alh /var/cache/apt/archivesO
ls -alh /var/cache/yum/
```
### Any of the service(s) settings misconfigured? Are any (vulnerable) plugins attached?	
```
cat /etc/syslog.conf
cat /etc/chttp.conf
cat /etc/lighttpd.conf
cat /etc/cups/cupsd.conf
cat /etc/inetd.conf
cat /etc/apache2/apache2.conf
cat /etc/my.conf
cat /etc/httpd/conf/httpd.conf
cat /opt/lampp/etc/httpd.conf
ls -aRl /etc/ | awk '$1 ~ /^.*r.*/
```

## What jobs are scheduled?

```
crontab -l
ls -alh /var/spool/cron
ls -al /etc/ | grep cron
ls -al /etc/cron*
cat /etc/cron*
cat /etc/at.allow
cat /etc/at.deny
cat /etc/cron.allow
cat /etc/cron.deny
cat /etc/crontab
cat /etc/anacrontab
cat /var/spool/cron/crontabs/root
```
## Any plain text usernames and/or passwords?
```
grep -i user [filename]
grep -i pass [filename]
grep -C 5 "password" [filename]
find . -name "*.php" -print0 | xargs -0 grep -i -n "var $password"   # Joomla
```
## Communications & Networking
### What NIC(s) does the system have? Is it connected to another network?
```
/sbin/ifconfig -a
cat /etc/network/interfaces
cat /etc/sysconfig/network
```
### What are the network configuration settings? What can you find out about this network? DHCP server? DNS server? Gateway?
```
cat /etc/resolv.conf
cat /etc/sysconfig/network
cat /etc/networks
iptables -L
hostname
dnsdomainname
```
### What other users & hosts are communicating with the system?
```
lsof -i
lsof -i :80
grep 80 /etc/services
netstat -antup
netstat -antpx
netstat -tulpn
chkconfig --list
chkconfig --list | grep 3:on
last
w
```
### Whats cached? IP and/or MAC addresses
```
arp -e
route
/sbin/route -nee
```
### Is packet sniffing possible? What can be seen? Listen to live traffic
```
tcpdump tcp dst 192.168.1.7 80 and tcp dst 10.5.5.252 21
```