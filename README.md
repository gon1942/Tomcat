# docker-ubuntu-tomcat9
Docker container (Ubuntu 20.04 &amp; Tomcat 9)

### Installed software:
* Ubuntu 20.04
* OpenJDK (11.0.7)
* Tomcat (9.0.31-1)


### Notes
***
Tomcat management console has been defaulted to admin:admin. If you would like to change it to something else change the following:
* TOM_USER=admin
* TOM_PASS=admin


```
docker create \
  --name=ubuntu-tomcat9 \
  -e TOM_USER=admin \
  -e TOM_PASS=admin \
  -e TZ=America/Los_Angeles \
  -p 8080:8080 \
  -v /path/to/webapps:/srv/webapps \
  -v /path/to/logs:/srv/logs \
  -v /path/to/opt:/opt \
  --restart unless-stopped
```
