# Posit Team & R

# Posit Connect

Posit Connect is a publishing platform for the work your team creates in R and [Python](https://github.com/sol-eng/python-examples).

This repository contains examples of R content, including:

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

- [Pins](./pins-r-penguins/README.md)

## Getting Started

You can deploy examples from this repo to your Connect server [via git-backed deployment](https://docs.rstudio.com/connect/user/git-backed/), or clone the repository and deploy examples using [push-button publishing](https://docs.posit.co/connect/user/publishing/) or from their manifests with the [`rsconnect` CLI](https://docs.posit.co/connect/user/publishing-r/).

If you want to explore an example more closely before deploying it:

* Clone this repository
* Navigate the working directory to the desired example, for example with `setwd("./shiny-penguins")`
* Restore the needed packages from the renv lock file after setting your repository to the appropriate source

```r
library(renv)

options(repos = c(REPO_NAME = "https://packagemanager.posit.co/cran/latest"))

renv::restore(repos = c(REPO_NAME = "https://packagemanager.posit.co/cran/latest"))
```

For forcing a change to a different repository: 
```
options(repos = c(REPO_NAME = "https://packagemanager.posit.co/cran/latest"))

renv::rebuild("MASS", recursive = TRUE)
renv::snapshot()
```


## Projects

### Bike share

The "mega" bike share demo:

-   To see all content on Connect filter on the tag [Bike Predict](https://colorado.rstudio.com/rsc/connect/#/content/listing?filter=min_role:viewer&filter=content_type:all&view_type=expanded&tags=111-tagtree:218)_
-   View the Connect Widgets Dashboard:
    -   [Solo View](https://colorado.rstudio.com/rsc/bike-share/)
    -   [Dashboard View](https://colorado.rstudio.com/rsc/connect/#/apps/3124a8f9-7d30-44b9-a49a-552db71b036e)
-   Source code: [https://github.com/sol-eng/bike_predict](https://github.com/sol-eng/bike_predict)

# Posit Workbench

Posit Workbench is the development environment and supports multiple editors with RStudio Pro, VS Code, and JupyterLab and Jupyter Notebook. 

This repository contains examples of some of the key features, including: 

## Job Launcher 

- [Simple job launching](./r-job-launcher/README.md)

# Posit Package Manager

Posit Package Manager hosts binaries of packages inside your network, including hosting of internally developed packages. 

Feature examples upcoming. 

# Want to add an example? 

Awesome! The requirements are: 

1. Use [renv](https://rstudio.github.io/renv/articles/renv.html) so that the package versions are recorded 
2. Create the [manifest.json file](https://docs.posit.co/connect/user/git-backed/#creating-a-manifest-file-from-r) to support git-backed publishing

