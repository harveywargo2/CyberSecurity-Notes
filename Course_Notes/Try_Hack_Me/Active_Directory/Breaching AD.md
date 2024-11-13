# References

# Notes

# Commands
Setting DNS on Interface 
~~~
systemd-resolve --interface <interface> --set-dns [IPADDRESS] --set-domain [rootdomain]
~~~

Password Spray Cmd
~~~
python ntlm_passwordspray.py -u <userfile> -f <fqdn> -p <password> -a <attackurl>
~~~

NetCat Listener for RDP
~~~
nc -lvp 389
~~~

tcpdump 
~~~
sudo tcpdump -SX -i <interface> tcp port 389
~~~

Responder
~~~
sudo responder -I <interface>
~~~