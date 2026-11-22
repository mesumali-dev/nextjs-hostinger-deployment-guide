# 🚀 Next.js Production Deployment Guide on Hostinger VPS

[![Linux](https://img.shields.io/badge/Linux-Ubuntu-E95420?style=flat-square&logo=ubuntu)](https://ubuntu.com/)
[![Nginx](https://img.shields.io/badge/Nginx-Reverse_Proxy-009639?style=flat-square&logo=nginx)](https://nginx.org/)
[![PM2](https://img.shields.io/badge/PM2-Process_Manager-2B037A?style=flat-square&logo=pm2)](https://pm2.keymetrics.io/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-336791?style=flat-square&logo=postgresql)](https://postgresql.org)

> Step-by-step production handbook and DevOps configuration scripts for deploying full-stack Next.js applications, PM2 process management, Nginx reverse proxy, SSL certs, and PostgreSQL backups on Hostinger VPS.

---

## 📖 Guide Overview

1. **Server Provisioning:** Initial Ubuntu setup, UFW firewall configuration, and non-root sudo user.
2. **Runtime Environment:** Installing Node.js via NVM, Git, and build essentials.
3. **Process Supervision:** Configuring PM2 cluster mode for zero-downtime reloads.
4. **Nginx Reverse Proxy:** Nginx server blocks routing port 80/443 to localhost Next.js app.
5. **SSL & Security:** Automated Let's Encrypt certificates with Certbot auto-renewal.
6. **Database Backups:** Automated cron job for PostgreSQL dump rotation and cloud synchronization.

---

## 🛠️ Quick Commands

```bash
# Build app on server
npm run build

# Start with PM2
pm2 start npm --name "nextjs-app" -- start

# Test Nginx configuration
sudo nginx -t && sudo systemctl reload nginx
```

---

## 👨‍💻 Author
**Syed Mesum Ali** — [@mesumali-dev](https://github.com/mesumali-dev)
