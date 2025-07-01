# UWP Icon Generator

A pure client-side JavaScript web tool that generates all default UWP (Universal Windows Platform) tile icons in PNG, JPEG, and SVG formats from a single uploaded image. It displays the tiles in a responsive grid layout and allows individual or batch downloads (ZIP).

## Features

* **UWP Default Tiles**: Generates StoreLogo, Square44x44Logo, Square71x71Logo, Square150x150Logo, Wide310x150Logo, Square310x310Logo, BadgeLogo, and SplashScreen.
* **Multiple Formats**: Outputs PNG, JPEG (quality 0.9), and SVG for each tile size.
* **Responsive Grid**: Tailwind CSS grid layout for a clean, modern UI.
* **Individual Downloads**: Download buttons for each format under each tile.
* **Batch Download**: "Download All as ZIP" packs all generated files into a ZIP archive using JSZip and FileSaver.js.
* **Pure Client-Side**: No backend required; works entirely in the browser.

## Getting Started

### Prerequisites

* Modern web browser (Chrome, Firefox, Edge, Safari).

### Installation

1. Clone or download the repository.
2. Place `index.html` in your project directory.
3. Ensure you have internet access or provide local copies for:

   * [Tailwind CSS 2.x](https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css)
   * [JSZip](https://cdnjs.cloudflare.com/ajax/libs/jszip/3.7.1/jszip.min.js)
   * [FileSaver.js](https://cdnjs.cloudflare.com/ajax/libs/FileSaver.js/2.0.5/FileSaver.min.js)

### Usage

1. Open `index.html` in your browser.
2. Click the file input and select your source logo image (PNG, JPEG, SVG, etc.).
3. Wait for the tool to generate all tile variants.
4. Download individual icons by clicking the format buttons under each tile.
5. Click **Download All as ZIP** to get a ZIP archive of all generated files.

## File Structure

```
project-root/
│
├── index.html       # Main HTML, CSS & JS file
└── README.md        # Project documentation
```

## Customization

* **Adding Custom Tiles**: In `index.html`, modify the `tiles` array with additional `{ name, width, height }` objects.
* **Image Quality**: Adjust the JPEG quality parameter in the `canvas.toDataURL('image/jpeg', 0.9)` call.
* **Styling**: Tweak Tailwind utility classes or replace with your own CSS.

## Dependencies

* [Tailwind CSS](https://tailwindcss.com/)
* [JSZip](https://stuk.github.io/jszip/)
* [FileSaver.js](https://github.com/eligrey/FileSaver.js)

## License

This project is released under the [MIT License](https://opensource.org/licenses/MIT).
