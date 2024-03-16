# Tools for Information Gaterhing in the Web

This information gathering section is specialized for methods in the web. 

## 1. Passive Information Gathering

In passive information gathering, we do not interact with the target. Therefore, we only use information that is publicly available. 

Well known tools: 

### WHOIS
- Can be used to query databases of domain names, IP addresses and provide information services to users

### Nslookup
- search for a domian name server
- we can ask for informations about hosts and domians
- with <code>-query</code> param we can specify resource records

### dig
- dig gives more detailed informations than nslook up 

The following tools are used for <b>passive subdomian enumeration</b>. This allows us to find subdomians to increase our attack surface. 

### Certificate Databases
- for Example: https://censys.io, https://crt.sh
- Every SSL/TLS Certificate is published in a public assessible log
- can be combined with curl to get a JSON list and parse it into an easy-to-read list.
- OpenSSL kann auch genutzt werden. 
- non-automatic method

### TheHarvester
- Collects emails, names, subdomains, IP addresses and URLs from various public data sources
- Data source can be specified in custom source text file
- Result can be sorted and saved to a file with multiple cat constructs.

The following tools are used for <b>passive infrastructure enumeration</b> 

### Netcraft
- is a convenient site to get information about the infrastructure without having to visit the target site. 