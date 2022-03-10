# tech-writing-samples
This is the markdown for my [technical writing sample site](https://samples.jamesteitsworth.com).

## Build the site
The site is built using [mdBook](https://rust-lang.github.io/mdBook/). If you need to build it for any reason:
1. Setup mdBook by following the [mdBook installation guide](https://rust-lang.github.io/mdBook/guide/installation.html)
2. Once mdBook is installed, clone this project
3. From your terminal run:

```bash
# To run it locally
cd /to/repo/folder
mdbook serve --open
```

```bash
# To build the static files for deployment
cd /to/repo/folder
mdbook build
```
