# Use dictionary
fcrackzip -v -D -u -p /usr/share/wordlists/rockyou.txt password.zip 

# brute force based on character length
fcrackzip -v -l 4-8 -u password.zip 