# Whittemore Painting

## Overview
A static brochure web application developed and deployed for a local residential and commercial painting contractor. The site is designed to provide critical business information, portfolio imaging, and contact routing with maximum uptime and zero maintenance overhead.

## Architecture & Deployment
The application is intentionally engineered as a purely static deployment, prioritizing speed, reliability, and security over complex dynamic rendering.

* **Frontend:** HTML5 and CSS3. 
* **Hosting:** Deployed via GitHub Pages, utilizing a global CDN for asset delivery and built-in SSL/TLS termination.
* **Media Handling:** Image assets are statically served, avoiding the need for a dynamic Content Management System (CMS) or database integration.

## Security Considerations & Threat Model
By deliberately choosing a static architecture for a non-transactional business site, the application's attack surface is drastically reduced.

### 1. Elimination of Backend Vulnerabilities
* Because there is no server-side processing (e.g., PHP, Node.js, Python), no database (e.g., SQL, MongoDB), and no API endpoints, traditional OWASP Top 10 vulnerabilities such as SQL Injection, Command Injection, and Server-Side Request Forgery (SSRF) are structurally impossible.

### 2. Client-Side Integrity
* The site does not rely on complex, third-party JavaScript libraries or frameworks, significantly mitigating the risk of Supply Chain attacks or Cross-Site Scripting (XSS) vectors originating from compromised dependencies.

### 3. Infrastructure Security
* Hosting relies entirely on GitHub's enterprise-grade infrastructure. Denial of Service (DoS) mitigation and SSL certificate management are handled at the platform level, ensuring the local business maintains a secure, uninterrupted web presence without requiring a dedicated DevOps resource.
