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
# Common Issues & Solutions
## SSH Connection Failed
**Error**: `Permission denied (publickey)`  
**Fix**:  
```bash
chmod 400 ~/.ssh/MyFirstKey.pem  # Set proper permissions
```

## Apache Not Serving Pages
**Error**: 403 Forbidden  
**Fix**:  
```bash
sudo chown -R www-data:www-data /var/www/html
```

## SSL Certificate Renewal
```bash
sudo certbot renew --dry-run
```
