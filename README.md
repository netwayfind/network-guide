# network-guide

identify yourself
- what is your hostname?
  - hostname
- what is your local IP?
  - Windows: ```ipconfig```
  - Linux: ```ifconfig``` or ```ip addr```
- what is your public IP address?
  - Open web browser, search for "what is my ip"
  - ```curl https://ifconfig.me/```
  - ```curl https://checkip.amazonaws.com```

what do you have
- network ports
  - Windows: ```netstat -nao```
  - Linux: ```netstat -ntlp``` or ```ss -ntlp```
  
check DNS
- Open web browser, go to https://dnsleaktest.com/
- Use default DNS
  - ```nslookup www.google.com```
- Use specific DNS server
  - Google DNS: ```nslookup www.google.com 8.8.8.8```
  - CloudFlare DNS: ```nslookup www.google.com 1.1.1.1```

identify routes
- routing table
  - Windows: ```route print```
  - Linux: ```ip route```
- test outbound routes
  - Windows: ```tracert [host]```
  - Linux: ```traceroute [host]```

identify your neighbors
- same subnet
  - Windows: ```arp -n```
  - Linux: ```ip neigh```

orient yourself on the Internet
- ping landmarks
  - Google DNS: ```ping 8.8.8.8```
  - CloudFlare DNS: ```ping 1.1.1.1```
  
look for hosts
- must have permission to perform activity
- scan specific host
  - ```nmap [IP address]```
- scan specific network
  - ```nmap [network]/[CIDR]```
    - for example ```nmap 192.168.0.0/24```
  
