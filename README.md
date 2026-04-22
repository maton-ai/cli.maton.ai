# cli.maton.ai

Source for [cli.maton.ai](https://cli.maton.ai) — the Maton CLI manual and landing page.

The `manual/maton*.md` files are generated and committed by the release workflow in [maton-ai/cli](https://github.com/maton-ai/cli) (`.github/workflows/deployment.yml`). Don't edit them by hand — they'll be overwritten on the next release.

## Local development

```sh
bundle install
bundle exec jekyll serve
```

Then open http://127.0.0.1:4000.

## Deployment

GitHub Pages serves whatever is on the default branch. The `CNAME` file binds the site to `cli.maton.ai`. DNS is a `CNAME` record in Route 53 pointing `cli.maton.ai` → `maton-ai.github.io`.
