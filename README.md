# ⌚ Realme Watch – Analog Clock

A minimal analog clock that shows the **real-time local time** with smoothly rotating hour, minute and second hands. Built with plain HTML, CSS and JavaScript – no frameworks, no dependencies.

🔗 **Live Demo:** [mkkapadi12.github.io/realmewatch](https://mkkapadi12.github.io/realmewatch/)

<!-- Add a screenshot after saving it as screenshot.png -->
<!-- ![Realme Watch preview](screenshot.png) -->

## ✨ Features

- Real-time analog clock synced with your system time
- Separate hour, minute and second hands with distinct styling (minute hand in accent blue `#10b9ff`)
- Realme-style watch dial rendered from a background image
- Circular face with soft inner/outer shadows for a 3D look
- Centered, dark-themed layout (`#091921`)
- Zero dependencies – opens directly in any browser

## 🛠️ Tech Stack

| Technology | Usage |
| ---------- | ----- |
| HTML5 | Page structure |
| CSS3 | Clock face, hands, shadows, layout (Flexbox) |
| JavaScript (ES6) | Time calculation and hand rotation |

## 📁 Project Structure

```
realmewatch/
├── index.html    # Markup + embedded CSS for the clock
├── script.js     # Clock logic (hand rotation)
├── clock.png     # Dial background image
└── README.md
```

## 🚀 Getting Started

No installation or build step needed.

```bash
# 1. Clone the repository
git clone https://github.com/mkkapadi12/realmewatch.git

# 2. Go to the project folder
cd realmewatch

# 3. Open index.html in your browser
```

Optional: use VS Code **Live Server** for auto-reload while editing.

## ⚙️ How It Works

`script.js` reads the current time with `new Date()` and converts it to rotation angles:

| Hand | Formula |
| ---- | ------- |
| Hour | `hours × 30° + minutes ÷ 12` |
| Minute | `minutes × 6°` |
| Second | `seconds × 6°` |

Each angle is applied to its hand with a CSS `rotateZ()` transform inside a `setInterval` loop.

## 🎨 Customization

- **Dial image:** replace `clock.png` with your own watch face.
- **Size:** change `width` / `height` of `.clock` in `index.html`.
- **Hand colors / thickness:** edit `.hr::before`, `.min::before`, `.sec::before`.
- **Background:** change the `body` background color.

## 🔮 Future Improvements

- [ ] Digital time and date display
- [ ] Light / dark theme toggle
- [ ] Multiple time zones
- [ ] Smooth sweeping second hand animation
- [ ] Responsive scaling for small screens

## 📚 What I Learned

- DOM manipulation with `getElementById`
- CSS transforms and pseudo-elements (`::before`)
- Working with the JavaScript `Date` object
- Deploying a static site on GitHub Pages

## 👤 Author

**Mayur Kapadi**

- GitHub: [@mkkapadi12](https://github.com/mkkapadi12)
- Email: mayurkapadi12@gmail.com

---

⭐ If you like this project, consider giving it a star!
