Linux Server Configuration 2016/03/11

#Access
- IP adress: 52.27.227.73
- SSH port 2200
- URL: http://ec2-52-27-227-73.us-west-2.compute.amazonaws.com

#Installed software
- Finger
- Apache
- PostgreSQL 9.3
- Fail2ban
- NTP
- libapache2-mod-wsgi
- unattended-upgrades

#Configurations
- Updated/Upgraded server
- Created user 'grader'
- Granted 'grader' sudo privilege
- Setup rsa authentication for 'grader'
- Changed ssh port to 2200
- Disabled root ssh login
- Set time zone to UTC
- Unattended-Upgrades configured to automatically install all stable upgrades
- Configured firewall to allow all outgoing connections, and only allow incoming
on port 2200(SSH), 80 (HTTP), and 123(NTP)
- Configured Apache to use mod_wsgi
- Refactored Catalog app to work on Apache
- Created 'catalog' user and database in Postgres
- 'catalog' user was given no privileges, and ownership of the database
- Hardened system against DDoS attacks using script written by Danny Sheehan
(see resources)
- Enabled fail2ban to block repeated ssh attempts

#Resources
- https://www.ftmon.org/blog/secure-ubuntu-server/
- https://github.com/dannysheehan/ubuntu
- https://discussions.udacity.com/t/project-5-resources/28343
- https://github.com/robertavram/Linux-Server-Configuration
- https://discussions.udacity.com/t/markedly-underwhelming-and-potentially-wrong-resource-list-for-p5/8587

