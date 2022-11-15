# Posit Connect & R

Posit Connect is a publishing platform for the work your team creates in R and Python.
This repository contains examples of R content you can deploy to Connect, including:

## Interactive apps

- [Shiny Penguins](./shiny-penguins/README.md)

## Web APIs

- [Plumber](./plumber-penguins/README.md)
- [Plumber Tableau Integration](./plumber-tableau-penguins/README.md)

## Documents

- [RMarkdown using Blastula for sending emails](./rmd-blastula/README.md)
- [RMarkdown](./rmd-penguins/README.md)
- [Connect Widgets](./connectwidgets-penguins/README.md)

## Pins

- [Pins](./pins-r-penguins)

## Getting Started

You can deploy examples from this repo to your Connect server [via git-backed deployment](https://docs.rstudio.com/connect/user/git-backed/), or clone the repository and deploy examples using [push-button publishing](https://docs.posit.co/connect/user/publishing/) or from their manifests with the [`rsconnect` CLI](https://docs.posit.co/connect/user/publishing-r/).

If you want to explore an example more closely before deploying it:

* Clone this repository
* Restore the needed packages from the renv lock file

```r
library(renv)
renv::hydrate()
```

### Want to add an example? 

Awesome! The requirements are: 

1. Use [renv](https://rstudio.github.io/renv/articles/renv.html) so that the package versions are recorded 
2. Create the [manifest.json file](https://docs.posit.co/connect/user/git-backed/#creating-a-manifest-file-from-r) to support git-backed publishing
