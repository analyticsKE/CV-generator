# 🎯 Modern CV Generator

A professional, free, and easy-to-use CV/Resume generator with live preview, PDF export, and persistent data storage. Built with React and hosted on GitHub Pages.

![CV Generator Demo](https://img.shields.io/badge/Status-Live-success) ![License](https://img.shields.io/badge/License-MIT-blue) ![Version](https://img.shields.io/badge/Version-1.0.0-orange)

## ✨ Features

### Core Functionality
- 📝 **Comprehensive CV Sections**
  - Personal Information with custom links (GitHub, LinkedIn, Portfolio)
  - Professional Summary
  - Work Experience (unlimited entries)
  - Education History
  - Skills (Technical, Languages, Soft Skills)
  - Projects with GitHub/Live Demo links
  
- 👁️ **Live Preview**
  - Real-time preview of your CV
  - Professional formatting
  - Clean, ATS-friendly layout
  
- 💾 **Data Persistence**
  - Auto-save to browser localStorage
  - Export CV data as JSON
  - Import previously saved data
  - No account or login required
  
- 📄 **PDF Export**
  - One-click PDF generation
  - Print-optimized layout
  - Professional formatting preserved

### User Experience
- 🎨 Clean, modern interface
- 📱 Responsive design (mobile-friendly)
- ⚡ Fast and lightweight
- 🔒 Privacy-focused (all data stays local)
- 🌐 Works offline after first load

## 🚀 Quick Start

### Option 1: Use the Live Version
Simply visit: **[Your GitHub Pages URL]**

### Option 2: Deploy Your Own

1. **Fork this repository**
   ```bash
   Click the "Fork" button at the top right
   ```

2. **Enable GitHub Pages**
   - Go to repository Settings
   - Navigate to Pages (under "Code and automation")
   - Set Source to "main" branch, "/" (root) folder
   - Click Save
   - Wait 2-3 minutes for deployment

3. **Access your CV Generator**
   ```
   https://yourusername.github.io/cv-generator/
   ```

### Option 3: Run Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/cv-generator.git
   cd cv-generator
   ```

2. **Open in browser**
   ```bash
   # Simply open index.html in your browser
   open index.html  # macOS
   start index.html # Windows
   xdg-open index.html # Linux
   ```

   Or use a local server:
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Python 2
   python -m SimpleHTTPServer 8000
   
   # Node.js (if you have http-server installed)
   npx http-server
   ```

   Then visit: `http://localhost:8000`

## 📖 How to Use

### Creating Your CV

1. **Fill in Personal Information**
   - Enter your name, title, contact details
   - Add links to GitHub, LinkedIn, portfolio, etc.

2. **Add Your Professional Summary**
   - Write a brief overview of your career and strengths

3. **Add Work Experience**
   - Click "Add Experience" for each position
   - Include company, role, dates, and key achievements
   - Use bullet points for better readability

4. **Add Education**
   - Click "Add Education" for each degree/certification
   - Include institution, degree, field, dates, and GPA (optional)

5. **List Your Skills**
   - Technical skills (programming languages, tools, frameworks)
   - Languages you speak
   - Soft skills (leadership, communication, etc.)

6. **Showcase Projects**
   - Click "Add Project" for each portfolio item
   - Include project name, description, technologies
   - Add GitHub and live demo links

7. **Save Your Work**
   - Click the "Save" button to store in browser
   - Click "Export" to download a backup JSON file

8. **Generate PDF**
   - Switch to "Preview" tab
   - Click "PDF" button
   - Use your browser's print dialog to save as PDF

### Managing Your Data

**Saving Progress:**
- Click **"Save"** frequently to store data in browser localStorage
- Data persists across sessions on the same browser/device
- Note: Clearing browser data will delete your CV

**Creating Backups:**
- Click **"Export"** to download your CV data as JSON
- Store the file in a safe location (cloud storage recommended)
- Recommended: Create backups before major edits

**Transferring Between Devices:**
1. Export CV data on Device A
2. Transfer JSON file (email, cloud, USB)
3. Import JSON file on Device B

**Resetting/Starting Over:**
- Export current data first (backup)
- Refresh the page and clear browser localStorage
- Or manually delete all content and save

## 🛠️ Technical Details

### Built With
- **React 18** - UI framework
- **Tailwind CSS** - Styling
- **Vanilla JavaScript** - No build process required
- **localStorage API** - Data persistence
- **Browser Print API** - PDF generation

### Browser Compatibility
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Opera 76+

### File Structure
```
cv-generator/
├── index.html          # Main application file (self-contained)
├── README.md          # Documentation (this file)
└── LICENSE            # MIT License
```

### Data Storage
- All CV data is stored in browser **localStorage**
- Key: `cvData`
- Format: JSON string
- Max size: ~5-10MB (varies by browser)
- Privacy: Data never leaves your device

### Data Format
```json
{
  "personal": {
    "name": "string",
    "title": "string",
    "email": "string",
    "phone": "string",
    "location": "string",
    "links": [{"label": "string", "url": "string"}]
  },
  "summary": "string",
  "experience": [{
    "company": "string",
    "role": "string",
    "startDate": "string",
    "endDate": "string",
    "description": "string"
  }],
  "education": [{
    "institution": "string",
    "degree": "string",
    "field": "string",
    "startDate": "string",
    "endDate": "string",
    "gpa": "string"
  }],
  "skills": {
    "technical": ["string"],
    "languages": ["string"],
    "soft": ["string"]
  },
  "projects": [{
    "name": "string",
    "description": "string",
    "technologies": "string",
    "githubUrl": "string",
    "liveUrl": "string"
  }]
}
```

## 🎨 Customization

### Changing Colors

Edit the `index.html` file and modify Tailwind classes:

**Button Colors:**
```html
<!-- Change from blue to purple -->
bg-blue-600 → bg-purple-600
hover:bg-blue-700 → hover:bg-purple-700
```

**Text Colors:**
```html
text-gray-900 → text-slate-900
text-gray-700 → text-slate-700
```

### Adding Custom Fonts

Add to the `<head>` section:
```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
<style>
  body { font-family: 'Inter', sans-serif; }
</style>
```

### Modifying Layout

The preview section uses standard HTML/CSS. Edit the Preview tab rendering section in the React component to customize the CV layout.

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. **Commit your changes**
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
4. **Push to the branch**
   ```bash
   git push origin feature/AmazingFeature
   ```
5. **Open a Pull Request**

### Ideas for Contributions
- [ ] Additional CV templates (classic, modern, minimal)
- [ ] Color theme switcher
- [ ] Multi-language support
- [ ] LinkedIn profile import
- [ ] Cover letter generator
- [ ] Auto-save functionality
- [ ] Dark mode
- [ ] Drag-and-drop section reordering
- [ ] ATS optimization tips
- [ ] Keyword highlighting

## 🐛 Troubleshooting

### Data Not Saving
**Problem:** Changes disappear after refresh
**Solutions:**
- Check if localStorage is enabled in browser settings
- Try a different browser
- Check browser privacy settings (incognito mode blocks localStorage)
- Export data as backup

### PDF Quality Issues
**Problem:** PDF looks different from preview
**Solutions:**
- Use Chrome or Edge for best results
- Check print settings: margins, scale, orientation
- Ensure "Background graphics" is enabled
- Try different paper sizes (A4, Letter)

### Site Not Loading
**Problem:** GitHub Pages URL returns 404
**Solutions:**
- Wait 2-3 minutes after enabling Pages
- Check repository Settings → Pages is configured correctly
- Ensure `index.html` is in the root directory
- Try hard refresh: Ctrl+F5 (Win) or Cmd+Shift+R (Mac)

### Styling Issues
**Problem:** CSS not loading or looks broken
**Solutions:**
- Check internet connection (CDN dependencies)
- Clear browser cache
- Try incognito/private window
- Verify Tailwind CDN is accessible

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2024 [Your Name]

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

## 🌟 Acknowledgments

- Built with [React](https://react.dev/)
- Styled with [Tailwind CSS](https://tailwindcss.com/)
- Icons inspired by [Lucide](https://lucide.dev/)
- Hosted on [GitHub Pages](https://pages.github.com/)

## 📞 Support

### Getting Help
- **Issues:** [Open an issue](https://github.com/yourusername/cv-generator/issues)
- **Discussions:** [Join discussions](https://github.com/yourusername/cv-generator/discussions)
- **Email:** your.email@example.com

### FAQ

**Q: Is my data secure?**
A: Yes! All data is stored locally in your browser. Nothing is sent to any server. For additional security, export your data and store it encrypted.

**Q: Can I use this for commercial purposes?**
A: Yes! This project is MIT licensed, so you can use it freely for personal or commercial purposes.

**Q: Will this work on mobile?**
A: Yes! The interface is responsive and works on tablets and smartphones, though desktop is recommended for editing.

**Q: Can I customize the CV template?**
A: Yes! You can modify the HTML/CSS in the preview section. Future versions will include multiple templates.

**Q: How do I delete my data?**
A: Clear your browser's localStorage for this site, or manually remove all content and click Save.

**Q: Can multiple people collaborate on one CV?**
A: Not directly, but you can share the exported JSON file and import it on another device.

## 🚀 Roadmap

### Version 1.1 (Coming Soon)
- [ ] Multiple CV templates
- [ ] Auto-save every 30 seconds
- [ ] Undo/Redo functionality
- [ ] Section reordering (drag & drop)

### Version 1.2 (Planned)
- [ ] Dark mode
- [ ] Color theme customizer
- [ ] Cover letter generator
- [ ] ATS optimization score

### Version 2.0 (Future)
- [ ] Cloud sync (optional)
- [ ] Collaboration features
- [ ] AI-powered content suggestions
- [ ] Multi-language support

---

## ⭐ Star This Repository

If you find this project helpful, please give it a star! It helps others discover it too.

---

**Made with ❤️ by [Your Name]**

[Live Demo](https://yourusername.github.io/cv-generator/) | [Report Bug](https://github.com/yourusername/cv-generator/issues) | [Request Feature](https://github.com/yourusername/cv-generator/issues)
