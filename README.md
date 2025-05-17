Musthofa Kamaluddin Portfolio
A personal portfolio website showcasing Musthofa Kamaluddin’s work as a full-stack web developer from Gresik, Indonesia. Built with PHP, Tailwind CSS, and JavaScript, the site features a responsive design, SEO optimizations, GSAP animations, and an infinite-scrolling project carousel.
Features

Dynamic Content: PHP-driven sections for projects, services, and contact form.
Responsive Design: Optimized for mobile and desktop with a clean, modern UI.
Infinite Scroll: Horizontal project carousel on desktop, vertical stack on mobile.
SEO: Includes meta tags, srcset for images, JSON-LD, and sitemap integration.
Animations: Smooth GSAP-powered transitions for engaging user experience.
Accessibility: ARIA attributes and keyboard navigation for the project carousel.
Security: XSS protection via htmlspecialchars and CSP meta tag.

Prerequisites

PHP: Version 7.4 or higher.
Web Server: Apache or Nginx with PHP support.
Composer: Optional, for dependency management (if used).
Node.js: For Tailwind CSS compilation (optional, if not using CDN).

Installation

Clone the Repository:
git clone https://github.com/ludgit/portfolio.git
cd portfolio


Set Up Web Server:

Configure your server to point to the project’s root directory (e.g., /public or root).
Ensure PHP is enabled.


Install Tailwind CSS (if using local build):
npm install -D tailwindcss
npx tailwindcss init


Update tailwind.config.js:module.exports = {
  content: ['./*.php', './assets/**/*.js'],
  theme: { extend: {} },
  plugins: [],
}


Compile CSS:npx tailwindcss -i ./assets/css/input.css -o ./assets/css/tailwind.min.css --minify




Copy Assets:

Ensure /assets/img/, /assets/css/, and /assets/js/ contain required files (e.g., favicon.png, tailwind.min.css, gsap.min.js).
Verify image paths in $projects array (e.g., main.jpg, project['image']).


Configure PHP:

Update $projects array in index.php with your project data:$projects = [
    ['id' => '1', 'title' => 'Project One', 'description' => '...', 'image' => 'assets/img/project1.jpg', 'image_medium' => 'assets/img/project1-medium.jpg', 'link' => 'https://example.com'],
    // Add more projects
];


Set up contact form logic (e.g., email handling) if not implemented.


Deploy:

Upload to a PHP-compatible server (e.g., shared hosting, VPS).
Ensure sitemap.xml exists in the root:<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
    <url><loc>https://luddin.my.id</loc></url>
    <url><loc>https://luddin.my.id/#about</loc></url>
    <url><loc>https://luddin.my.id/#services</loc></url>
    <url><loc>https://luddin.my.id/#portfolio</loc></url>
    <url><loc>https://luddin.my.id/#contact</loc></url>
</urlset>





File Structure
portfolio/
├── assets/
│   ├── css/
│   │   ├── styles.css       # Custom styles
│   │   ├── tailwind.min.css # Compiled Tailwind CSS
│   ├── img/
│   │   ├── favicon.png      # 32x32 favicon
│   │   ├── main.jpg         # Profile image
│   │   ├── og-image.jpg     # Open Graph image
│   │   ├── project*.jpg     # Project images
│   ├── js/
│   │   ├── gsap.min.js      # GSAP fallback
│   │   ├── ScrollTrigger.min.js
│   │   ├── sweetalert2.min.js
├── index.php                # Main PHP file
├── sitemap.xml              # SEO sitemap
└── README.md                # This file

Usage

View the Site: Access via http://your-domain.com or http://localhost/portfolio.
Update Projects: Edit $projects in index.php to add/remove projects.
Customize Styles: Modify assets/css/styles.css for design tweaks.
Test Responsiveness:
Desktop: Confirm infinite scroll (horizontal, left) and hover effects.
Mobile: Verify vertical card stack, tap effects, and no overflow (<360px).


SEO Check:
Use Google’s Structured Data Testing Tool for JSON-LD.
Verify srcset and loading="lazy" in DevTools.



Troubleshooting

Mobile Layout Issues:
Ensure assets/css/styles.css includes the latest Portfolio CSS (single-column, max-width: 350px).
Test on 320px screens to confirm no overflow.


Infinite Scroll Lag:
Reduce $projects array size or adjust scrollSpeed in initInfiniteScroll (e.g., 0.5).


Image Loading:
Verify image and image_medium paths in $projects.
Optimize images (<100KB) for performance.


PHP Errors:
Check server logs for syntax issues.
Ensure $projects is defined before the Portfolio section.



Contributing

Fork the repository and submit pull requests for bug fixes or enhancements.
Report issues via GitHub Issues, including screenshots for UI problems.

License
This project is licensed under the MIT License. See LICENSE for details.
Contact
Musthofa Kamaluddin  

Email: musthofa.kamaluddin21@gmail.com  
LinkedIn: musthofa-kamaluddin-8338812a1  
GitHub: musthofa-kamaluddin
