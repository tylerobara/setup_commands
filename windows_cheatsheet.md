#Change Hostname from CMD

`wmic computersystem where name="%computername%" call rename name="<your_hostname>"`

#Start the Firewall

`net start "windows defender firewall"`

#Enable the Windows Firewall Profiles

`netsh advfirewall set allprofiles state on`

#Force all profiles to block all inbound traffic

`netsh advfirewall set allprofiles firewallpolicy blockinboundalways,allowoutbound`

#Remove all firewall exceptions

`netsh advfirewall firewall delete rule name=all`

#Remove a firewall exception called "Samba Stuff"

`netsh advfirewall firewall delete rule name="Samba Stuff" (dir=<in/out)`

#Adding Exceptions

`netsh advfirewall firewall add rule name=<name> dir=in action=<allow/block> protocol=<protocol> localport=<port> remoteip=<IP>`
`netsh advfirewall firewall add rule name=<name> dir=out action=<allow/block> protocol=<protocol> localport=<port> remoteip=<IP>`

#Examples

#Allow SMB from 10.0.0.100

`netsh advfirewall firewall add rule name="SMB in" dir=in action=allow protocol=tcp localport=445 remoteip=10.0.0.100`

#Allow
