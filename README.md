
# 🌌 **NASA Space Explorer** 🚀

<div align="center">

![NASA Logo](https://www.nasa.gov/wp-content/themes/nasa/assets/images/nasa-logo.svg)

**An immersive web application to explore our Solar System powered by NASA APIs**

[![React](https://img.shields.io/badge/React-19+-61dafb?style=for-the-badge&logo=react&logoColor=white)](https://reactjs.org/)
[![NASA API](https://img.shields.io/badge/NASA-API-0B3D91?style=for-the-badge&logo=nasa&logoColor=white)](https://api.nasa.gov/)
[![Vite](https://img.shields.io/badge/Vite-6+-646cff?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)

---

### 🌍 **[Live Demo](#)** | 📖 **[Documentation](#features)**

</div>

---

## ✨ **Overview**

NASA Space Explorer is a modern, interactive web application that brings the wonders of our Solar System to your fingertips. Built with React and powered by NASA's official APIs, this application offers:

- 🪐 **10+ Celestial Bodies** - Explore planets, dwarf planets, and our Sun
- 🌓 **Dark & Light Mode** - Beautiful galaxy-themed interface
- 🌍 **Multilingual Support** - Available in English, French, Spanish, and Italian
- 📸 **NASA APOD Integration** - Daily astronomy pictures from NASA
- 🎨 **Stunning Visuals** - High-quality images from NASA's archives
- 📱 **Fully Responsive** - Perfect on all devices

---

## 🎯 **Features**

### 🌟 **Core Features**

| Feature | Description |
|---------|-------------|
| 🔍 **Search** | Find any planet or celestial body instantly |
| 📊 **Detailed Info** | Comprehensive data on diameter, mass, gravity, temperature, and more |
| 🎨 **Beautiful UI** | Galaxy-inspired design with smooth animations |
| 🌓 **Theme Toggle** | Switch between dark space theme and light mode |
| 🌐 **i18n Support** | Full multilingual support (EN, FR, ES, IT) |
| 🖼️ **NASA APOD** | Daily astronomy picture with detailed explanations |

### 🎨 **Visual Features**

- ⭐ Animated starfield background in dark mode
- 🌟 Glowing effects on celestial bodies
- 🎭 Smooth transitions and hover effects
- 🌈 Color-coded planets based on their actual appearance
- 📸 High-quality NASA imagery

---

## 🚀 **Quick Start**

### Prerequisites

- Node.js 18+ 
- npm or yarn

### Installation

```bash
# 1️⃣ Clone the repository
git clone https://github.com/yourusername/nasa-space-explorer.git
cd nasa-space-explorer

# 2️⃣ Install dependencies
npm install

# 3️⃣ Start development server
npm run dev

# 🎉 Open http://localhost:3000
```

### Build for Production

```bash
npm run build
npm run preview
```

---

## 🎮 **How to Use**

### 🔍 **Exploring Planets**

1. **Search Mode**: Enter a planet name in the search bar
2. **Gallery Mode**: Click "View Gallery" to browse all celestial bodies
3. **Details View**: Click on any planet to see comprehensive information

### 🌓 **Switching Themes**

- Click the **sun/moon icon** in the header to toggle between light and dark themes
- Theme preference is saved automatically

### 🌍 **Changing Language**

- Click on **EN**, **FR**, **ES**, or **IT** buttons in the header
- All content updates instantly
- Language preference is preserved

---

## 🛠️ **Technology Stack**

<div align="center">

| Category | Technologies |
|----------|-------------|
| **Frontend** | React 19, JSX, Hooks (useState, useEffect, useMemo, useContext) |
| **Styling** | CSS Modules, CSS Variables, Animations, Flexbox, Grid |
| **UI Library** | PrimeReact, PrimeFlex, PrimeIcons |
| **Build Tool** | Vite (SWC compiler) |
| **APIs** | NASA Open APIs (APOD, Planetary Data) |
| **State Management** | React Context API |
| **Internationalization** | Custom i18n implementation |
| **Analytics** | Vercel Analytics |

</div>

---

## 📂 **Project Structure**

```
nasa-space-explorer/
├── src/
│   ├── pages/
│   │   ├── planet/
│   │   │   ├── planet.jsx          # Planet detail component
│   │   │   └── PlanetInfo.module.css
│   │   └── planetList/
│   │       ├── planetList.jsx      # Gallery component
│   │       └── list.css
│   ├── utils/
│   │   ├── contexts.js             # Theme & Language contexts
│   │   └── solarSystemData.js      # Planet data
│   ├── locales/
│   │   └── translations.js         # i18n translations
│   ├── App.jsx                     # Main component
│   ├── main.jsx                    # Entry point
│   ├── index.css                   # Global styles
│   └── page.module.css             # Page styles
├── index.html
├── package.json
├── vite.config.js
└── README.md
```

---

## 🌐 **API Integration**

### NASA APIs Used

#### 1. **APOD (Astronomy Picture of the Day)**
```javascript
https://api.nasa.gov/planetary/apod?api_key=YOUR_KEY
```
- Daily astronomy images and explanations
- Videos or images
- Free with API key (1000 requests/hour)

#### 2. **Solar System Data**
- Local dataset with comprehensive information
- 10 celestial bodies (Sun + 8 planets + Pluto)
- Multilingual descriptions

### Getting Your NASA API Key

1. Visit [api.nasa.gov](https://api.nasa.gov/)
2. Sign up for free
3. Replace `DEMO_KEY` in `src/pages/planet/planet.jsx`

---

## 🎨 **Design System**

### Color Palette

**Dark Theme (Default)**
```css
--bg-primary: #0a0e27     /* Deep space blue */
--bg-secondary: #1a1f3a   /* Nebula purple */
--accent-primary: #60a5fa /* Cosmic blue */
--accent-secondary: #a78bfa /* Stellar purple */
```

**Light Theme**
```css
--bg-primary: #f0f4f8     /* Soft gray */
--bg-secondary: #ffffff   /* Pure white */
--accent-primary: #3b82f6 /* Bright blue */
--accent-secondary: #8b5cf6 /* Vibrant purple */
```

### Typography

- **Headings**: Orbitron (Futuristic, space-themed)
- **Body**: Exo 2 (Modern, readable)

---

## 🌟 **Key Features Explained**

### Dark/Light Mode

The theme system uses:
- **React Context API** for global state
- **CSS Variables** for dynamic theming
- **localStorage** for persistence
- **Smooth transitions** between themes

```javascript
const { theme, toggleTheme } = useTheme();
```

### Internationalization

Custom i18n system with:
- **4 Languages**: English, French, Spanish, Italian
- **Context-based** language switching
- **Instant updates** across all components
- **localStorage persistence**

```javascript
const { language, changeLanguage } = useLanguage();
const t = (key) => getTranslation(language, key);
```

### Animated Starfield

Pure CSS animation creating a moving starfield:
```css
@keyframes twinkle {
  from { transform: translateY(0); }
  to { transform: translateY(-2000px); }
}
```

---

## 📊 **Performance Optimizations**

- ⚡ **Lazy Loading**: Images load only when visible
- 🔄 **useMemo**: Optimized filtering and sorting
- 📦 **Code Splitting**: React components loaded on demand
- 🎯 **SWC Compiler**: Ultra-fast compilation with Vite
- 💾 **LocalStorage Caching**: Theme and language preferences

---

## 🤝 **Contributing**

Contributions are welcome! Here's how:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 **License**

This project is licensed under the MIT License.

---

## 🙏 **Acknowledgments**

- 🚀 **[NASA](https://www.nasa.gov/)** for the amazing APIs and imagery
- ⚛️ **[React Team](https://reactjs.org/)** for the framework
- 🎨 **[PrimeReact](https://primereact.org/)** for UI components
- ⚡ **[Vite](https://vitejs.dev/)** for the blazing-fast build tool
- 🌌 **Space enthusiasts** worldwide for inspiration

---

## 📞 **Contact**

- **GitHub**: [@yourusername](https://github.com/yourusername)
- **Email**: your.email@example.com
- **Website**: [your-website.com](https://your-website.com)

---



**⭐ Star this repo if you find it helpful! ⭐**

![Space](https://media.giphy.com/media/3o7btPCcdNniyf0ArS/giphy.gif)

**Made with ❤️ and lots of ☕ for space exploration**

# planet
# planet
#   n a z a  
 