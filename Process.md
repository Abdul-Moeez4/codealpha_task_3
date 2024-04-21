
# Snort/Starting intrusion detection

A brief description on code_alpha's task 2 regarding the use of snort in intrusion detection systems


## Deployment

To deploy this project run

- First download/extract the snort-2.9.20.tar.gz file

- type in the command sudo nano /etc/snort/rules/local.rules

you should get something like this:

$Id: local.rules,v 1.11 2004/07/23 20:15:44 bmc Exp $

LOCAL RULES

This file intentionally does not come with signatures.  Put your local
 additions here.

- here is where you will put in your own rules:

alert icmp any any -> $HOME_NET any (msg:"ICMP PING DETECTED"; sid:100001; rev:1;)

alert tcp any any -> $HOME_NET 22 (msg:"SSH AUTHENTICATION ATTEMPT"; sid:100002; rev:1;)


You will then put in the command/instructions as follows:

sudo snort -q -1 /var/log/snort -i enp0s3 -A console -c /etc/snort/snort.conf

- Use your other machine to ping the ip address of the machine you ran this command in and you should see alerts coming in through


-For further understand, watch this video i have created talking all on how to operate snort:
https://www.linkedin.com/posts/abdul-moeez-siddiqui-913578279_cybersecurity-networkdetection-snort-ugcPost-7183053655468605440-Ykgh?utm_source=share&utm_medium=member_desktop








## Authors

- Abdul Moeez Siddiqui (https://github.com/Abdul-Moeez4)



## Screenshots

![App Screenshot](https://i.im.ge/2024/04/21/ZaEqny.Screenshot-2024-04-21-114645.png)

![App Screenshot](https://i.im.ge/2024/04/21/ZaEdxJ.Screenshot-2024-04-21-114352.png)

