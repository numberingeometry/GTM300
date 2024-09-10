# GTM300 Project

This is a repository for the [webpage](https://numberingeometry.github.io/GTM300/intro.html) that gathers solutions of the book [An Introduction to Automorphic Representations: with a view toward trace formulae](https://link.springer.com/book/10.1007/978-3-031-41153-3) by [Jayce R. Getz](https://sites.duke.edu/jgetz/) and [Heekyoung Hahn](https://sites.duke.edu/heekyounghahn/) (Springer GTM300).

## Requirements

- `jupyter-book`, use `pip install jupyter-book`
- (Optional, for maintainers) `ghp-import`, use `pip install ghp-import`

## How to contribute

Solutions for each problem (exercise) correspond to a single markdown file `chapter{number}/exercise{number.number}.md`, which is the only thing you may need to edit if you want to upload your own solution.

0. Make a new branch for pull request - do not work on the `main` branch.
    ```
    git checkout -b my-new-branch
    ```

1. Edit the corresponding markdown file. See [this](https://ashki23.github.io/markdown-latex.html#latex) to learn how to use LaTeX in markdown, which is almost same as the usual LaTex.


2. Build the html files with
    ```
    jupyter-book build gtm300/
    ```

3. Make a pull request to the main branch.

## How to publish (for the maintainers)

Requires `ghp-import`. Install with `pip install ghp-import` if it is not installed yet.

0. Make sure that the new html files are built out of jupyterbook. Skip if you already did.
    ```
    jupyter-book build gtm300/
    ```

1. Switch to the `main` branch if needed.
    ```
    git checkout main
    ```

2. Move to the `gtm300/` directory.
    ```
    cd gtm300/
    ```

3. Call `ghp-import`. This will push new files to the `gh-pages` branch and publish it online, which can be viewed at https://numberingeometry.github.io/GTM300/intro.html.
    ```
    ghp-import -n -p -f _build/html
    ```

You should **NOT** update the codes on the `gh-pages` branch manually.