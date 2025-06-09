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
- **A Record**: 13.215.248.232 

## 📸 Screenshots
- [EC2 Dashboard](screenshots/ec2-setup/1-dashboard.png)  
- [Apache Default Page](screenshots/apache-config/2-default-page.png)  
