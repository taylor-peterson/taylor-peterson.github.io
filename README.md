1. Install Docker and docker-compose
2. Run `docker-compose up`
3. Visit http://0.0.0.0:4000

# Acknowledgements

* Theme based on [jekyll-clean](https://github.com/scotte/jekyll-clean)

# Notes
* Global permalink configuration doesn't work locally (i.e. urls will have
  ".html" appended to them.
* GitHub pages (reasonably) uses the "--safe" option to disable custom plugins
  so they're not executing arbitrary ruby code on their servers. Moreover, the
  set of supported plugins is rather sparse and the alternative of generating
  the site locally and pushing the output instead of the source is distasteful.
