# Introduction to Web Hosting — Apache Task

## 📚 Overview
This repository contains all files created for the **“Introduction to Web Hosting”** internship task conducted by IPSR Solutions Ltd.

The objective was to set up Apache Web Server, configure a default site, and create a custom Virtual Host.

---

## 🧾 Task Objectives
- Install and configure Apache (httpd)
- Create an index.html in the default document root `/var/www/html`
- Create a new virtual host for `mysamplewebsite.itfs`
- Take backup of configuration files before editing
- Record and study Apache default files, document root, and modules

---

## 🧩 Folder Structure
apache-web-hosting-task/
│
├── default_website/
│ └── index.html
│
├── mysamplewebsite.itfs/
│ ├── public_html/
│ │ └── index.html
│ └── conf/
│ └── mysamplewebsite.itfs.conf
│
├── apache-config-backups/
│ └── httpd.conf.bak
│
├── detailed pdf/
│ └── apache.pdf
│
└── README.md

yaml
Copy code

---

## ⚙️ Steps Performed
1. Installed Apache using  
   ```bash
   sudo dnf install -y httpd
   sudo systemctl enable --now httpd
Verified service:

bash
Copy code
sudo systemctl status httpd
curl -I http://localhost
Created index.html in /var/www/html

Created a Virtual Host config /etc/httpd/conf.d/mysamplewebsite.itfs.conf

Reloaded Apache and tested:

bash
Copy code
sudo apachectl configtest
sudo systemctl reload httpd
Edited Windows hosts file to resolve mysamplewebsite.itfs

Verified in browser — website loaded successfully 
