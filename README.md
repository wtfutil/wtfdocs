# wtfdocs

A documentation and browser management tool built with Tauri.

## Features

- Browser discovery and management
- Cross-platform support (Windows, macOS, Linux)
- Built with Rust and Tauri

## Documentation

For detailed information, see the [docs](./docs) folder.

### Core Documentation
- **[Browser Discovery Overview](./docs/browser-discovery-overview.md)** - Complete guide to how browser discovery works
  - Frontend to Rust backend communication flow
  - Tauri command implementation
  - Platform-specific filesystem access
  - Interactive mermaid sequence diagrams
  - Windows troubleshooting and edge cases
  
- **[Documentation Index](./docs/README.md)** - Full documentation navigation and quick links

## Getting Started

```bash
# Install dependencies
npm install

# Run development server
npm run tauri dev

# Build for production
npm run tauri build
```

## Development

This project uses:
- **Tauri** - Desktop app framework
- **Rust** - Backend logic
- **React/Vue** - Frontend UI

## Contributing

Contributions are welcome! Please see the [Contributing Guidelines](./CONTRIBUTING.md).

## License

[Your License Here]

# WTF Docs

This site is built using [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

### Development environment setup

1. Install python 3
2. Create a virtual-env:
```bash
python -m venv virtual-env
source virtual-env/bin/activate
```
3. `pip install -r requirements.txt`
4. `mkdocs serve`

### To add documentation for a new module

1. Create a new [Markdown](https://guides.github.com/features/mastering-markdown/) file in the `/docs/modules` directory
2. Add a new route in the `mkdocs.yml` file, under the `nav:` section.
3. To add pictures, add the image to `./docs/overrides/assets/modules/<IMAGE>.png`

### Deploying

* Merge changes into `master`
* Run `mkdocs gh-deploy --force` to push the changes to the `gh-pages` branch on github.com
* Commit the resulting changes into `master`
