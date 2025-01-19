# <img src="https://archive.org/download/postgresql_32/postgresql.png" alt="PostgreSQL Logo" width="50" height="50">  Install Frappe 15 with PostgreSQL

This guide provides step-by-step instructions to install Frappe1️⃣5️⃣ with PostgreSQL on a Linux system🐧.

## 1. Update System Packages
```bash
sudo apt update && sudo apt upgrade -y
```

## 2. Install Required Packages
```bash
sudo apt install python3 python3-pip python3-dev libssl-dev libffi-dev build-essential \
    git curl wget gnupg2 software-properties-common -y
```

## 3. Install PostgreSQL🐘
```bash
sudo apt install postgresql postgresql-contrib libpq-dev -y
```

Switch to the PostgreSQL user:
```bash
sudo -i -u postgres
```

Create a new PostgreSQL role:
```bash
createuser --interactive
```
Provide a name for the role (e.g., `frappe`). Then exit the PostgreSQL user shell:
```bash
exit
```

## 4. Install Redis
```bash
sudo apt install redis-server -y
sudo systemctl start redis
sudo systemctl enable redis
```

## 5. Install Node.js and npm
```bash
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install -y nodejs
```

## 6. Install Yarn
```bash
sudo npm install --global yarn
```

## 7. Install wkhtmltopdf
```bash
sudo apt install -y xfonts-75dpi xfonts-100dpi
sudo apt install -y fonts-dejavu
sudo apt install -y wkhtmltopdf
```

## 8. Install Frappe Bench1️⃣5️⃣
```bash
sudo pip3 install frappe-bench
```

## 9. Create a Frappe Bench Instance
```bash
bench init frappe-branch-15 --frappe-branch version-15
cd frappe-branch-15
```

## 10. Create a New Site🏗️
```bash
bench new-site SITE_NAME --db-type postgresql
bench use SITE_NAME
```

Replace `SITE_NAME` with your desired site name.

## 11. Create a New App🧩
```bash
bench new-app APP_NAME
bench --site SITE_NAME install-app APP_NAME
```
Replace `APP_NAME` with your desired app name.

## 12. Start Frappe Development Server
```bash
bench start
```

---
Feel free to communicate with me in case you face any problems

<div align="center">
  <a href="asilgharbia@gmail.com" target="_blank">
    <img src="https://img.shields.io/static/v1?message=Gmail&logo=gmail&label=&color=D14836&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="gmail logo"  />
  </a>
  
  <a href="https://www.linkedin.com/in/asil-gharbia/" target="_blank">
    <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="linkedin logo"  />

  </a>
</div>

