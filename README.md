# Google Slides Clone - GitHub Pages Presentation

A web-based presentation tool that mimics Google Slides functionality, built with Reveal.js and designed to be hosted on GitHub Pages.

## 🚀 Features

- **Custom Images and Text**: Add your own images and customize text for each slide
- **Unique Audio Per Slide**: Each slide can have its own background music, sound effects, or narration
- **Presentation Mode**: Full-screen presentation with keyboard navigation
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Easy Hosting**: Deployable to GitHub Pages with zero configuration
- **Keyboard Controls**: Navigate with arrow keys, press F for fullscreen

## 📁 Project Structure

```
your-repo/
├── index.html          # Main presentation file
├── audio/              # Audio files for each slide
│   ├── slide1.mp3
│   ├── slide2.mp3
│   ├── slide3.mp3
│   ├── slide4.mp3
│   └── slide5.mp3
├── images/             # Image assets
│   ├── welcome.jpg
│   ├── project.jpg
│   ├── features.jpg
│   ├── demo.jpg
│   └── thankyou.jpg
└── README.md          # This file
```

## 🛠️ Setup Instructions

### Option 1: Quick Setup (Recommended)

1. **Create a new GitHub repository**
   - Go to GitHub and create a new repository
   - Name it something like `my-presentation` or `slides`

2. **Upload the files**
   - Upload the `index.html` file to your repository
   - Create `audio/` and `images/` folders
   - Upload your audio and image files to respective folders

3. **Enable GitHub Pages**
   - Go to Settings → Pages in your repository
   - Select "Deploy from branch"
   - Choose "main" branch and "/ (root)" folder
   - Click Save

4. **Access your presentation**
   - Your presentation will be available at: `https://yourusername.github.io/your-repo-name`

### Option 2: Local Development

1. **Clone this repository**
   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
   ```

2. **Serve locally**
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Python 2
   python -m SimpleHTTPServer 8000
   
   # Using Node.js
   npx http-server
   ```

3. **Open in browser**
   - Visit `http://localhost:8000`

## 🎵 Adding Audio Files

1. **Supported formats**: MP3, WAV, OGG, AAC, M4A
2. **File naming**: Use descriptive names (e.g., `slide1.mp3`, `intro-music.mp3`)
3. **File size**: Keep files under 10MB for faster loading
4. **Placement**: Put all audio files in the `audio/` folder

### Adding Audio to a Slide

In `index.html`, add the `data-audio` attribute to any slide:

```html
<section data-audio="audio/your-audio-file.mp3">
    <!-- Slide content -->
</section>
```

## 🖼️ Adding Images

1. **Supported formats**: JPG, PNG, GIF, WebP, SVG
2. **Recommended size**: 1920x1080 or smaller for web optimization
3. **Placement**: Put all images in the `images/` folder

### Adding Images to a Slide

```html
<section>
    <div class="slide-content">
        <h2>Your Title</h2>
        <img src="images/your-image.jpg" alt="Description">
        <p>Your text content</p>
    </div>
</section>
```

## 🎮 Controls

- **Arrow Keys**: Navigate between slides
- **F Key or F11**: Enter fullscreen presentation mode
- **Esc**: Exit fullscreen
- **Space**: Next slide
- **Shift + Space**: Previous slide

## 🎨 Customization

### Themes

Change the theme by modifying the CSS link in `index.html`:

```html
<!-- Available themes: black, white, league, beige, sky, night, serif, simple, solarized -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@4.6.1/dist/theme/black.css">
```

### Custom Styling

Modify the `<style>` section in `index.html` to customize:
- Colors and fonts
- Layout and spacing
- Animation effects
- Audio player appearance

### Adding New Slides

Add a new slide by inserting a `<section>` element:

```html
<section data-audio="audio/slide6.mp3">
    <div class="slide-content">
        <h2 class="slide-title">New Slide Title</h2>
        <img src="images/new-image.jpg" alt="New Image">
        <p class="slide-text">Your slide content here</p>
    </div>
</section>
```

## 🌐 Browser Compatibility

- **Chrome**: Full support
- **Firefox**: Full support
- **Safari**: Full support
- **Edge**: Full support
- **Mobile browsers**: Responsive design works on all modern mobile browsers

**Note**: Audio autoplay policies vary by browser. Users may need to interact with the page before audio starts playing automatically.

## 🔧 Advanced Features

### Auto-advancing Slides

To automatically advance slides after audio finishes:

```javascript
slideAudio.addEventListener('ended', function() {
    Reveal.next();
});
```

### Custom Transitions

Add different transition effects:

```javascript
Reveal.initialize({
    transition: 'slide', // none/fade/slide/convex/concave/zoom
    transitionSpeed: 'default' // default/fast/slow
});
```

### Speaker Notes

Add speaker notes that only you can see:

```html
<section>
    <h2>Slide Title</h2>
    <p>Slide content</p>
    <aside class="notes">
        These are speaker notes. Only visible in speaker view.
    </aside>
</section>
```

## 📱 Mobile Optimization

The presentation is fully responsive and works well on:
- Smartphones (portrait and landscape)
- Tablets
- Desktop computers
- Large displays

Touch gestures are supported for slide navigation on mobile devices.

## 🚨 Troubleshooting

### Audio Not Playing
- Check file paths are correct
- Ensure audio files are in the correct format
- Some browsers require user interaction before playing audio
- Check browser console for error messages

### Images Not Loading
- Verify image file paths
- Check image file formats are supported
- Ensure images are not too large (>5MB)

### GitHub Pages Not Working
- Check repository settings
- Ensure `index.html` is in the root directory
- Wait a few minutes after enabling Pages
- Check the Actions tab for build errors

## 🤝 Contributing

1. Fork this repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- [Reveal.js](https://revealjs.com/) - The HTML Presentation Framework
- [GitHub Pages](https://pages.github.com/) - Free hosting for the presentation
- [Font Awesome](https://fontawesome.com/) - Icons (if you choose to add them)

---

**Happy Presenting! 🎬**

For questions or support, please open an issue in this repository.
