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
