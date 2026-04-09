# Local Preview

For local preview of this Jekyll site, always start the server with the local config override so that CSS, images, and other static assets are loaded from `localhost` instead of the production domain.

Use this command:

```bash
PATH=$HOME/.gem/ruby/2.6.0/bin:$PATH bundle _2.4.22_ exec jekyll serve -H localhost --port 4000 --config _config.yml,_config_local.yml
```

Notes:

- Use this command for local development in this repository.
- Do not start local preview with plain `bundle exec jekyll serve`.
- The `_config_local.yml` override is required for correct local asset loading.
