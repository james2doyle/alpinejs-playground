# Alpine Playground

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

1. Visit the playground in your browser
2. Write Alpine.js code in the left editor pane
3. See live results in the right preview pane
4. Use the toolbar buttons:
   - **Reset**: Clear code and start fresh
   - **Copy**: Copy your code to clipboard
   - **Save**: Generate a shareable URL

### Sharing Code

The playground automatically generates shareable URLs when you click "Save". The code is compressed using JsonUrl's LZMA algorithm and stored in the URL parameter `?s=...`.

### Custom Alpine Magic Properties

The playground includes two custom Alpine.js magic properties:

#### `$clipboard(text)`

Copy text to the clipboard:

```javascript
@click="$clipboard('Text to copy')"
```

#### `$confirm(message)`

Show a confirmation dialog:

```javascript
@click="$confirm('Are you sure?').then(() => doSomething())"
```

## Development

To run this playground locally:

1. Clone this repository
2. Open `index.html` in your browser
3. No build step required - it runs entirely in the browser

## Example Code

Here's a simple counter example to get you started:

```html
<div x-data="{ count: 0 }" class="p-8 text-center font-sans">
    <h1 class="text-4xl font-bold mb-4" x-text="count"></h1>

    <div class="flex gap-2 justify-center">
        <button
            @click="count--"
            class="px-4 py-2 bg-slate-200 rounded hover:bg-slate-300 transition"
        >Decrease</button>

        <button
            @click="count++"
            class="px-4 py-2 bg-blue-600 text-white rounded hover:bg-blue-700 transition"
        >Increase</button>
    </div>

    <p class="mt-4 text-slate-500 text-sm italic" x-show="count > 10">
        That's a lot of clicks!
    </p>
</div>
```

## License

This project is open source and available for personal and commercial use.
