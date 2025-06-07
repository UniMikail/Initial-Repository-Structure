## AWS EC2 Configuration
**Instance Details**:
- AMI: Ubuntu 22.04 LTS
- Type: t2.micro
- Public IP: 54.179.182.56
- Security Group Rules: [See ScreenShot2](docs/screenshots/Screenshot2.png)

**Key Commands**:
```bash
shh -i MyFirstKey.pem ubuntu@54.179.182.56
sudo apt update && sudo apt upgrade -y
sudo apt install -y git tree ufw


