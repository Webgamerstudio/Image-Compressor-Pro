# 🖼️ Image Compressor Pro

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Live Demo](https://img.shields.io/badge/Live-Demo-success)](https://webgamerstudio.github.io/Image-Compressor-Pro/)

A fast, secure, and completely client-side image compression tool that supports JPEG, PNG, and WEBP formats.

**🌐 Live Demo:** [https://webgamerstudio.github.io/Image-Compressor-Pro/](https://webgamerstudio.github.io/Image-Compressor-Pro/)

**Built by [Webgamer Studio](https://webgamerstudio.github.io/Image-Compressor-Pro/)**

---

## ✨ Features

### 🔒 **100% Private and Secure**
- Complete client-side processing
- Your images never leave your device
- All operations happen in your browser
- No server uploads, no data collection

### ⚡ **Lightning Fast Compression**
- Instant results
- Process multiple images simultaneously
- No processing limits
- Real-time preview

### 🎯 **Advanced Customization**
- Custom resolution settings (Max Width/Height)
- Quality slider (10%-100%)
- Multiple output formats (JPEG, PNG, WEBP)
- Aspect ratio preservation option
- Flexible compression control

### 📱 **Works on All Devices**
- Fully responsive design
- Mobile, tablet, and desktop optimized
- Touch and drag-and-drop support
- Progressive Web App ready

### ♿ **Accessibility Focused**
- ARIA labels and roles
- Keyboard navigation support
- Screen reader friendly
- WCAG 2.1 compliant

---

## 🚀 Quick Start

### Installation

1. **Clone the repository:**
```bash
git clone https://github.com/webgamerstudio/Image-Compressor-Pro.git
cd Image-Compressor-Pro
```

2. **Open in browser:**
```bash
# No server needed, just open index.html directly
open index.html
```

Or use a live server:
```bash
# VS Code Live Server
# Or Python HTTP server
python -m http.server 8000

# Or Node.js http-server
npx http-server
```

3. **Visit the live version:**
Simply visit [https://webgamerstudio.github.io/Image-Compressor-Pro/](https://webgamerstudio.github.io/Image-Compressor-Pro/)

---

## 📖 How to Use

### Step 1: Upload Images
- **Drag & Drop**: Drag images directly to the upload area
- **Browse**: Click the upload area to select files
- Supported formats: JPEG, PNG, WEBP
- Multiple file selection supported

### Step 2: Customize Settings
```
⚙️ Compression Settings:
├── Max Width (px): Set maximum image width
├── Max Height (px): Set maximum image height
├── Quality Slider: Compression quality (10%-100%)
├── Output Format: Select JPEG/PNG/WEBP
└── Preserve Aspect Ratio: Maintain original proportions
```

### Step 3: Compress and Download
- **Single Image**: Click "⚡ Compress" button
- **All Images**: Click "✨ Compress All" button
- **Download**: After compression, click "📥 Download" to save
- **Preview**: Click "👁️ Preview" to view compressed image

---

## 🛠️ Technical Details

### Technologies Used
- **HTML5 Canvas API**: For image processing
- **JavaScript (Vanilla)**: Core logic, no dependencies
- **Tailwind CSS**: Styling and responsive design
- **Web APIs**: FileReader, Blob, URL.createObjectURL

### Browser Support
| Browser | Version |
|---------|---------|
| Chrome | 90+ ✅ |
| Firefox | 88+ ✅ |
| Safari | 14+ ✅ |
| Edge | 90+ ✅ |
| Opera | 76+ ✅ |
| Mobile Safari | iOS 14+ ✅ |
| Chrome Mobile | Android 90+ ✅ |

### Performance Metrics
- **File Size**: ~15KB (minified)
- **Load Time**: < 1s
- **Compression Speed**: 1-2 seconds per image (device dependent)
- **Max File Size**: Unlimited (browser memory dependent)
- **Concurrent Processing**: Yes

---

## 📁 File Structure

```
Image-Compressor-Pro/
│
├── index.html              # Main HTML file (all-in-one)
├── README.md               # This file
├── LICENSE                 # MIT License
├── favicon.png             # Site icon (optional)
│
├── images/                 # Optional: OG images
│   ├── og-image.jpg        # 1200x630px
│   └── twitter-image.jpg   # 1200x600px
│
├── screenshots/            # Optional: App screenshots
│   ├── desktop.png
│   ├── mobile.png
│   └── tablet.png
│
└── docs/                   # Optional: Documentation
    ├── CONTRIBUTING.md
    ├── CHANGELOG.md
    └── CODE_OF_CONDUCT.md
```

---

## ⚙️ Configuration

### Customize Meta Tags
```html
<!-- In <head> section of index.html -->
<meta property="og:title" content="Your Custom Title">
<meta property="og:description" content="Your Custom Description">
<meta property="og:image" content="https://your-domain.com/og-image.jpg">
<meta property="og:url" content="https://your-domain.com">
<link rel="canonical" href="https://your-domain.com">
```

### Ad Integration (Optional)
```html
<!-- Header Ad -->
<div id="ad-header" class="ad-container">
    <!-- Paste your ad code here -->
</div>

<!-- Sidebar Ad -->
<div id="ad-sidebar" class="ad-container">
    <!-- Paste your ad code here -->
</div>

<!-- Footer Ad -->
<div id="ad-footer" class="ad-container">
    <!-- Paste your ad code here -->
</div>
```

**Ad Placement Zones:**
- `#ad-header`: Desktop only (728x90)
- `#ad-sidebar`: Tablet/Desktop (300x250)
- `#ad-footer`: Mobile only (320x50)

---

## 🎨 Customization

### Change Colors
```css
/* Find gradient-bg class in CSS */
.gradient-bg {
  background: linear-gradient(135deg, #your-color-1 0%, #your-color-2 100%);
}

/* Change button colors */
.btn-primary {
  background: linear-gradient(to right, #your-color-1, #your-color-2);
}
```

### Change Default Settings
```javascript
// In JavaScript section
const qualityInput = el('quality');
qualityInput.value = 0.9;  // Default quality 90%

const formatSelect = el('format');
formatSelect.value = 'image/webp';  // Default format WEBP

const preserveAspect = el('preserveAspect');
preserveAspect.checked = true;  // Default preserve aspect ratio
```

### Change Max File Size Limit (Optional)
```javascript
function handleFiles(fileList) {
  const MAX_SIZE = 50 * 1024 * 1024; // 50MB limit
  const arr = Array.from(fileList).filter(f => {
    if (f.size > MAX_SIZE) {
      showAlert(`⚠️ ${f.name} is too large (max 50MB)`);
      return false;
    }
    return f.type.startsWith('image/');
  });
  // rest of the code...
}
```

---

## 🔧 Troubleshooting

### Common Issues

**1. Images Not Uploading**
- Check browser console (F12) for errors
- Ensure file format is JPEG/PNG/WEBP
- Check if file size is reasonable (<50MB recommended)
- Try a different browser
- Clear browser cache

**2. Compression is Slow**
- Normal for large images (>10MB)
- Reduce Max Width/Height settings
- Lower quality setting (70-80%)
- Close other browser tabs
- Try on a more powerful device

**3. Download Not Working**
- Check browser popup blocker settings
- Update browser to latest version
- Try right-click → "Save link as"
- Check browser download settings

**4. Drag-Drop Not Working on Mobile**
- Drag-drop is limited on mobile browsers
- Use "tap to browse" instead
- Some mobile browsers don't support drag-drop

**5. Out of Memory Error**
- Image is too large
- Reduce resolution settings
- Compress one image at a time
- Close other browser tabs
- Restart browser

---

## 📊 SEO Optimization

### Included SEO Features:
✅ Semantic HTML5 tags  
✅ Meta descriptions  
✅ Open Graph tags (Facebook, LinkedIn)  
✅ Twitter Card tags  
✅ Schema.org JSON-LD markup  
✅ Canonical URL  
✅ Alt texts for images  
✅ ARIA labels for accessibility  
✅ Mobile-friendly responsive design  
✅ Fast loading time (<1s)  

### SEO Checklist:
- [x] All meta tags updated with correct domain
- [x] OG image created (1200x630px)
- [x] Twitter image created (1200x600px)
- [x] Favicon.png added
- [ ] Sitemap.xml created
- [ ] Robots.txt created
- [ ] Google Analytics integrated (optional)
- [ ] Google Search Console verified (optional)

### Create Sitemap.xml:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://webgamerstudio.github.io/Image-Compressor-Pro/</loc>
    <lastmod>2024-01-01</lastmod>
    <changefreq>monthly</changefreq>
    <priority>1.0</priority>
  </url>
</urlset>
```

### Create Robots.txt:
```
User-agent: *
Allow: /
Sitemap: https://webgamerstudio.github.io/Image-Compressor-Pro/sitemap.xml
```

---

## 🚀 Deployment

### GitHub Pages (Already Deployed ✅)
Your site is already live at:
**https://webgamerstudio.github.io/Image-Compressor-Pro/**

To update:
```bash
git add .
git commit -m "Update: description of changes"
git push origin main
# Changes will be live in 1-2 minutes
```

### Deploy to Netlify:
```bash
# Install Netlify CLI
npm install -g netlify-cli

# Login to Netlify
netlify login

# Deploy
netlify deploy --prod

# Or drag and drop folder to netlify.com
```

### Deploy to Vercel:
```bash
# Install Vercel CLI
npm i -g vercel

# Login to Vercel
vercel login

# Deploy
vercel --prod
```

### Deploy to Cloudflare Pages:
1. Go to pages.cloudflare.com
2. Connect GitHub repository
3. Select `Image-Compressor-Pro` repo
4. Deploy (auto-deploys on push)

---

## 🤝 Contributing

We welcome all contributions! Whether it's bug fixes, new features, or documentation improvements.

### How to Contribute:
1. Fork this repository
2. Create a new branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Commit your changes (`git commit -m 'Add amazing feature'`)
5. Push to the branch (`git push origin feature/amazing-feature`)
6. Open a Pull Request

### Contribution Guidelines:
- Write clean, readable code
- Add comments for complex logic
- Maintain responsive design
- Follow accessibility standards
- Test on multiple browsers
- Update README if needed
- Add descriptive commit messages

### Code of Conduct:
- Be respectful and inclusive
- Provide constructive feedback
- Help others learn and grow
- Follow project guidelines

---

## 🐛 Bug Reports

Found a bug? Please report it!

### Before Reporting:
- [ ] Check if bug already exists in [Issues](https://github.com/webgamerstudio/Image-Compressor-Pro/issues)
- [ ] Try reproducing in different browser
- [ ] Clear browser cache and try again

### Bug Report Template:
```markdown
**Bug Description:**
A clear description of the bug.

**Steps to Reproduce:**
1. Go to '...'
2. Click on '...'
3. See error

**Expected Behavior:**
What should happen

**Actual Behavior:**
What actually happens

**Screenshots:**
If applicable, add screenshots

**Environment:**
- Browser: [e.g., Chrome 120]
- OS: [e.g., Windows 11]
- Device: [e.g., Desktop]
```

---

## 💡 Feature Requests

Have an idea? We'd love to hear it!

Submit feature requests at:
[GitHub Discussions](https://github.com/webgamerstudio/Image-Compressor-Pro/discussions)

---

## 📝 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2024 Webgamer Studio

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 💬 Support & Contact

Need help or have questions?

- 🐛 **Bug Reports**: [GitHub Issues](https://github.com/webgamerstudio/Image-Compressor-Pro/issues)
- 💡 **Feature Requests**: [GitHub Discussions](https://github.com/webgamerstudio/Image-Compressor-Pro/discussions)
- 📧 **Email**: webgamerconnect@gmail.com
- 🌐 **Website**: [https://webgamerstudio.github.io/Image-Compressor-Pro/](https://webgamerstudio.github.io/Image-Compressor-Pro/)
- 💬 **Discord**: Coming soon
- 🐦 **Twitter**: Coming soon

### Response Time:
- Issues: Within 48 hours
- Email: Within 72 hours
- Pull Requests: Within 1 week

---

## 🙏 Acknowledgments

This project was made possible by:

- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS framework
- [Google Fonts](https://fonts.google.com/) - Inter font family
- [HTML5 Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API) - Image processing
- [GitHub Pages](https://pages.github.com/) - Free hosting
- All contributors and users ❤️

### Special Thanks:
- The open-source community
- MDN Web Docs for excellent documentation
- Stack Overflow community
- All beta testers and early adopters

---

## 📈 Roadmap

### Version 2.0 (Coming Soon)
- [ ] Batch download as ZIP file
- [ ] Image filters (Grayscale, Sepia, Blur, etc.)
- [ ] Crop functionality with preset ratios
- [ ] Watermark support (text & image)
- [ ] Before/After comparison slider
- [ ] Advanced settings (DPI, color space)

### Version 2.5 (Future)
- [ ] Dark mode toggle
- [ ] Multi-language support (ES, FR, DE, HI, BN)
- [ ] Cloud storage integration (Dropbox, Google Drive)
- [ ] Browser extension (Chrome, Firefox)
- [ ] API for developers

### Version 3.0 (Vision)
- [ ] Progressive Web App (PWA)
- [ ] Offline mode
- [ ] Image editing tools
- [ ] AI-powered optimization
- [ ] Bulk processing (100+ images)
- [ ] Desktop app (Electron)

### Vote for Features:
Visit [GitHub Discussions](https://github.com/webgamerstudio/Image-Compressor-Pro/discussions) to vote on features you want!

---

## 📸 Screenshots

### Desktop View
![Desktop Screenshot](screenshots/desktop.png)
*Full-featured interface with drag-and-drop support*

### Mobile View
![Mobile Screenshot](screenshots/mobile.png)
*Optimized for touch interactions*

### Tablet View
![Tablet Screenshot](screenshots/tablet.png)
*Perfect for on-the-go compression*

### Compression Results
![Results Screenshot](screenshots/results.png)
*See compression savings in real-time*

---

## 📊 Project Stats

![GitHub Stars](https://img.shields.io/github/stars/webgamerstudio/Image-Compressor-Pro?style=social)
![GitHub Forks](https://img.shields.io/github/forks/webgamerstudio/Image-Compressor-Pro?style=social)
![GitHub Watchers](https://img.shields.io/github/watchers/webgamerstudio/Image-Compressor-Pro?style=social)
![GitHub Issues](https://img.shields.io/github/issues/webgamerstudio/Image-Compressor-Pro)
![GitHub Pull Requests](https://img.shields.io/github/issues-pr/webgamerstudio/Image-Compressor-Pro)
![GitHub Last Commit](https://img.shields.io/github/last-commit/webgamerstudio/Image-Compressor-Pro)
![GitHub Code Size](https://img.shields.io/github/languages/code-size/webgamerstudio/Image-Compressor-Pro)

---

## 🌟 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=webgamerstudio/Image-Compressor-Pro&type=Date)](https://star-history.com/#webgamerstudio/Image-Compressor-Pro&Date)

---

## 🔗 Related Projects

Check out other tools by Webgamer Studio:
- Coming soon...

---

## ❓ FAQ

**Q: Is my data safe?**  
A: Yes! All processing happens in your browser. Nothing is uploaded to any server.

**Q: What's the maximum file size?**  
A: There's no hard limit, but we recommend <50MB for best performance.

**Q: Can I use this for commercial projects?**  
A: Yes! This project is MIT licensed, so you can use it freely.

**Q: Why is compression slow on my phone?**  
A: Mobile devices have less processing power. Try reducing image resolution.

**Q: Can I compress videos?**  
A: Not yet, but it's on our roadmap!

**Q: How do I report a bug?**  
A: Create an issue on GitHub or email us at webgamerconnect@gmail.com

**Q: Can I contribute?**  
A: Absolutely! We welcome all contributions. See Contributing section.

**Q: Is there an API?**  
A: Not yet, but planned for version 2.5.

---

## 🌟 Star Us!

If this project helps you, please consider giving it a ⭐ on GitHub!

It helps others discover this tool and motivates us to keep improving it.

[⭐ Star on GitHub](https://github.com/webgamerstudio/Image-Compressor-Pro)

---

## 📢 Share

Help others discover Image Compressor Pro:

[![Twitter](https://img.shields.io/badge/Share-Twitter-1DA1F2?logo=twitter&logoColor=white)](https://twitter.com/intent/tweet?text=Check%20out%20Image%20Compressor%20Pro!%20Free,%20fast,%20and%20secure%20image%20compression%20tool.&url=https://webgamerstudio.github.io/Image-Compressor-Pro/)
[![Facebook](https://img.shields.io/badge/Share-Facebook-1877F2?logo=facebook&logoColor=white)](https://www.facebook.com/sharer/sharer.php?u=https://webgamerstudio.github.io/Image-Compressor-Pro/)
[![LinkedIn](https://img.shields.io/badge/Share-LinkedIn-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/sharing/share-offsite/?url=https://webgamerstudio.github.io/Image-Compressor-Pro/)
[![Reddit](https://img.shields.io/badge/Share-Reddit-FF4500?logo=reddit&logoColor=white)](https://www.reddit.com/submit?url=https://webgamerstudio.github.io/Image-Compressor-Pro/&title=Image%20Compressor%20Pro)

---

**Made with ❤️ by [Webgamer Studio](https://webgamerstudio.github.io/Image-Compressor-Pro/)**

*Last Updated: January 2024*

---

### ⚡ Quick Links

- [Live Demo](https://webgamerstudio.github.io/Image-Compressor-Pro/)
- [Report Bug](https://github.com/webgamerstudio/Image-Compressor-Pro/issues)
- [Request Feature](https://github.com/webgamerstudio/Image-Compressor-Pro/discussions)
- [Contact Us](mailto:webgamerconnect@gmail.com)

---

**Enjoy compressing! 🎉**