# WTF Docs

This site is built using [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

To add documentation for a new module, create a new [Markdown](https://guides.github.com/features/mastering-markdown/) file 
in the `/docs/modules` directory, and add a new route in the `mkdocs.yml` file, under the `nav:` section.

### Deploying

* Merge changes into `master`
* Run `mkdocs gh-deploy --force` to push the changes to the `gh-pages` branch on github.com
* Commit the resulting changes into `master`
