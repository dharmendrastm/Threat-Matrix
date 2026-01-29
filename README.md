# 🔐 ThreatMatrix - CVSS v3.1 Calculator & Vulnerability Dashboard

![ThreatMatrix Banner](https://img.shields.io/badge/ThreatMatrix-Security%20Research%20Platform-00d4ff?style=for-the-badge)
![CVSS v3.1](https://img.shields.io/badge/CVSS-v3.1%20Official-39ff14?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-b620e0?style=for-the-badge)

**Complete security research platform combining CVSS v3.1 scoring with advanced vulnerability analytics.**

Created by **Dharmendra Kumar** ([dharmendrastm](https://github.com/dharmendrastm)) for security researchers, penetration testers, and bug bounty hunters worldwide.

---

## 🚀 Features

### 🎯 CVSS v3.1 Calculator
- ✅ **Official CVSS v3.1 Algorithm** - Accurate base score calculation
- ✅ **Button-Style Metrics** - Intuitive selection interface
- ✅ **8 Base Metrics** - Attack Vector, Complexity, Privileges, User Interaction, Scope, CIA Impact
- ✅ **Real-Time Scoring** - Instant score calculation with severity rating
- ✅ **Vector String Generation** - Standard CVSS v3.1 vector format
- ✅ **Copy Score** - Quick clipboard copy functionality
- ✅ **Screenshot Result** - Export CVSS result as image

### 📊 Vulnerability Dashboard
- ✅ **4 Interactive Charts** - Bar, Pie, Line, and Doughnut visualizations
- ✅ **Real-Time Statistics** - Automatic totals and percentage calculations
- ✅ **Risk Level Indicator** - Overall risk assessment based on severity distribution
- ✅ **Individual Chart Downloads** - Export each chart as high-quality PNG
- ✅ **Multiple Screenshot Options** - Capture graphs, input panel, or full dashboard
- ✅ **Data Persistence** - Save/Load reports using LocalStorage

### 🎨 Professional Design
- ✅ **Dark Cybersecurity Theme** - Eye-friendly interface for long research sessions
- ✅ **Glassmorphism Effects** - Modern UI with backdrop blur
- ✅ **Neon Color Scheme** - Professional and visually appealing
- ✅ **Report-Ready Graphics** - Large, clear charts perfect for documentation
- ✅ **Responsive Layout** - Works on desktop, tablet, and mobile devices
- ✅ **Visitor Counter** - Track tool usage

---

## 📸 Screenshots

### CVSS Calculator
![CVSS Calculator](https://via.placeholder.com/800x400/0a0e27/00d4ff?text=CVSS+v3.1+Calculator)

### Vulnerability Dashboard
![Vulnerability Dashboard](https://via.placeholder.com/800x400/0a0e27/00d4ff?text=Vulnerability+Dashboard)

### Statistical Analysis
![Charts](https://via.placeholder.com/800x400/0a0e27/00d4ff?text=4+Interactive+Charts)

---

## 🎓 How to Use

### 1️⃣ Calculate CVSS Score

1. **Select Metrics**: Click buttons to choose values for all 8 base metrics
2. **Calculate**: Click "Calculate CVSS v3.1 Score" button
3. **View Results**: See score, severity, and vector string
4. **Copy or Screenshot**: Save your results

**Example Metrics:**
```
Attack Vector: Network (N)
Attack Complexity: Low (L)
Privileges Required: None (N)
User Interaction: None (N)
Scope: Unchanged (U)
Confidentiality: High (H)
Integrity: High (H)
Availability: High (H)
```

**Result:** Score: 9.8 - CRITICAL

---

### 2️⃣ Generate Vulnerability Dashboard

1. **Enter Counts**: Input number of vulnerabilities for each severity level
2. **Generate Graphs**: Click "Generate" button
3. **View Analytics**: 4 different chart types for comprehensive analysis
4. **Export Reports**: Download individual charts or full dashboard
5. **Save Data**: Save your report for future reference

**Chart Types:**
- **Bar Chart** - Severity distribution comparison
- **Pie Chart** - Vulnerability breakdown with percentages
- **Line Chart** - Risk trend analysis
- **Doughnut Chart** - Severity proportion visualization

---

## 🔧 Technical Details

### CVSS v3.1 Implementation

**Official Formula Used:**
```javascript
// Impact Sub Score (ISS)
ISS = 1 - ((1 - Confidentiality) × (1 - Integrity) × (1 - Availability))

// Impact
Impact (Unchanged Scope) = 6.42 × ISS
Impact (Changed Scope) = 7.52 × (ISS - 0.029) - 3.25 × (ISS - 0.02)^15

// Exploitability
Exploitability = 8.22 × AttackVector × AttackComplexity × PrivilegesRequired × UserInteraction

// Base Score
BaseScore (Unchanged) = min(Impact + Exploitability, 10)
BaseScore (Changed) = min(1.08 × (Impact + Exploitability), 10)

// Round up to 1 decimal place
FinalScore = ceil(BaseScore × 10) / 10
```

**Severity Ratings:**
| Score Range | Severity | Color |
|-------------|----------|-------|
| 0.0 | None | Blue |
| 0.1 - 3.9 | Low | Green |
| 4.0 - 6.9 | Medium | Red |
| 7.0 - 8.9 | High | Orange |
| 9.0 - 10.0 | Critical | Dark Red |

### Technologies Used

- **HTML5** - Structure
- **CSS3** - Styling with custom properties and glassmorphism
- **JavaScript (ES6+)** - Core functionality
- **Chart.js v4.4.0** - Interactive charts
- **html2canvas v1.4.1** - Screenshot functionality
- **LocalStorage API** - Data persistence

### Browser Compatibility

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

---

## 📦 Installation

### Option 1: Direct Download

1. Download `ThreatMatrix.html`
2. Open in any modern browser
3. Start using immediately (no installation required!)

### Option 2: Clone Repository

```bash
git clone https://github.com/dharmendrastm/ThreatMatrix.git
cd ThreatMatrix
```

Open `ThreatMatrix.html` in your browser.

### Option 3: GitHub Pages (Live Demo)

Visit: [https://dharmendrastm.github.io/ThreatMatrix](https://dharmendrastm.github.io/Threat-Matrix)

---

## 💡 Use Cases

### 🔍 Security Research
- Calculate CVSS scores for discovered vulnerabilities
- Document findings with visual reports
- Track vulnerability severity distribution

### 🎯 Penetration Testing
- Score identified vulnerabilities during assessments
- Generate professional reports for clients
- Visualize security posture improvements

### 🐛 Bug Bounty Hunting
- Quickly assess vulnerability severity
- Create comprehensive reports
- Track findings across multiple programs

### 📝 Security Documentation
- Include CVSS scores in vulnerability reports
- Add professional charts to presentations
- Maintain consistent scoring methodology

### 🎓 Security Training
- Teach CVSS v3.1 scoring methodology
- Demonstrate real-world vulnerability assessment
- Practice report generation

---

## 🎨 Customization

### Change Theme Colors

Edit CSS variables in the `:root` section:

```css
:root {
    --neon-blue: #00d4ff;    /* Primary accent */
    --neon-purple: #b620e0;  /* Secondary accent */
    --neon-green: #39ff14;   /* Success color */
    --neon-red: #ff073a;     /* Danger color */
}
```

### Add Custom Metrics

Extend the CVSS calculator by modifying the `CVSS_WEIGHTS` object:

```javascript
const CVSS_WEIGHTS = {
    // Add your custom metric weights here
};
```

---

## 📊 Export Features

### Individual Charts
- Download each chart separately as PNG
- High-quality 2x scale for print
- Transparent or solid backgrounds

### Full Dashboard
- Complete screenshot of entire dashboard
- Includes all charts and statistics
- Perfect for comprehensive reports

### CVSS Results
- Screenshot individual CVSS calculations
- Copy score to clipboard
- Save vector strings for documentation

---

## 🔒 Security & Privacy

- ✅ **100% Client-Side** - No data sent to servers
- ✅ **LocalStorage Only** - Data stays on your device
- ✅ **No Tracking** - No analytics or external requests
- ✅ **Open Source** - Fully auditable code
- ✅ **Offline Capable** - Works without internet (after first load)

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Contribution Ideas

- 🎨 UI/UX improvements
- 📊 Additional chart types
- 🔧 New export formats (PDF, CSV, JSON)
- 🌐 Internationalization (i18n)
- 📱 Mobile app version
- 🔌 API integration options

---

## 🐛 Bug Reports

Found a bug? Please open an issue with:
- Detailed description
- Steps to reproduce
- Expected vs actual behavior
- Screenshots (if applicable)
- Browser and OS information

---

## 📜 License

This project is licensed under the **MIT License**.

```
MIT License

Copyright (c) 2025 Dharmendra Kumar (dharmendrastm)

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

## 🌟 Related Projects

### 🔍 Surface Hunter Pro
Advanced OSINT & Security Research Tool by Dharmendra Kumar

**Features:**
- Domain Intelligence Gathering
- Subdomain Enumeration
- Technology Detection
- Security Headers Analysis
- And much more!

**Visit:** [https://surfacehunter.vercel.app/](https://surfacehunter.vercel.app/)

---

## 👨‍💻 About the Developer

### Dharmendra Kumar
**Cybersecurity Researcher & Developer**

Passionate about cybersecurity, ethical hacking, and building tools that empower security researchers worldwide.

**Aliases:**
- dharmendrastm
- dharmendrahacker
- dharmendracyberhack

### 🔗 Connect With Me

[![Portfolio](https://img.shields.io/badge/Portfolio-dharmendrastm-00d4ff?style=for-the-badge&logo=vercel)](https://dharmendrastm.vercel.app/)
[![GitHub](https://img.shields.io/badge/GitHub-dharmendrastm-181717?style=for-the-badge&logo=github)](https://github.com/dharmendrastm)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-dharmendrastm-0077b5?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/dharmendrastm/)
[![Medium](https://img.shields.io/badge/Medium-@dharmendrastm-12100E?style=for-the-badge&logo=medium)](https://medium.com/@dharmendrastm)
[![YouTube](https://img.shields.io/badge/YouTube-dharmendrastm-FF0000?style=for-the-badge&logo=youtube)](https://www.youtube.com/@dharmendrastm)

---

## 📈 Project Stats

![GitHub stars](https://img.shields.io/github/stars/dharmendrastm/ThreatMatrix?style=social)
![GitHub forks](https://img.shields.io/github/forks/dharmendrastm/ThreatMatrix?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/dharmendrastm/ThreatMatrix?style=social)

---

## 🏷️ Tags

`dharmendrahacker` `dharmendracyberhack` `cybersecurity` `ThreatMatrix` `ethical-hacking` `cvss-calculator` `vulnerability-assessment` `penetration-testing` `bug-bounty` `security-research` `osint` `infosec` `appsec` `devsecops` `security-tools`

---

## 💖 Support

If you find ThreatMatrix useful, please:
- ⭐ Star this repository
- 🐛 Report bugs and suggest features
- 📢 Share with fellow security researchers
- 💬 Provide feedback

---

## 📞 Contact

- **Email:** dharmendrastm@gmail.com
- **Twitter:** [@dharmendrastm](https://twitter.com/dharmendrastm)
- **Discord:** dharmendrastm#0000

---

## 🙏 Acknowledgments

- **FIRST.org** - For CVSS v3.1 specification
- **Chart.js Team** - For amazing charting library
- **html2canvas Team** - For screenshot functionality
- **Security Community** - For continuous feedback and support

---

## 📝 Changelog

### Version 1.0.0 (January 2025)
- ✅ Initial release
- ✅ CVSS v3.1 calculator with official algorithm
- ✅ 4 interactive chart types
- ✅ Screenshot and export features
- ✅ Dark cybersecurity theme
- ✅ Visitor counter
- ✅ Save/Load functionality

---

## 🎯 Roadmap

### Version 1.1.0 (Planned)
- [ ] CVSS v4.0 support
- [ ] Temporal score calculation
- [ ] Environmental score calculation
- [ ] PDF export functionality
- [ ] CSV data export
- [ ] Multiple language support

### Version 2.0.0 (Future)
- [ ] Cloud sync for reports
- [ ] Collaborative features
- [ ] API integration
- [ ] Mobile app (iOS/Android)
- [ ] Advanced analytics dashboard
- [ ] Custom metric definitions

---

<div align="center">

### Made with ❤️ by Dharmendra Kumar

**ThreatMatrix** - Empowering Security Researchers Worldwide

[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github)](https://github.com/dharmendrastm)

**© 2025-26 ThreatMatrix | All Rights Reserved**

</div>
