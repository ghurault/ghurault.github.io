# Personal website

Code to generate my personal website, hosted at <https://ghurault.github.io/>.

The website is generated with [Hugo Blox](https://hugoblox.com/) — the
[Academic CV](https://github.com/HugoBlox/hugo-theme-academic-cv) template, built on
the [Hugo Blox Kit](https://github.com/HugoBlox/kit) `blox` module — and
[Hugo Extended](https://gohugo.io/).

- [Documentation](https://docs.hugoblox.com/)
- [Kit release notes](https://github.com/HugoBlox/kit/releases)

## Note-to-self

### Development

Everything runs in the devcontainer (`.devcontainer/`), so no Hugo, Go, Node or pnpm
installation is needed on the host. Open the folder in VS Code and _Reopen in
Container_, then:

```bash
pnpm run dev
```

That runs `hugo server --disableFastRender` on <http://localhost:1313>.

The devcontainer image is built from `docker.io/hugomods/hugo:debian-<version>`, which
already ships Hugo Extended, Go, Node and git, with pnpm added on top.

Two version pins have to be kept in step by hand:

| File                       | Key                                      |
| -------------------------- | ---------------------------------------- |
| `hugoblox.yaml`            | `build.hugo_version` — what CI installs  |
| `.devcontainer/Dockerfile` | the `hugomods/hugo:debian-<version>` tag |

> [!WARNING]
> Do not use Hugo **0.162.0** (which is what the upstream template pins). In that
> release `dict` returns a nil map when called with no arguments, and the `blox`
> module relies on `(dict)` in `functions/build_links.html`, so every page with a
> `links` entry fails to render. Fixed in 0.163.0.

To work outside VS Code, the same environment is available directly:

```bash
docker build -t hugoblox-dev .devcontainer
```

then run commands in it with
`docker run --rm -it -v "${PWD}:/workspaces/personal-website" -w /workspaces/personal-website -p 1313:1313 hugoblox-dev sh`.
Note the nested working directory: Hugo refuses to run from a path that is itself a
mount point.

### Editing the content

- The **homepage** is assembled from the `sections:` list in
  [`content/_index.md`](content/_index.md). Each entry is a _blox_ (block); the
  available blocks live in the Kit module under `modules/blox/blox/`.
- **Publications**, **projects** and **events** are page bundles under
  [`content/publications`](content/publications),
  [`content/projects`](content/projects) and [`content/events`](content/events).
- The **profile** (name, role, bio, education, interests, social links) is
  [`data/authors/admin.yaml`](data/authors/admin.yaml), not a content page. The avatar is
  `assets/media/authors/admin.jpeg` — the filename must match the author slug.
- Site configuration is in [`config/_default/`](config/_default), using the
  `hugoblox` schema 2.0 tree in `params.yaml`.

Two things are worth knowing before editing:

- **Search is Pagefind**, and its index is only built after a full Hugo build. So the
  search box finds nothing under `pnpm run dev`. To check it, run
  `pnpm run build` (`hugo --minify` followed by `pnpm run pagefind`).
- **Projects deliberately keep `external_link`.** It makes a project card link
  straight to the project instead of to a near-empty detail page. Hugo Blox prints a
  deprecation warning for it on every build, but the card view still treats the field
  as first class, so the warnings are expected noise rather than something to fix.
  Switching to `links: [{type: site, url: ...}]` would silence them at the cost of
  that behaviour.

### Deployment

`main` is deployed to GitHub Pages by
[`.github/workflows/deploy.yml`](.github/workflows/deploy.yml), which calls
[`build.yml`](.github/workflows/build.yml) and publishes over OIDC — no access token
required. `build.yml` also runs on pull requests as a build check.

[`upgrade.yml`](.github/workflows/upgrade.yml) opens a weekly pull request that bumps
the Hugo Blox modules and applies any content migrations. It needs
_Settings → Actions → General → Allow GitHub Actions to create and approve pull
requests_ to be enabled.

## License

Copyright 2017-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/HugoBlox/theme-academic-cv/blob/main/LICENSE.md) license.
