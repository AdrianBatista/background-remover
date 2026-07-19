# Background Remover

A browser-based tool that removes an image background and exports the result as a transparent PNG. Processing happens locally in the browser; the selected image is not uploaded to an application server.

## Features

- Accepts image files through file selection or drag and drop.
- Previews the source image and transparent result.
- Uses IMG.LY's `@imgly/background-removal` model in the browser.
- Uses WebGPU when available and falls back to CPU processing.
- Downloads the generated result as a PNG.
- Includes English and Portuguese UI text.

## Run locally

This is a static HTML, CSS, and ES-module application. Serve it over HTTP; opening `index.html` with `file://` will not load the modules correctly.

```bash
npx serve .
```

The current page is integrated with the [personal-site](https://github.com/AdrianBatista/personalsite) design system and imports shared assets from absolute paths such as `/css/main.css` and `/js/i18n.js`. To run it exactly as shipped, initialize the parent repository's submodules and serve that repository root:

```bash
git clone --recurse-submodules https://github.com/AdrianBatista/personalsite.git
cd personalsite
npx serve .
```

Then open `/projects/background-remover/`.

## Dependencies

The background-removal library, ONNX Runtime, and model assets are loaded from jsDelivr on first use. The browser may cache them for later use.

## Documentation

The in-site technical article is available at `article.html` when served through the parent site.

## License

Not yet specified.
