# ritvikrao.github.io

Personal academic website, built on the [Academic Pages](https://academicpages.github.io/) Jekyll template.

## Running locally

1. Make sure you have ruby-dev, bundler, and nodejs installed.

    On MacOS:
    ```bash
    brew install ruby
    brew install node
    gem install bundler
    ```
1. Run `bundle install` to install ruby dependencies. If you get errors, delete `Gemfile.lock` and try again.

    If you see a file permission error, install gems locally instead:
    ```bash
    bundle config set --local path 'vendor/bundle'
    bundle install
    ```
1. Run `jekyll serve -l -H localhost` (or `bundle exec jekyll serve -l -H localhost`) to build and serve the site at `localhost:4000`. It rebuilds automatically on changes to Markdown/HTML files; changes to `_config.yml` require restarting.

## Using Docker

You can also use the provided `Dockerfile` to run the site without installing Ruby/Node locally:

```bash
chmod -R 777 .
docker compose up
```

Then visit `localhost:4000`.

## Attribution

This site is based on [Academic Pages](https://github.com/academicpages/academicpages.github.io), maintained by Robert Zupko and originally forked by Stuart Geiger from the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) Jekyll theme (© 2016 Michael Rose, MIT License — see `LICENSE`).
