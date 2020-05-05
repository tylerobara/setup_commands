#Check Hostname

`hostname`

#Set hostname

`hostnamectl set-hostname <your_hostname>`

#Verify firewall settings

`sudo iptables -nL -v --line-numbers`

#Edit the trusted.hosts

`sudo vi /etc/trusted.hosts`

#Edit the target.hosts

`sudo vi /etc/trusted.hosts`

#Edit the exclude.hosts file

`sudo vi /etc/exclude.hosts`

#Enable firewall exceptions without ports

`sudo set_firewall`

#Enable firewall exceptions with ports

`sudo set_firewall -tt -it <Port1,Port2>`

#Show Network Address configuration information

`ip a`

#Show routes

`ip r`

#Show DNS configuration

`cat /etc/resolv.conf`

#Operator Accountability - TCPDump

`sudo tcpdump -n -i <interface> -w <filename.pcap>`

#Active Scanning Method - fping

`fping -a -q -g <NETWORK/CIDR>` #( -a => alives, -q => quiet, -g => generate range from subnet)

#Active Scanning Method - nmap

`sudo nmap -O -iL <range.txt> -oG os_scan.txt` #( -O => OS Scan, -p 1-1024 => Ports 1-1024, -sV => Services)

`sudo nmap -O <ip>`

`diff <yesterday_filename> <today_filename>` #Show changes in alives
