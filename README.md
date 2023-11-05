# module-05
Cloud & Infrastructure as Service Basics with DigitalOcean
---------------------------------------------
Setup Server on DigitalOcean
1. created new project on DigitalOcean named "bootcamp"
2. created droplet: FRA1, ubuntu 23.10, shared CPU, regular SSD. Added public ssh key.
3. added firewall to droplet: inbound Port 22, my online IPv4
4. tested ssh connection from local to droplet with ssh root@"dopletIPv4"
5. apt update
6. apt install openjdk-8-jre-headless
---------------------------------------------

Deploy and run application artifact on droplet
1. pulled example project "java-react-example" 
2. build application with "gradle build"
3. scp "local_file" root@"dropletIPv4":"path"
4. on droplet: run application java -jar java-react-example.jar & (start app in background)
5. added port of application to firewall (Port 7071)
6. tested connection in browser "dropletIPv4":7071 (took a bit a first, worked fine after a minute)
---------------------------------------------

Create and configure a Linux user on a cloud server
1. adduser "username"
2. adduser "username" sudo (added user to group sudo)
3. su - "username"
4. tested sudo apt update
5. added pubkey also for new user in .ssh/authorized_keys and tested ssh "username"@"dropletIPv4"
---------------------------------------------
Reference: DevOps Bootcamp and TWN
