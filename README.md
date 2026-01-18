# James Saiba - Professional Portfolio

A premium, high-performance personal portfolio website showcasing software development projects, data analysis expertise, and creative works in photography and graphic design.

## 🎨 Features

-   **"Aurora" UI Theme**: A custom-designed dark aesthetic with animated gradients, glassmorphism, and "living" hover effects.
-   **Responsive Design**: Fully optimized for mobile, tablet, and desktop viewports.
-   **Interactive Elements**:
    -   Custom image slider for Graphic Design projects.
    -   Reveal-on-scroll animations.
    -   Dark/Light mode toggle (Persistent preference).
-   **Asset Organization**: Structured directory for manageable project assets.

## 📂 Project Structure

```
portfolio/
├── index.html          # Main application file
├── README.md           # Documentation
└── assets/
    ├── cv/             # Resume/CV files
    └── images/         # Static assets
        ├── profile/    # Personal profile shots
        ├── softlink/   # Professional experience images
        └── projects/   # Project screenshots and gallery images
```

## 🚀 Performance Optimization Guide

To ensure this portfolio loads instantly and provides a smooth experience, I found the following specific optimizations relevant to this codebase:

### 1. Image Optimization (Critical)
The current `assets` folder contains full-resolution images.
*   **Recommendation**: Convert all `.jpg` and `.png` images to **WebP** format. This typically reduces file size by 30-50% with no loss in quality.
*   **Tool**: Use [Squoosh.app](https://squoosh.app/) or a bulk converter.
*   **Code Update**: Change `src="image.jpg"` to `src="image.webp"` in `index.html` after conversion.

### 2. Lazy Loading
Images below the "fold" (not visible when the page first loads) should not block the initial render.
*   **Action**: I have added `loading="lazy"` to project images, but ensure any new images added also include this attribute.
    ```html
    <img src="..." loading="lazy" alt="...">
    ```

### 3. Font Loading
We are using Google Fonts (Outfit).
*   **Current Status**: We are correctly using `preconnect` to `fonts.gstatic.com`, which speeds up the handshake.
*   **Optimization**: Ensure `font-display: swap;` is used (default for Google Fonts) so text is visible immediately even if the custom font is still downloading.

### 4. Minification
For the final deployment (production), "minify" the code to remove spaces and comments.
*   **Impact**: Reduces `index.html` size.
*   **Tools**: Use an online HTML/CSS/JS minifier before uploading to your host.

## 🛠️ Setup & Editing

1.  **Editing Content**: Open `index.html` in any text editor (VS Code recommended).
2.  **Adding Images**: Place new images in the relevant `assets/images/` subfolder and update the `src` path in the HTML.
3.  **Viewing Locally**: Simply double-click `index.html` to open it in your browser.

## 🔗 Links

-   **GitHub**: [mufasa-james](https://github.com/mufasa-james)
-   **LinkedIn**: [James Saiba](https://www.linkedin.com/in/james-saiba-ke/)
