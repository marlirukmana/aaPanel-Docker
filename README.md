aaPanel Docker Deployment

The docker image is officially released by aaPanel
Currently x86_64 and ARM architecture platforms are available for download

Maintained by: aaPanel⁠

图标⁠

fresh tag means that the panel is installed but the base lib is not installed, and the installation of the first software will be slower
lib tag is to install the panel and the basic library, the installation using this mirror to install the software is faster
lnmp tag is to install the panel and the basic library, and the integration LNMP is integrated【Nginx1.22+MySQL5.7+PHP7.4】*arm tab is【MySQL5.6】
lamp tag is to install the panel and the basic library, and the integration LAMP is integrated【Apache2.4+MySQL5.7+PHP7.4】*arm tab is【MySQL5.6】
How to use
```
docker run -d -p 8886:7800 -p 22:21 -p 443:443 -p 80:80 -p 889:888 -v ~/website_data:/www/wwwroot -v ~/mysql_data:/www/server/data -v ~/vhost:/www/server/panel/vhost aapanel/aapanel:lib
```
Now you can access aaPanel at http://youripaddress:8886/⁠

from your host system.

Default installation entry:aapanel
Default username:aapanel
Default password:aapanel123
Default root password:aapanel123

Port usage analysis

Control Panel : 7800
Phpmyadmin : 888

Dir usage analysis
```
Website data : /www/wwwroot
Mysql data : /www/server/data
Vhost file : /www/server/panel/vhost
```
Note: after the deployment is complete, please immediately modify the user name and password in the panel settings and add the installation entry

refer to https://hub.docker.com/r/aapanel/aapanel
