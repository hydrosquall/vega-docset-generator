# vega-docset-generator

A Python script to generate offline documentation for [vega](https://github.com/vega/vega), an expressive language for building data interactive visualizations.

## Features

- In-page table of contents for all pages, including images and examples for each Vega spec property.
- Mobile friendly layout (sidebars have been removed)
- Quick search of all pages on the public docs page, including examples. (Note that examples that load remote data require an internet connection to load normally.)

## Custom Usage

This step is only necessary if you intend to hack on the published docset locally. Otherwise, it can be installed from the Dash app or the [Dash contributions repository](https://github.com/Kapeli/Dash-User-Contributions).

1. Clone `vega` as a sibling folder of this repository using the changes from [this PR](https://github.com/vega/vega/pull/3280).
2. In that directory, run `yarn install && yarn build && yarn build:static` to generate the site
  a. You may need to install `rbenv` and `Jekyll` to build the documentation site.
3. In your python virtual environment, add python dependencies: `pip install -r requirements.txt`
  a. Using Jupyter is optional, but recommended for ease of debugging the notebook output.
4. Run `jupyter notebook`, and select `generate-vega-docset.ipynb`. Run all cells.
5. Your generated docset will be in `vega.docset`. Clicking on it in `Finder` will add it to your documentation library

See [notebook](./generate-vega-docset.ipynb) for detailed instructions. The `DEBUG` flag can be toggled to adjust the amount of logging.

## Related

- See [vega-lite-docset-generator](https://github.com/hydrosquall/vega-lite-docset-generator/) for documentation about Vega-Lite, a layer of abstraction on top of Vega.
