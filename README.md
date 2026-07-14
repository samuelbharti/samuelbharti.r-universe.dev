# samuelbharti.r-universe.dev

This is my personal [R-universe](https://r-universe.dev) registry.

R-universe automatically builds and hosts R packages listed in
[`packages.json`](packages.json). Once this repository is created under my
GitHub account as `samuelbharti/samuelbharti.r-universe.dev`, my universe is
served at:

**https://samuelbharti.r-universe.dev**

## Packages

| Package | Source |
| --- | --- |
| `peacock` | [samuelbharti/peacock](https://github.com/samuelbharti/peacock) |
| `biobouncer` | [samuelbharti/biobouncer](https://github.com/samuelbharti/biobouncer) (`pkg-r/` subdir) |

## Installing packages from this universe

```r
install.packages(
  c("peacock", "biobouncer"),
  repos = c(
    "https://samuelbharti.r-universe.dev",
    "https://cloud.r-project.org"
  )
)
```

## Adding a package

Add an entry to [`packages.json`](packages.json):

- `package` — the R package name (must match the `Package:` field in the
  package's `DESCRIPTION`).
- `url` — the Git URL of the repository.
- `subdir` *(optional)* — path within the repo if the package is not at the root.
- `branch` *(optional)* — defaults to the repository's default branch.

R-universe monitors this file and rebuilds automatically on each commit.
