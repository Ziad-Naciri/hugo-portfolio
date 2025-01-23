# Secure Portfolio Website with Hugo

## Project Overview

This project is a secure and high-performance personal portfolio website developed using [Hugo](https://gohugo.io/), a fast and flexible static site generator written in Go. The portfolio demonstrates modern web development practices, including security hardening, performance optimization, and responsiveness. It is designed to showcase advanced features and best practices, with a particular focus on security and efficiency.

**Live Demo:** [https://ziad-naciri.netlify.app/](https://ziad-naciri.netlify.app/)  

**Repository:** [GitHub - Hugo Portfolio](https://github.com/Ziad-Naciri/hugo-portfolio/)  

**Project Guide:** [Portfolio Guide](https://github.com/Ziad-Naciri/portfolio-guide)  

---

## Technologies Used
- **Hugo**: Static Site Generator
- **Go**: Core Language for Hugo
- **Dart Sass**: CSS Preprocessor
- **Netlify**: Deployment and DNS management
- **Google Analytics**: Analytics and traffic management
- **Markdown**: Content Management
- **Git**: Version Control
- **Snap**: Package Manager for Installation

---

## Project Features and Objectives

### Design and Responsiveness
- **Modern, responsive design** for optimal viewing on mobile, tablet, and desktop.

### Security Implementation
- **HTTPS**: Ensures secure, encrypted connections.
- **Content Security Policy (CSP)**: Blocks unauthorized scripts and limits resource loading to trusted origins, with the use of hash-based policies.
- **Security Headers**: Configured headers like `X-Content-Type-Options`, `X-Frame-Options`, and `X-XSS-Protection` to mitigate potential vulnerabilities.
- **Cross-site request forgery (CSRF) Mitigation**: Implemented honeypot fields and Netlify Spam Filters using Akismet to prevent spam and bot submissions in forms.
- **OWASP ZAP Testing**: Performed regular security audits, ensuring a clean scan with only non-impactful informational alerts.

### Performance Optimization
- **Image Optimization**: Images are compressed and served in modern formats like WebP to save bandwidth.
- **Lazy Loading**: Improves load times by deferring off-screen images.
- **Code Minification**: HTML, CSS, and JavaScript are minified to reduce file size and improve load times.
- **Cache-Control for Static Assets**: Configured caching for CSS, JS, and image assets, setting `Cache-Control: public, max-age=31536000, immutable` to reduce server load and improve repeat load performance.

### SEO and Analytics
- **Meta Tags and Schema**: Configured meta descriptions, Open Graph tags, and JSON-LD schema for better search engine indexing and social media sharing.
- **Netlify Analytics**: Provides insights into website traffic and visitor behavior.
- **Google Analytics**: Provides indepth summary of the portfolios traffic and visitor behavior.
- **Google Lighthouse**: Achieved high performance scores on PageSpeed Insights, with detailed [test results here](https://pagespeed.web.dev/analysis/https-ziad-naciri-netlify-app/wykzch4isv?form_factor=desktop).

---

## Project Setup and Configuration

### Initial Setup
1. **Install Hugo and Dependencies**  
   ```bash
   snap install hugo --channel=extended
   ```
2. **Clone Repository**  
   ```bash
   git clone https://github.com/Ziad-Naciri/hugo-portfolio/
   cd hugo-portfolio
   ```
3. **Install Raditian Theme**  
   Follow the [Raditian Theme Installation Guide](https://github.com/radity/raditian-free-hugo-theme) to configure the theme.

### Running Locally
To test the project locally:
1. Run the Hugo server:
   ```bash
   hugo server -D
   ```
2. Access the local site at `http://localhost:1313`.

---

## Testing and Optimization

### Testing
- **OWASP ZAP**: Regular scans to identify security vulnerabilities, with adjustments made to mitigate any identified risks.
- **Google Lighthouse**: Tests performed with high scores achieved in Performance (99), Accessibility (100), Best Practices (100), and SEO (100).

### Performance Enhancements
- **Render-blocking Resources**: Defer non-critical CSS/JS files to optimize loading.
- **Minify Resources**: HTML, CSS, and JavaScript are minified to improve load times.

---

## Future Improvements
- **Add CSP Reporting and Error Tracking**: Use a `report-uri` endpoint for tracking CSP violations.
---

