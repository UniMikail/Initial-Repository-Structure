# Server Configuration Documentation
**Last Updated**: [YYYY-MM-DD]

## 1. AWS EC2 Setup
### Instance Details
- **AMI**: Ubuntu 22.04 LTS  
- **Security Group Rules**:  
  ```plaintext
  SSH (22)    : My IP only
  HTTP (80)   : 0.0.0.0/0
  HTTPS (443) : 0.0.0.0/0
  ```

### SSH Access
```bash
shh -i MyFirstKey.pem ubuntu@54.179.182.56
```

## 2. Apache Installation
```bash
sudo apt install apache2 -y
sudo ufw allow 'Apache Full'
```

## 3. DNS Configuration
- **Domain**: [yourdomain.com  ](https://www.detailsrecipes.shop/)
- 
- # Check DNS propagation
##Apache Virtual Host Setup
```bash
<VirtualHost *:80>
    ServerName detailsrecipes.shop
    ServerAlias www.detailsrecipes.shop
    DocumentRoot /var/www/detailsrecipes.shop/public_html
    ErrorLog ${APACHE_LOG_DIR}/detailsrecipes.shop-error.log
    CustomLog ${APACHE_LOG_DIR}/detailsrecipes.shop-access.log combined
</VirtualHost>
```
# Local hosts file test 
```bash
echo "13.215.248.232 detailsrecipes.shop" | sudo tee -a /etc/hosts
## result: 13.215.248.232 detailsrecipes.shop
```

