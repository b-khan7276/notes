---
description: Scanning & Enumeration
---

# Scanning & Enumeration

## Nmap Basic Commands

| Protocol           | Commands             |
| ------------------ | -------------------- |
| TCP                | nmap -sT 192.168.1.1 |
| UDP                | nmap -sU 192.168.1.1 |
| SYN -sS            | nmap -sS 192.168.1.1 |
| Aggressive -A      | nmap -A 192.168.1.1  |
| OS Banner Grabbing | nmap -O 192.168.1.1  |
| Verbose            | nmap -v 192.168.1.1  |
| Port               | nmap -p 192.168.1.1  |
|                    |                      |



```bash
nmap -T4 -p- -A 192.168.16.5
```



## Network Scanning

### IP Resolution

```bash
# Resolve domains using the resolveDomains tool
# https://github.com/Josue87/resolveDomains
resolveDomains -d subdomains.txt
```

### Netdiscover

```bash
# Perform an interface-based scan
netdiscover -i eth0

# Perform a range-based scan
netdiscover -r 10.11.1.1/24
```

### Nmap

```bash
# Scan hosts in a network using CIDR notation
nmap -sn 10.11.1.1/24

# Scan hosts in a range
nmap -sn 10.11.1.1-253

# Scan hosts using wildcard notation
nmap -sn 10.11.1.*
```

#### searching for nmap scripts

```bash
ls -la /usr/share/nmap/scripts | grep  -e "ftp" 
```

#### Look for all the nmap scripts

```bash
ls -la /usr/share/nmap/scripts
```

#### scanning the target with script

```bash
nmap -sV -Pn  --script ftp-vsftpd-backdoor 58.65.168.132
```

#### stelth scan

```bash
 sudo nmap -sS -A -T4 -O  -Pn  58.65.168.132
```

### NetBios

```bash
# Perform a NetBios scan
nbtscan -r 10.11.1.1/24
```

### Ping Sweep - Bash

```bash
# Perform a ping sweep using a loop
for i in {1..254} ;do (ping -c 1 172.21.10.$i | grep "bytes from" &) ;done
```

### Ping Sweep - Windows

```bash
# Perform a ping sweep using a loop in Windows
for /L %i in (1,1,255) do @ping -n 1 -w 200 172.21.10.%i > nul && echo 192.168.1.%i is up.
```

```bash
# Additional Scanning Commands

# Perform an ARP scan
arp-scan -l

# Use whatweb to scan a specific IP
whatweb 10.10.10.10

# Perform an Nmap vulnerability scan
nmap -p 21 --script=vuln ip

# Perform a nuclei vulnerability scan
nuclei -u https://google.com -t vulnerabilities

# Perform another ARP scan
arp-scan -l

# Use skipfish with a specified wordlist to scan a target
skipfish -w /usr/share/wordlists/dirb -o report http:10.101.10.1

# Perform a uniscan with specified options
uniscan -u http:10.10.1.1 -wqeds

# Perform a WordPress scan on localhost
wpscan --url localhost

# Perform user enumeration for WordPress on localhost
wpscan -e u --url localhost

# Perform brute force password attack on WordPress on localhost
wpscan -e u --url localhost -P /usr/share/wordlists/metasploit/default_http_password.txt

# Perform brute force attack on WordPress with specified username
wpscan -U admin --url localhost -P /usr/share/wordlists/metasploit/default_http_password.txt
```

### Directory Busting and CMS Scanning

```bash
# Perform a dirb scan with a specified wordlist
dirb http:localhost /usr/share/worldlists/dirb

# Perform a dirb scan with specified file extensions
dirb http:localhost -X php,txt,js,zip,sh,jar,exe
```

#### Hydra

```bash
# Information Required for Hydra Brute Force:

# 1. Login or Wordlist for Usernames - admin
# 2. Password or Wordlist for Passwords - usr/share/wordlists/metasploit/http_default_pass.txt
# 3. IP Address or Domain of the Target - 10.10.10.129
# 4. HTTP Method (POST/GET) - POST
# 5. Path to the Login Page - http://10.10.10.129/secret/wp-login.php
# 6. Request body for Username/Password — log=jkdsakjdbnsa&pwd=dsadasd&wp-submit=Log+In&redirect_to=http%3A%2F%2Fvtcsec%2Fsecret%2Fwp-admin%2F&testcookie=1
# 7. A Way to Identify Failed/Successful Attempts — incorrect

# Format of the Hydra Syntax:
# sudo hydra <Username/List> <IP> <Method> "<Path>:<Request Body>:<Fail or Success Identifier>"

# Example Command:
# sudo hydra -l admin -P /usr/share/wordlists/metasploit/http_default_pass.txt 10.10.10.129 http-post-form "/secret/wp-login.php:log=admin&pwd=^PASS^&wp-submit=Log+In&redirect_to=http%3A%2F%2Fvtcsec%2Fsecret%2Fwp-admin%2F&testcookie=1:F=incorrect"

sudo hydra -l admin -P /usr/share/wordlists/rockyou.txt 10.10.10.129 http-post-form "/secret/wp-login.php:log=admin&pwd=^PASS^&wp-submit=Log+In&redirect_to=http%3A%2F%2Fvtcsec%2Fsecret%2Fwp-admin%2F&testcookie=1:F=incorrect"
```

