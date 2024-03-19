# Tools for Information Gaterhing in the Web

This information gathering section is specialized for methods in the web. 

## 1. Passive Information Gathering

In passive information gathering, we do not interact with the target. Therefore, we only use information that is publicly available. 

Well known tools: 

### WHOIS
- Can be used to query databases of domain names, IP addresses and provide information services to users

### Nslookup (DNS)
- search for a domian name server
- we can ask for informations about hosts and domians
- with <code>-query</code> param we can specify resource records

### dig (DNS)
- dig gives more detailed informations than nslook up 

### Passive subdomain enumeration

The following tools are used for <b>passive subdomian enumeration</b>. This allows us to find subdomians to increase our attack surface. 

#### Certificate Databases
- for Example: https://censys.io, https://crt.sh
- Every SSL/TLS Certificate is published in a public assessible log
- can be combined with curl to get a JSON list and parse it into an easy-to-read list.
- OpenSSL kann auch genutzt werden. 
- non-automatic method

#### TheHarvester
- Collects emails, names, subdomains, IP addresses and URLs from various public data sources
- Data source can be specified in custom source text file
- Result can be sorted and saved to a file with multiple cat constructs.

### Passive infrastructure identification 
The following tools are used for <b>passive infrastructure identification</b> 

### Netcraft
- is a convenient site to get information about the infrastructure without having to visit the target site. 

### Wayback machine
- site to access serveral versions of a website
- find websites at a specific point of time
- same is possible with waybackurls (just for urls)
- useful to detect the usage of vulnerable plugins and other weak points

## 2. Active Information Gathering

### Active Infrastructure Identification

- when the discover the web server, it gives important informations about the os 

#### Usage of Curl

- First of all we can look into response http headers
- usage of curl to achieve this
- fields of special interest:
    - X-Powered-y: this header can tell us what the webb app is using
    - Cookies: each technology has its own specific cookies

#### WhatWeb
https://github.com/urbanadventurer/WhatWeb

- WhatWeb detects several web technologies like CMS, analytic packages, JS Libraries, web servers and embedded devices

#### Wappalyzer
- same functionality as whatweb but it is installed as browser plugin

#### WafW00f

https://github.com/EnableSecurity/wafw00f

- web application firewall fingerprinting tool
- sends request to webserver to detect the used security solution

#### Aquatone

https://github.com/michenriksen/aquatone

- Tool for automatic and visual inspection
- Gaining quick overview of HTTP-based attack surface
- Visits configured ports with headless browser and screenshots all sites
- Result is stored in aquatone_report.html
- Contains screenshots, reponse headers, identified technologies

### Active Subdomian Enumeration

TODO

