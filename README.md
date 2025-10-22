# jmatthiesen.github.io
My personal website.

## Build & preview locally

Quick steps to get the site building and previewing on your machine.

Prerequisites
- Ruby (recommended 2.7+)
- Bundler (gem)

This repository uses the `github-pages` gem (see `Gemfile`) for GitHub Pages compatibility. We use Bundler to install and run the correct gem versions.

Install dependencies
```bash
brew install bundler     # if you don't already have bundler
bundle install
```

Build the site
```bash
# Build into the `_site/` folder
bundle exec jekyll build
```

Serve locally with live reload
```bash
# Start a local preview at http://127.0.0.1:4000
bundle exec jekyll serve --livereload
```

Include drafts and future-dated posts
```bash
# Show draft posts and posts dated in the future as well
bundle exec jekyll serve --drafts --future --livereload

# Or build only with drafts/future included:
bundle exec jekyll build --drafts --future
```

Docker (optional)
```bash
# If you prefer to run via Docker (no Ruby install required):
docker run --rm -v "$(pwd)":/srv/jekyll -it -p 4000:4000 jekyll/jekyll:4 jekyll serve --watch --drafts --future --livereload
```

Notes
- If you run into native gem install errors, make sure you have a working Ruby development toolchain (build-essential, libssl-dev, zlib1g-dev, etc.) installed for your OS.
- On Windows, the `wdm` gem is used to improve file watching; it is included conditionally in the `Gemfile`.

If you'd like I can also add a small Makefile or npm scripts to make these commands shorter.
# jmatthiesen.github.io
My personal website.
