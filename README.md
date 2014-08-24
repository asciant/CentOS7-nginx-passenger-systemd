CentOS7-nginx-passenger-systemd
===============================

CentOS 7 systemd (systemctl) file to use with nginx and Phusion Passenger

Can be used on CentOS 7 after compiling nginx through the `passenger-install-nginx-module` installer.

Save file to:

    /lib/systemd/system/nginx.service

Use commands like:

    sudo systemctl start nginx.service
    sudo systemctl enable nginx.service

Status:

    nginx.service - The nginx HTTP and reverse proxy server
       Loaded: loaded (/usr/lib/systemd/system/nginx.service; enabled)
       Active: active (running) since Sun 2014-08-24 16:55:36 EST; 22min ago
     Main PID: 2745 (nginx)
       CGroup: /system.slice/nginx.service
               ├─2727 PassengerWatchdog
               ├─2730 PassengerHelperAgent
               ├─2735 PassengerLoggingAgent
               ├─2745 nginx: master process /opt/nginx/sbin/nginx
               └─2747 nginx: worker process
    
    Aug 24 16:55:36 vps.mydomain.com nginx[2706]: nginx: the configuration file /opt/nginx/conf/nginx.conf syntax is ok
    Aug 24 16:55:36 vps.mydomain.com nginx[2706]: nginx: configuration file /opt/nginx/conf/nginx.conf test is successful
    Aug 24 16:55:36 vps.mydomain.com systemd[1]: Failed to read PID from file /opt/nginx/logs/nginx.pid: Invalid argument
    Aug 24 16:55:36 vps.mydomain.com systemd[1]: Started The nginx HTTP and reverse proxy server.
  
