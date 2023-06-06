---
description: Information Gathering (Reconnaissance) summery of the page is written below
---

# Information Gathering (Reconnaissance)

##

## Passive Recon&#x20;



In the field of cybersecurity, passive reconnaissance refers to the process of collecting information about a target without directly engaging with it. This approach can be useful for identifying potential vulnerabilities and attack surfaces. Passive reconnaissance typically involves using publicly available resources to gather information about the target, such as social media, public websites, and search engines.

Some resources that are commonly used for passive reconnaissance include:

* [**BuiltWith.com**](http://builtwith.com/): A website that allows users to see what technologies a website is built with, including server information and content management systems.
* [**Robtex.com**](http://robtex.com/): A website that provides a variety of tools for analyzing domains and IP addresses, including DNS information, network information, and related domains.
* [**Shodan.io**](http://shodan.io/): A search engine that allows users to search for internet-connected devices, including routers, servers, and cameras.
* **Google Dorks**: Specialized search terms that can be used to find specific types of information on Google, such as passwords or vulnerabilities.
* [intodns.com](http://intodns.com)
* [sllabs.com](http://sllabs.com)
* [social-searcher.com](http://social-searcher.com)
* [Securityheaders.com](http://securityheaders.com)
* [archive.org](http://archive.org)
* [https://osintframework.com](https://osintframework.com)
* [FindSubDomains.com](http://findsubdomains.com/)
* Open-source intelligence (OSINT) ([codecademy.com](http://codecademy.com/))
* Recon-ng ([blog.projectdiscovery.io](http://blog.projectdiscovery.io/))
* Maltego ([blog.projectdiscovery.io](http://blog.projectdiscovery.io/))
* The Harvester ([allabouttesting.org](http://allabouttesting.org/))
* Metagoofil ([allabouttesting.org](http://allabouttesting.org/))
* FOCA ([allabouttesting.org](http://allabouttesting.org/))

## Active Recon

Active scanning is a method of testing a system or application by simulating an attack ([danielmiessler.com](http://danielmiessler.com/)). It involves sending requests to a target system and analyzing its responses to identify vulnerabilities ([owasp.org](http://owasp.org/)). Here are some web resources that can help you learn more about active scanning:

### Web based tools

* OWASP Testing Guide ([danielmiessler.com](http://danielmiessler.com))
* OWASP ASVS ([danielmiessler.com](http://danielmiessler.com))
* OWASP ZAP ([danielmiessler.com](http://danielmiessler.com))
* Burp Suite ([danielmiessler.com](http://danielmiessler.com))
* Nessus ([portswigger.net](http://portswigger.net))
* OpenVAS ([portswigger.net](http://portswigger.net))
* Acunetix ([portswigger.net](http://portswigger.net))
* Netsparker ([portswigger.net](http://portswigger.net))
* QualysGuard ([portswigger.net](http://portswigger.net))
* Nexpose ([portswigger.net](http://portswigger.net))
* Retina CS ([portswigger.net](http://portswigger.net))
* AppScan ([portswigger.net](http://portswigger.net))
* WebInspect ([portswigger.net](http://portswigger.net))
* Metasploit Framework: [https://www.metasploit.com/](https://www.metasploit.com/)
* Arachni: No longer supported since Feb. 2020
* Vega: [https://subgraph.com/vega/](https://subgraph.com/vega/)
* Wapiti: [https://wapiti.sourceforge.io/](https://wapiti.sourceforge.io/)
* Nikto: [https://cirt.net/Nikto2](https://cirt.net/Nikto2)

### More active recon tools

* Burp Suite: [https://portswigger.net/burp](https://portswigger.net/burp)
* Nessus: [https://www.tenable.com/products/nessus](https://www.tenable.com/products/nessus)
* OpenVAS: [https://www.openvas.org/](https://www.openvas.org/)
* OWASP ZAP: [https://owasp.org/www-project-zap/](https://owasp.org/www-project-zap/)
* Acunetix: [https://www.acunetix.com/](https://www.acunetix.com/)
* Netsparker: [https://www.netsparker.com/](https://www.netsparker.com/)
* QualysGuard: [https://www.qualys.com/](https://www.qualys.com/)
* Nexpose: [https://www.rapid7.com/products/nexpose/](https://www.rapid7.com/products/nexpose/)
* Retina CS: [https://www.beyondtrust.com/products/retina-network-security-scanner/](https://www.beyondtrust.com/products/retina-network-security-scanner/)
* AppScan: [https://www.hcltech.com/products-and-platforms/security/appscan](https://www.hcltech.com/products-and-platforms/security/appscan)
* WebInspect: [https://www.microfocus.com/en-us/cyberres/application-security/webinspect-dynamic-analysis-dast](https://www.microfocus.com/en-us/cyberres/application-security/webinspect-dynamic-analysis-dast)
* Nmap: [https://nmap.org/](https://nmap.org/)
* Metasploit Framework: [https://www.metasploit.com/](https://www.metasploit.com/)
* Arachni: [http://web.archive.org/web/20220103123855/http://www.arachni-scanner.com/](http://web.archive.org/web/20220103123855/http://www.arachni-scanner.com/)
* Vega: [http://subgraph.com/vega/](http://subgraph.com/vega/)
* Wapiti: [http://wapiti.sourceforge.net/](http://wapiti.sourceforge.net/)
* Skipfish: [http://code.google.com/p/skipfish/](http://code.google.com/p/skipfish/)
* Nikto: [https://cirt.net/Nikto2](https://cirt.net/Nikto2)

## Physical/ Social

#### Location Information

* Satellite images
* Drone recon
* Building layout (badge readers, break areas, security, fencing)

***

#### Job Information

* Employees (name, job title, phone number, manager, etc.)
* Pictures (badge photos, desk photos, computer photos, etc.)

***

#### Web/Host

1. Target Validation
   1. WHOIS, nslookup, dnsrecon
2. Finding Subdomains
   1. Google Fu, dig, Nmap, Sublist3r, Bluto, [crt.sh](http://crt.sh/), ete
3. Fingerprinting
   1. Namp, Weppalyzer, whatweb, buitwith, netcat
4. Data Breaches
   1. HavelBeen Pwned, Breach- Parse, WeLeaklnfo

***

### **Identifying Our Target**

#### Discovering Email Addresses

Websites

1. [https://hunter.io/](https://hunter.io/)
2. [https://phonebook.cz/](https://phonebook.cz/)
3. [https://intelx.io/](https://intelx.io/)
4. [https://www.voilanorbert.com/](https://www.voilanorbert.com/)
5. [https://www.emailhippo.com/](https://www.emailhippo.com/)
6. [https://email-checker.net/](https://email-checker.net/)
7. [https://chrome.google.com/webstore/detail/clearbit-connect-supercha/pmnhcgfcafcnkbengdcanjablaabjplo?hl=en](https://chrome.google.com/webstore/detail/clearbit-connect-supercha/pmnhcgfcafcnkbengdcanjablaabjplo?hl=en)

### **Gathering Breached Credentials with Breach-Parse**

1. [https://github.com/hmaverickadams/breach-parse](https://github.com/hmaverickadams/breach-parse)

### **Hunting Breached Credentials with DeHashed**

1. [https://dehashed.com/](https://dehashed.com/)
2. [https://alternativeto.net/software/dehashed/](https://alternativeto.net/software/dehashed/)
3. [https://hashes.org/](https://hashes.org/)

### **Hunting Subdomains Part 1**

1. sublist3r (kali tool)
2. [https://crt.sh/](https://crt.sh/)
3. [https://github.com/OWASP/Amass](https://github.com/OWASP/Amass)

## Summery of All tools&#x20;



<table><thead><tr><th width="213">Category</th><th>Resources</th></tr></thead><tbody><tr><td><strong>Active Recon</strong></td><td></td></tr><tr><td>OWASP Testing Guide</td><td><a href="https://danielmiessler.com/">https://danielmiessler.com</a></td></tr><tr><td>OWASP ASVS</td><td><a href="https://danielmiessler.com/">https://danielmiessler.com</a></td></tr><tr><td>OWASP ZAP</td><td><a href="https://danielmiessler.com/">https://danielmiessler.com</a></td></tr><tr><td>Burp Suite</td><td><a href="https://danielmiessler.com/">https://danielmiessler.com</a></td></tr><tr><td>Nessus</td><td><a href="https://www.portswigger.net/products/nessus">https://www.portswigger.net/products/nessus</a></td></tr><tr><td>OpenVAS</td><td><a href="https://www.openvas.org/">https://www.openvas.org</a></td></tr><tr><td>Acunetix</td><td><a href="https://www.acunetix.com/">https://www.acunetix.com</a></td></tr><tr><td>Netsparker</td><td><a href="https://www.netsparker.com/">https://www.netsparker.com</a></td></tr><tr><td>QualysGuard</td><td><a href="https://www.qualys.com/">https://www.qualys.com</a></td></tr><tr><td>Nexpose</td><td><a href="https://www.rapid7.com/products/nexpose">https://www.rapid7.com/products/nexpose</a></td></tr><tr><td>Retina CS</td><td><a href="https://www.beyondtrust.com/products/retina-network-security-scanner">https://www.beyondtrust.com/products/retina-network-security-scanner</a></td></tr><tr><td>AppScan</td><td><a href="https://www.hcltech.com/products-and-platforms/security/appscan">https://www.hcltech.com/products-and-platforms/security/appscan</a></td></tr><tr><td>Web Recon</td><td></td></tr><tr><td>Nmap</td><td><a href="https://nmap.org/">https://nmap.org</a></td></tr><tr><td>Metasploit Framework</td><td><a href="https://www.metasploit.com/">https://www.metasploit.com</a></td></tr><tr><td>Arachni</td><td><a href="http://web.archive.org/web/20220103123855/http://www.arachni-scanner.com">http://web.archive.org/web/20220103123855/http://www.arachni-scanner.com</a></td></tr><tr><td>Vega</td><td><a href="http://subgraph.com/vega/">http://subgraph.com/vega/</a></td></tr><tr><td>Wapiti</td><td><a href="http://wapiti.sourceforge.net/">http://wapiti.sourceforge.net/</a></td></tr><tr><td>Nikto</td><td><a href="https://cirt.net/Nikto2">https://cirt.net/Nikto2</a></td></tr><tr><td><strong>Passive Recon</strong></td><td></td></tr><tr><td>BuiltWith.com</td><td><a href="https://builtwith.com/">https://builtwith.com</a></td></tr><tr><td>Robtex.com</td><td><a href="https://robtex.com/">https://robtex.com</a></td></tr><tr><td>Shodan.io</td><td><a href="https://shodan.io/">https://shodan.io</a></td></tr><tr><td>Google Dorks</td><td>Specialized search terms that can be used to find specific types of information on Google</td></tr><tr><td>intodns.com</td><td><a href="https://intodns.com/">https://intodns.com</a></td></tr><tr><td>sllabs.com</td><td><a href="https://www.ssllabs.com/">https://www.ssllabs.com</a></td></tr><tr><td>social-searcher.com</td><td><a href="https://www.social-searcher.com/">https://www.social-searcher.com</a></td></tr><tr><td>Securityheaders.com</td><td><a href="https://securityheaders.com/">https://securityheaders.com</a></td></tr><tr><td>archive.org</td><td><a href="https://archive.org/">https://archive.org</a></td></tr><tr><td>OSINT Framework</td><td><a href="https://osintframework.com/">https://osintframework.com</a></td></tr><tr><td>FindSubDomains.com</td><td><a href="https://www.findsubdomains.com/">https://www.findsubdomains.com</a></td></tr><tr><td><strong>Social/Physical</strong></td><td></td></tr><tr><td>Location Information</td><td>Satellite images, Drone recon, Building layout (badge readers, break areas, security, fencing)</td></tr><tr><td>Job Information</td><td>Employees (name, job title, phone number, manager, etc.), Pictures (badge photos, desk photos, computer photos, etc.)</td></tr><tr><td><strong>Web/Host</strong></td><td></td></tr><tr><td>Target Validation</td><td>WHOIS, nslookup, dnsrecon</td></tr><tr><td>Finding Subdomains</td><td>Google Fu, dig, Nmap, Sublist3r, Bluto, crt.sh, ete</td></tr><tr><td>Fingerprinting</td><td>Nmap, Weppalyzer, whatweb, builtwith, netcat</td></tr><tr><td>Data Breaches</td><td>HaveIBeenPwned, Breach-Parse, WeLeakInfo</td></tr><tr><td>Identifying Our Target</td><td>Discovering Email Addresses, Websites</td></tr><tr><td>Gathering Breached Credentials with Breach-Parse</td><td><a href="https://github.com/hmaverickadams/breach-parse">https://github.com/hmaverickadams/breach-parse</a></td></tr><tr><td>Hunting Breached Credentials with DeHashed</td><td><a href="https://dehashed.com/">https://dehashed.com</a></td></tr><tr><td>Hunting Subdomains Part 1</td><td>sublist3r (kali tool), <a href="https://crt.sh/">https://crt.sh</a>, <a href="https://github.com/OWASP/Amass">https://github.com/OWASP/Amass</a></td></tr></tbody></table>
