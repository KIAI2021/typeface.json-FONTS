# Typeface.json Fonts Collection

A collection of **1,395 fonts** converted to Three.js typeface.json format for 3D text rendering.

## 🚀 Quick Start

### Direct CDN Access (jsDelivr - Fastest)
```javascript
const fontUrl = 'https://cdn.jsdelivr.net/gh/KIAI2021/typeface.json-FONTS@main/fonts/Roboto-Regular.json';
const response = await fetch(fontUrl);
const fontData = await response.json();
const font = new THREE.FontLoader().parse(fontData);
```

### Raw GitHub (Always works)
```javascript
const fontUrl = 'https://raw.githubusercontent.com/KIAI2021/typeface.json-FONTS/main/fonts/ABeeZee-Regular.json';
```

### With GitHub Pages
```javascript
const fontUrl = 'https://kiai2021.github.io/typeface.json-FONTS/fonts/ABeeZee-Regular.json';
```

## 📚 Available Fonts

See [fonts/fonts-catalog.json](fonts/fonts-catalog.json) for the complete list of 1,395 fonts.

Sample fonts include:
- ABeeZee (Regular, Italic)
- Roboto (Multiple weights)
- Open Sans
- Lato
- Montserrat
- And 1,390+ more!

## 🎨 Usage with Three.js

```javascript
import * as THREE from 'three';
import { FontLoader } from 'three/examples/jsm/loaders/FontLoader.js';
import { TextGeometry } from 'three/examples/jsm/geometries/TextGeometry.js';

// Load font
const loader = new FontLoader();
const fontUrl = 'https://cdn.jsdelivr.net/gh/KIAI2021/typeface.json-FONTS@main/fonts/ABeeZee-Regular.json';

fetch(fontUrl)
  .then(response => response.json())
  .then(fontData => {
    const font = loader.parse(fontData);
    
    // Create 3D text
    const geometry = new TextGeometry('Hello 3D!', {
      font: font,
      size: 80,
      height: 5,
      curveSegments: 12,
      bevelEnabled: true,
      bevelThickness: 2,
      bevelSize: 1,
      bevelSegments: 5
    });
    
    const material = new THREE.MeshPhongMaterial({ color: 0x00ff00 });
    const mesh = new THREE.Mesh(geometry, material);
    scene.add(mesh);
  });
```

## 🔗 CDN URLs

### jsDelivr (Recommended - Fast CDN)
```
https://cdn.jsdelivr.net/gh/KIAI2021/typeface.json-FONTS@main/fonts/FONTNAME.json
```

### Raw GitHub
```
https://raw.githubusercontent.com/KIAI2021/typeface.json-FONTS/main/fonts/FONTNAME.json
```

### GitHub Pages (After enabling)
```
https://kiai2021.github.io/typeface.json-FONTS/fonts/FONTNAME.json
```

## 📦 Format

All fonts are in Three.js typeface.json format, compatible with:
- ✅ Three.js TextGeometry
- ✅ react-three-fiber
- ✅ Any Three.js-based 3D text rendering

## 🎯 Features

- **1,395 fonts** ready to use
- **Pre-converted** to typeface.json format
- **CDN delivery** via jsDelivr
- **No conversion needed** - just fetch and use
- **Validated** for 3D text rendering

## 📝 License

Fonts are subject to their original licenses. Please check individual font licenses before commercial use.

## 🛠️ Integration

This repository is designed to work with the 3D Text Generator app:
- Automatic font catalog loading
- Live preview before applying
- Search and category filtering
- On-demand font loading with caching

## 📊 Statistics

- **Total Fonts**: 1,395
- **Format**: typeface.json
- **Total Size**: ~500MB
- **Average Font Size**: ~350KB

## 🤝 Contributing

Found a font that doesn't work? Open an issue!

Want to add more fonts? Submit a PR with typeface.json files.

---

**Repository**: https://github.com/KIAI2021/typeface.json-FONTS  
**Created**: April 2026  
**Format**: Three.js typeface.json
