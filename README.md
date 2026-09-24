# Whale-0.github.io

This repository contains my personal Quarto website. It includes one blog post about orientation and two computational blog posts written in R and Python.

## Requirements

The site was built using:

- Quarto: 1.10.18
- uv: 0.12.5
- R: 4.6.1
- Python: 3.14.7

The R package environment is managed with `renv`, and the Python environment is managed with `uv`.

## Build Instructions

### 1. Clone the repository

Run the following commands in a terminal:

``` bash
git clone git@github.com:Whale-0/Whale-0.github.io.git
cd Whale-0.github.io
```

### 2. Restore the Python environment

From the repository root, run:

``` bash
uv sync
```

This creates the project-specific Python environment using `pyproject.toml` and `uv.lock`.

### 3. Restore the R environment

Open R from the repository root and run the following command in the R console:

``` r
renv::restore()
```

This restores the R packages recorded in `renv.lock`.

### 4. Render the website

Return to the terminal at the repository root and run:

``` bash
uv run quarto render
```

The rendered website is written to the `docs/` directory.

### 5. View the website locally

After rendering, open `docs/index.html` in a web browser.

## Data Sources

The R computational post uses the [Gapminder dataset](https://www.gapminder.org/data/).

The Python computational post uses the [Palmer Penguins dataset](https://allisonhorst.github.io/palmerpenguins/).

Both datasets are provided through installed packages, so the website does not need to download.
