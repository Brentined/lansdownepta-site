# Lansdowne Elementary PTA Website

Welcome to the official website repository for the Lansdowne Elementary School PTA.

This project provides a simple, modern, and fun **static website** hosted via **cPanel** on Namecheap and deployed automatically from GitHub using **GitHub Actions + FTP**.

---

## 🎯 Purpose

- Provide a public-facing website for parents, staff, and community members
- Offer continuity and version control across PTA board transitions
- Empower future volunteers with easy-to-use tools and workflows

---

## 🧱 Project Structure
.
├── index.html
├── about.html
├── contact.html
├── events.html
├── support.html
├── css/
├── img/
├── js/
├── .github/
│ └── workflows/
│ └── deploy.yml
└── README.md

---

## 🚀 Deployment

This site is automatically deployed to:

**🌐 [https://lansdownepta.org](https://lansdownepta.org)**

Using **GitHub Actions** and **FTP to cPanel** whenever changes are pushed to the `main` branch.

---

## ⚙️ How It Works

1. On every push to `main`, GitHub runs `.github/workflows/deploy.yml`
2. It connects via FTPS to the Namecheap hosting server
3. It uploads the latest version of the website to `/public_html/`

---

## 🔐 Secrets & FTP Setup

GitHub repository secrets (set in **Settings → Secrets → Actions**):

| Name           | Description                       |
|----------------|-----------------------------------|
| `FTP_HOST`     | e.g. `ftp.lansdownepta.org`       |
| `FTP_USERNAME` | Your FTP username from cPanel     |
| `FTP_PASSWORD` | Your FTP password from cPanel     |

These secrets are used in the `deploy.yml` GitHub Actions workflow.

---

## 🛠 How to Update the Site

1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/lansdownepta-site.git