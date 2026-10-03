# Tools

A collection of simple, low-stakes web-based tools, inspired by [Simon Willison's tools page](https://tools.simonwillison.net/).

## Available Tools

### Playlist Cover Generator
**[https://tools.ben.report/playlist-covers.html](https://tools.ben.report/playlist-covers.html)**

Generate custom geometric playlist covers with a 4x4 grid of rotatable pattern tiles. Features:
- Interactive tile rotation (click any tile to rotate 90°)
- Customizable color palette with 8 preset color options
- Four configurable elements: background, two arc styles, and corner dots
- Export as 960x960 PNG images perfect for music streaming services
- Real-time preview with responsive design

### Recipe Tracker
**[https://tools.ben.report/recipes.html](https://tools.ben.report/recipes.html)**

Plan your weekly meals with an interactive meal planning interface. Features:
- Weekly meal grid for lunch and dinner across 7 days
- Meal database with protein categorization
- Track ingredients for each meal
- Visual meal summary showing serving counts
- Export/import functionality for both meal database and weekly plans
- Dark mode support
- Persistent storage using localStorage

### Chromecast Screensaver Crop Tool
**[https://tools.ben.report/chromecast-screensaver-crop.html](https://tools.ben.report/chromecast-screensaver-crop.html)**

Prepare photos for perfect Chromecast Ambient Mode display by adding letterboxing. Features:
- Upload and process photos for Chromecast screensaver display
- Configurable aspect ratios (16:9, 4:3, custom)
- Smart letterboxing with customizable blur and brightness
- Live preview with dimension calculations
- Download processed images ready for Chromecast
- Handles various input image sizes and orientations

### EPUB LOC Estimator
**[https://tools.ben.report/epub-locs.html](https://tools.ben.report/epub-locs.html)**

Estimate Amazon Kindle Location (LOC) numbers for EPUB files. Features:
- Upload EPUB files for analysis
- Calculate estimated LOC count based on character count
- Display book metadata (title, author, publisher)
- Chapter-by-chapter breakdown with LOC ranges
- Searchable LOC lookup to find specific locations
- Export chapter breakdown as CSV

### JPEG → WebP Converter
**[https://tools.ben.report/jpeg-to-webp.html](https://tools.ben.report/jpeg-to-webp.html)**

Batch-convert JPEGs (and PNGs) to WebP entirely in the browser. Features:
- Drag-and-drop or select multiple images at once
- Output multiple sizes per image (400px thumb, 1200px medium, 2400px full)
- Quality-controlled, high-quality step-down resizing (never enlarges)
- Per-file results table showing dimensions and size savings
- Download all converted files as a single `.zip`
- Generates a responsive `srcset` snippet for the converted images

### Swim FIT Editor
**[https://tools.ben.report/swim-fit-editor.html](https://tools.ben.report/swim-fit-editor.html)**

Correct pool swims recorded by a Garmin watch, then download a fixed `.fit` file. Features:
- Horizontally scrollable column chart of every length (height = length time, colour = stroke), grouped by interval with rests marked
- Change the stroke of one or many lengths (freestyle, breaststroke, backstroke, butterfly, drill)
- Split a length into two equal lengths where the watch missed a turn
- Merge neighbouring lengths where the watch counted a turn that didn't happen
- Recalculates interval and activity totals (distance, length counts, pace, SWOLF, strokes per length)
- Undo, reset, and a change log; all other data in the file is preserved byte-for-byte

## Getting Started

Each tool is a standalone HTML file that can be opened directly in a web browser. No installation or build process required.

Simply open any of the HTML files in your browser to start using the tool.

## Hosting

These tools are hosted at [tools.ben.report](https://tools.ben.report).
