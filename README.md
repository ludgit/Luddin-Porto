# Musthofa Kamaluddin Portfolio

A sleek, responsive portfolio website showcasing Musthofa Kamaluddin’s full-stack web development projects. Built with PHP, Tailwind CSS, and JavaScript, it features an infinite-scrolling project carousel, SEO optimizations, and smooth animations.

## ✨ Features

- **Dynamic Projects**: PHP-driven portfolio with responsive project cards.
- **Infinite Scroll**: Horizontal carousel on desktop, vertical stack on mobile.
- **Mobile-Optimized**: Clean, polished UI for all screen sizes.
- **SEO-Friendly**: Meta tags, `srcset`, JSON-LD, and sitemap integration.
- **Animated**: GSAP-powered transitions for a modern feel.
- **Accessible**: ARIA attributes and keyboard navigation support.

## 🚀 Getting Started

### Prerequisites

- PHP 7.4+
- Web server (Apache/Nginx)
- Node.js (optional, for Tailwind CSS build)

### Installation

1. Clone the repo:

   ```bash
   git clone https://github.com/musthofa-kamaluddin/Portfolio.git
   cd portfolio
   ```
2. Set up your web server to point to the project root.
3. (Optional) Compile Tailwind CSS:

   ```bash
   npm install -D tailwindcss
   npx tailwindcss -i ./assets/css/input.css -o ./assets/css/tailwind.min.css --minify
   ```
4. Update project data in `index.php`:

   ```php
   $projects = [
       ['id' => '1', 'title' => 'Project One', 'description' => '...', 'image' => 'assets/img/project1.jpg', 'link' => 'https://example.com'],
       // Add more
   ];
   ```
5. Deploy to a PHP-compatible server (e.g., `https://luddin.my.id`).

## 📂 Project Structure

```
portfolio/
├── assets/
│   ├── css/              # Styles (styles.css, tailwind.min.css)
│   ├── img/              # Images (favicon.png, project images)
│   ├── js/               # Scripts (GSAP, SweetAlert2 fallbacks)
├── index.php             # Main PHP file
├── sitemap.xml           # SEO sitemap
└── README.md             # This file
```

## 🖥️ Usage

- **View**: Access at `http://your-domain.com` or `http://localhost/portfolio`.
- **Customize**: Edit `$projects` in `index.php` or tweak `styles.css`.
- **Test**:
  - Desktop: Check infinite scroll and hover effects.
  - Mobile: Ensure vertical card stack and tap interactions (&lt;360px).
- **SEO**: Verify `srcset`, JSON-LD, and `sitemap.xml` in DevTools.

## 🛠️ Troubleshooting

- **Mobile Issues**: Confirm `styles.css` has mobile styles (`flex-direction: column`, `max-width: 350px`).
- **Scroll Lag**: Adjust `scrollSpeed` in `initInfiniteScroll` (e.g., `0.5`).
- **Images**: Ensure project image paths exist in `$projects`.

## 🤝 Contributing

Pull requests and issues are welcome! Fork the repo and submit changes.

## 📜 License

MIT License. See LICENSE for details.

## 📬 Contact

- **Musthofa Kamaluddin**
- Email: musthofa.kamaluddin21@gmail.com
- GitHub: musthofa-kamaluddin
- LinkedIn: musthofa-kamaluddin

---

Built with 💻 by Musthofa Kamaluddin
