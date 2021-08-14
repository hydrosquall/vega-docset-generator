# vega-lite-docset-generator

A Python script to generate offline documentation for [vega-lite](https://github.com/vega/vega-lite), an expressive language for building data interactive visualizations.

## Features

- In-page table of contents for all pages, including images and examples for each Vega-Lite spec property.
- Mobile friendly layout (sidebars have been removed)
- Quick search of all pages on the public docs page, including examples. (Note that examples that load remote data require an internet connection to load normally.)

## Usage

1. Clone `vega-lite` as a sibling folder of this repository using the changes from [this PR](https://github.com/vega/vega-lite/pull/7642).
2. In that directory, run `yarn install && yarn docset` to generate the site
  2a. Note that you may need to install `rbenv` and `Jekyll` to build the documentation site.
3. In your python virtual environment, add python dependencies: `pip install -r requirements.txt`
  3a. Note that using Jupyter is optional, but recommended for ease of debugging the notebook output.
4. Run `jupyter notebook`, and double-click `generate-vega-lite-docset.ipynb`. Run all cells.
5. Your generated docset will be in `vega-lite.docset`

See [notebook](./generate-vega-lite-docset.ipynb) for detailed instructions. The `DEBUG` flag can be toggled to adjust the amount of logging.
