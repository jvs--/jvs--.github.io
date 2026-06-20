github page based on the Jekyll implementation of the [Creative Theme](http://startbootstrap.com/template-overviews/creative/) template by [Start Bootstrap](http://startbootstrap.com).

## Run locally

The site is built with Jekyll and runs inside Docker, so nothing (Ruby, gems)
is installed on your machine. This mirrors how GitHub Pages builds it.

**Every time** (from the repo root):

```bash
colima start          # start the Docker engine
docker compose up     # build + serve the site
```

Wait for `Server running... http://0.0.0.0:4000/`, then open
<http://localhost:4000>. Source edits live-reload in the browser.

**To stop:** `Ctrl-C`, then `docker compose down`, then `colima stop`.

First run downloads an image and installs gems (a few minutes); later runs are
fast.

### One-time setup (first machine, or after a fresh OS)

```bash
brew install colima docker docker-compose
```

If `docker compose` is not found afterward, register the plugin by adding this
to `~/.docker/config.json`:

```json
"cliPluginsExtraDirs": ["/opt/homebrew/lib/docker/cli-plugins"]
```
