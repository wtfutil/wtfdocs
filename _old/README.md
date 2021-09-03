# WTF Documentation

This is the documentation repository for [WTF](https://github.com/wtfutil/wtf), the terminal-based dashboard utility written in [Go](https://golang.org). The output of this repository is [https://wtfutil.com](https://wtfutil.com).

This documentation is built atop [Hugo](https://gohugo.io), the static site generator, and served up by GitHub pages.

## Adding or Editing Documentation

### Adding a New Module
Documentation for new modules should be added into the `content/modules/` directory. Each new module is defined in a single Markdown file.

Name the Markdown file as logically as possible. If the module adds a new service to the collection, name it after the service (ie: `twitter.md`, `shopify.md`). If it adds a new capability, try to name it as simply as possible, ideally using a single word (ie: `clocks.md`, `security.md`). The file must end in the `.md` extension.

### Content Format
Documentation is written in [GitHub Markdown](https://guides.github.com/features/mastering-markdown/). 

## Local Development
Contributions and pull requests are absolutely welcome. Please feel free to improve, expand, and fix this documentation by opening pull requests against this repository.

### Running Locally
To run the documentation locally: 

1. `cd` into the root directory of this repository
2. Execute `hugo server` in the terminal. You'll see a bunch of output including the following lines:
	
	{{< code lang="bash" >}}
	Serving pages from memory
	Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
	Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
	Press Ctrl+C to stop
	```

3. Open [http://localhost:1313/](http://localhost:1313/) in your browser

You should now be looking at the local development instance of the WTF documentation.

### Building Locally
Because this site is statically-generated, any time you make changes you'll need to rebuild the static pages (which live in the `/docs` directory). **Do not** make changes directly to files in the `/docs` directory, because they won't be persisted, they'll be over-written on the next build.

To rebuild the static site:

1. `cd` into the root directory of this repository
2. Execute `hugo` in the terminal. This step compiles the static site

Now if you `git status`, you should see a list of changed or created `.html` files waiting to be committed.