## Fuzzing

```bash
sudo ffuf -w /usr/share/wordlists/dirb/common.txt -u <https://fccl.com.pk/FUZZ> -fc 403 -p 2
```

#### gobuster

error

```bash
 gobuster dir -u <https://portal.bisemultan.edu.pk>  -w /snap/seclists/current/Discovery/DNS/subdomains-top1million-5000.txt
```

### Shodan

```bash
sudo apt install python3-shodan

shodan init APIKEY 
shodan info 
shodan count wordpress 

shodan host ip    
shodan scan submit ip 

 
```

## Subdomain Enumeration

```bash
# Perform subdomain enumeration using amass
amass enum -brute -d website
```

```
sublist3r -d web.bisemultan.edu.pk
```

## Vul Scanner

```bash
nuclei -u <https://google.com> -t vulnerabilities 
```

Nikto ( Can be busted by blue team )

```bash
nikto  -h google.com
```

##

## Summery&#x20;

```bash


# Network Scanning

# IP resolution
# https://github.com/Josue87/resolveDomains
resolveDomains -d subdomains.txt

# Netdiscover
netdiscover -i eth0
netdiscover -r 10.11.1.1/24

# Nmap
nmap -sn 10.11.1.1/24
nmap -sn 10.11.1.1-253
nmap -sn 10.11.1.*

# NetBios
nbtscan -r 10.11.1.1/24

# Ping Sweep - Bash
for i in {1..254} ;do (ping -c 1 172.21.10.$i | grep "bytes from" &) ;done

# Ping Sweep - Windows
for /L %i in (1,1,255) do @ping -n 1 -w 200 172.21.10.%i > nul && echo 192.168.1.%i is up.

# Additional Scanning Commands

arp-scan -l
whatweb 10.10.10.10

# nmap vul scan
nmap -p 21 --script=vuln ip
nuclei -u https://google.com -t vulnerabilities
arp-scan -l

skipfish -w /usr/share/wordlists/dirb -o report http:10.101.10.1

uniscan -u http:10.10.1.1 -wqeds

wpscan --url localhost
# for user enumeration
wpscan -e u --url localhost
# for brute force password
wpscan -e u --url localhost -P /usr/share/wordlists/metasploit/default_http_password.txt

# bruteforce with username
wpscan -U admin --url localhost -P /usr/share/wordlists/metasploit/default_http_password.txt

# Directory Busting And CMS Scanning

dirb http:localhost /usr/share/worldlists/dirb

dirb http:localhost -X php,txt,js,zip,sh,jar,exe

# Hydra

# Information Required for Hydra Brute Force:-

# 1. Login or Wordlist for Usernames - admin

# 2. Password or Wordlist for Passwords - usr/share/wordlists/metasploit/http_default_pass.txt

# 3. IP Address or Domain of the Target - 10.10.10.129

# 4. HTTP Method (POST/GET) - POST

# 5. Path to the Login Page - http://10.10.10.129/secret/wp-login.php

# 6. Request body for Username/Password — log=jkdsakjdbnsa&pwd=dsadasd&wp-submit=Log+In&redirect_to=http%3A%2F%2Fvtcsec%2Fsecret%2Fwp-admin%2F&testcookie=1

# 7. A Way to Identify Failed/Successful Attempts — incorrect

# Format of the Hydra Syntax:-
# sudo hydra <Username/List> <IP> <Method> "<Path>:<Request Body>:<Fail or Success Identifier>"

sudo hydra -l admin -P /usr/share/wordlists/metasploit/http_default_pass.txt 10.10.10.129 http-post-form "/secret/wp-login.php:log=admin&pwd=^PASS^&wp-submit=Log+In&redirect_to=http%3A%2F%2Fvtcsec%2Fsecret%2Fwp-admin%2F&testcookie=1incorrect:F=incorrect"

# Subdomain enumeration

amass enum -brute -d website

# Vul Scanner
nuclei -u <https://google.com> -t vulnerabilities 

```
