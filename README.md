
# 🛠️ SSH and Pterodactyl Panel Installation Guide

![Header Image](https://via.placeholder.com/1200x400.png?text=SSH+%26+Pterodactyl+Installation+Guide)

This guide provides a step-by-step walkthrough for setting up **SSH** and installing the **Pterodactyl Panel**, a game server management tool.

---

## 📌 Introduction

🔑 **SSH (Secure Shell)** enables secure remote server access.  
🎮 **Pterodactyl Panel** allows you to manage game servers with an intuitive web interface.

This guide covers:  
1. Installing and configuring **SSH**.  
2. Installing and setting up **Pterodactyl Panel**.  
3. Firewall and SSL configuration for security.

![Illustration](https://via.placeholder.com/800x400.png?text=Secure+Your+Server+Today)

---

## 🔒 SSH Installation Steps

### 1. Install OpenSSH Client
Run the following command to install the SSH client:
```bash
sudo apt install openssh-client
```

### 2. Install OpenSSH Server
Install the SSH server to enable remote access:
```bash
sudo apt install openssh-server
```

### 3. Restart the SSH Service
Restart the SSH service to apply changes:
```bash
sudo systemctl restart sshd.service
```

### 4. Check SSH Status (Optional)
Verify that SSH is running correctly:
```bash
sudo systemctl status sshd.service
```

---

## 🎮 Pterodactyl Panel Installation

### 1. Switch to Superuser
Gain root privileges with:
```bash
sudo su
```

### 2. Update Package Index
Update the list of available packages:
```bash
apt update
```

### 3. Upgrade Installed Packages
Upgrade all installed packages to their latest versions:
```bash
apt upgrade
```

### 4. Install Curl
Install Curl, required for downloading the Pterodactyl installer:
```bash
apt install curl
```

### 5. Run the Pterodactyl Installer
Download and run the Pterodactyl installer:
```bash
bash <(curl -s https://pterodactyl-installer.se/)
```

---

## 🛡️ Additional Considerations

### 1. Firewall Configuration
Allow SSH and HTTP/HTTPS traffic using UFW:
```bash
sudo ufw allow OpenSSH
sudo ufw allow 'Nginx Full'
```

### 2. Domain Configuration
Set up your domain’s DNS to point to your server’s IP address.

### 3. SSL Setup
Install an SSL certificate for secure HTTPS connections:
```bash
sudo apt install certbot python3-certbot-nginx
sudo certbot --nginx -d yourdomain.com
```

---

## ✔️ Final Steps

1. Complete the prompts during the Pterodactyl installation process.
2. Configure the database and create your admin account.
3. Visit the official Pterodactyl Documentation for advanced configurations.

---

## 📞 Contact

For questions or support, feel free to reach out:

- **GitHub**: [nobita586](https://github.com/nobita586)
- **Email**: [your-email@example.com](mailto:your-email@example.com)

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

## 🎉 Acknowledgments

Special thanks to:
- [Pterodactyl Panel](https://pterodactyl.io)
- [Certbot](https://certbot.eff.org)
- [OpenSSH](https://www.openssh.com)

---

## 📄 Notes

1. Replace placeholder image links (https://via.placeholder.com/...) with actual images or diagrams.
2. Replace `your-email@example.com` and `yourdomain.com` with your email and domain.
3. Test all commands on your server to ensure they work as intended.
```

You can now copy this `README.md` into your GitHub project. Let me know if you'd like further refinements or additional sections!
