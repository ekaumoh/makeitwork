# makeitwork
# Azure Static Resume Site – ekaetteumoh.tech

This repo contains the source and documentation for my dark-themed resume site, hosted as a **static website on Azure Storage**, fronted with **Azure CDN**, **Azure DNS**, and secured end-to-end with **HTTPS** using a custom SSL certificate.

🌐 **Live site:** `https://ekaetteumoh.tech` (replace with your final URL)  
👩🏾‍💻 **Role:** Junior Cloud Engineer (Azure | GCC High | M365)

---

## ✨ Project Overview

This project started as a simple static HTML resume and evolved into a **production-style cloud deployment**:

- Static site hosted in **Azure Storage** with Static Website hosting.
- Fronted by **Azure CDN** for performance and global reach.
- Custom domain managed via **Namecheap → Azure DNS → CDN**.
- **Custom SSL certificate** converted to PFX and wired into Azure for HTTPS.

It’s a small site, but the deployment pipeline and cloud pieces reflect how I think like a Cloud Engineer.

---

## 🧱 Architecture

**Components:**

- **Azure Storage (Static Website)**  
  Hosts `index.html`, `style.css`, and any future static assets.

- **Azure CDN Endpoint**  
  Fronts the storage static website for caching, performance, and TLS termination.

- **Azure DNS Zone**  
  Hosts DNS records for `ekaetteumoh.tech` and `www.ekaetteumoh.tech`.

- **Namecheap (Registrar)**  
  Points domain nameservers to Azure DNS.

- **Custom SSL Certificate**  
  CA-issued certificate converted to `.pfx` and used to enable HTTPS on the CDN custom domain.

See [`docs/architecture.md`](docs/architecture.md) for a more detailed breakdown and diagrams (logical + DNS flow).

---

## 📁 Repo Structure

```text
.
├── index.html              # Resume site HTML
├── style.css               # Site styling
├── script.js               # (Optional) future JS enhancements
├── docs/
│   ├── architecture.md     # Architecture & diagrams
│   ├── deployment-guide.md # Step-by-step Azure + Namecheap setup
│   └── notes.md            # Lessons learned and troubleshooting
└── assets/
    └── diagrams/
        └── architecture.png
