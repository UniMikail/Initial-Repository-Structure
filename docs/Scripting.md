#Check Apache Syntax
```bash
sudo apache2ctl configtest
```
Verify Apache Logs
Error Log:

````bash
sudo tail -n 50 /var/log/apache2/error.log
````
Access Log:

```bash
sudo tail -n 50 /var/log/apache2/access.log
```
#Checking if port 80 is listening
```bash
sudo lsof -i :80
```

