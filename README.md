# JourneyMap Docs

This repository contains user documentation for the JourneyMap mod. Written in markdown and compiled into a static site using [MkDocs](https://www.mkdocs.org/) and [Material for Mkdocs](https://squidfunk.github.io/mkdocs-material/).

## Contributing

We are happy to accept pull requests for documentation changes. If you would like to contribute, please fork this repository and submit a pull request. If you are not familiar with Git or GitHub, you can also submit an issue with your suggested changes, and we will add them to the documentation.

When submitting a pull request, please follow these guidelines:

- Make sure to describe your changes in the pull request description.
- Make sure to run the documentation locally to ensure that your changes are displayed correctly. See the [Installing](#installing) section below for instructions on how to do this.

## Installing

To run the documentation locally, you will need to first install MkDocs and Material for MkDocs. You can do this by running the following commands:

- `pip install -r requirements.txt`

These commands will install MkDocs and Material for MkDocs.

Run one of the following commands to start the local documentation server:

1. `mkdocs serve -f ./config/en/mkdocs.yml`
2. `python -m mkdocs serve -f ./config/en/mkdocs.yml`

If you want to see the docs in another language, just replace en with your language name.
