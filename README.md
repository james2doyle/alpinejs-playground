# Alpine Playground

![screenshot.png](screenshot.png)

A live coding playground for [Alpine.js](https://alpinejs.dev/) with Tailwind CSS support. Write, test, and share Alpine.js components in real-time with an interactive split-pane interface.

## Features

- **Live Preview**: See your Alpine.js code render instantly as you type
- **Code Sharing**: Generate shareable URLs with compressed code
- **Resizable Panes**: Adjust the editor/preview split to your preference
- **Tailwind CSS Support**: Full Tailwind CSS utility classes available
- **One-Click Actions**: Copy code, reset to default, and save with URL updates

## Technologies

- **Alpine.js 3.x**: Lightweight JavaScript framework
- **Tailwind CSS**: Utility-first CSS framework
- **JsonUrl**: For URL-safe code compression
- **HTML5**: Modern web standards

## Usage

### Online Usage

1. [Visit the playground](https://james2doyle.github.io/alpinejs-playground/) in your browser
2. Write Alpine.js code in the left editor pane
3. See live results in the right preview pane
4. Use the toolbar buttons:
   - **Reset**: Clear code and start fresh
   - **Copy**: Copy your code to clipboard
   - **Save**: Generate a shareable URL

### Sharing Code

The playground automatically generates shareable URLs when you click "Save". The code is compressed using JsonUrl's LZMA algorithm and stored in the URL parameter `?s=...`.

## Development

To run this playground locally:

1. Clone this repository
2. Open `docs/index.html` in your browser
3. No build step required - it runs entirely in the browser
