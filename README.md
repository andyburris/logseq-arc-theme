# logseq-arc-theme
A Logseq theme based on Arc by The Browser Company

### Screenshots 
(last updated v0.1)
![Journals screenshot](arc-light-journals.png)
![Page screenshot](arc-light-demo.png)

### Installation
**Marketplace**

Find Arc Theme in the Logseq theme marketplace within the app.

**Manual installation**

Copy `custom.css` into `logseq/custom.css` or paste this line into `logseq/custom.css`:
```css
@import url('https://cdn.jsdelivr.net/gh/andyburris/logseq-arc-theme/custom.css');
```

### Customization
Currently, the following options (shown here with their default values) are available to customize the view, which you can put into your own `custom.css`
```scss
:root {
    --display-pdf-arrows: none; // toggles whether the page up/down arrows are available in the PDF viewer
}
```

Also, Arc Theme uses a simplified palette of colors that's applied throughout the app. You can still customize the individual Logseq variables (e.g. `--ls-primary-text-color`) if fine-grained control is needed, but to change theme-wide colors, use these variables (shown with default values):
```scss
.white-theme, html[data-theme=light] {
  --arc-background-shell: #F2F2F2;
  --arc-background-card: #FFFFFF;
  --arc-background-overlay: rgba(0, 0, 0, 0.05);
  --arc-background-glass: rgba(255, 255, 255, 0.85);
  --arc-content-primary: rgba(0, 0, 0, 0.80);
  --arc-content-secondary: rgba(0, 0, 0, 0.5);
  --arc-content-tertiary: rgba(0, 0, 0, 0.25);
  --arc-content-divider: rgba(0, 0, 0, 0.12);
  --arc-accent-primary: hsla(206, 75%, 50%, 0.98);
}

.dark-theme, html[data-theme=dark] {
  --arc-background-shell: #191919;
  --arc-background-card: #272727;
  --arc-background-overlay: rgba(255, 255, 255, 0.07);
  --arc-background-glass: rgba(35, 35, 35, 0.85);
  --arc-content-primary: rgba(255, 255, 255, 0.83);
  --arc-content-secondary: rgba(255, 255, 255, 0.5);
  --arc-content-tertiary: rgba(255, 255, 255, 0.25);
  --arc-content-divider: rgba(255, 255, 255, 0.12);
  --arc-accent-primary: hsla(206, 75%, 50%, 1);
}
```

### Roadmap
Generally, I want to really polish each surface before moving on to the next one. Also, I will mainly be updating this theme as I find the need to, so progress might be slow. In the meantime, there will probably be a lot of screens that are very default-looking (and maybe broken). 

All planned improvements are in the issues, and if you have ideas or bugs, feel free to open a new issue, and I'll try to make it happen.

### Building
1. Install [Sass](https://sass-lang.com/)
2. `sass --watch custom.scss custom.css`
3. Edit `custom.scss`
