Click on the cloudera image and click settings Click on Network -> Adapter 1(by default have attached to as NAT) -> Advanced -> Port Forwarding Add a new entry (click on + to add) with the following settings:

Host Port: 1111, Guest Port: 22, leave the host IP and guest IP blank

Connect from your Mac cmd shell using the following

ssh -p 1111 cloudera@localhost

At Ubuntu 18.04 additionally install ssh and reboot

sudo apt-get install openssh-server
