# ControlPage-Docs

## Canonical source

I do development on my [personal GitLab instance](https://gitlab.fischerserver.eu/controlpage/controlpage-docs).

But contributions are welcome on [Gitlab.com](https://gitlab.com/controlpage/controlpage-docs).

Furthermore, this project is mirrored to [GitHub](https://github.com/SimonFischer04/controlpage-docs). But don't open any issues or pull requests there!

## Installation

Install dependencies for doc.

1. Creating a virtual environment

    As with any python project it is usually recommended creating a virtual environment:

    ```bash
    python -m venv env
    # enter / re-enter later the venv using:
    source env/bin/activate
    ```

2. Install dependencies using provided requirements file

    ```bash
    pip install -r requirements.txt
    ```

### Local Development

```bash
# run using the provided helper script
npm start
# or directly using
mkdocs serve
```

### Building

```bash
mkdocs build
```

This generates a static site into the `site` directory that can be served by any web server / static web hosting provider like GitHub Pages / GitLab Pages / ....

To check out the result you could also for example use pythons built-in web server by running `python3 -m http.server 4200` inside the `site` folder.

## Linting

This project uses [markdownlint](https://github.com/DavidAnson/markdownlint) for linting.

It can be run either directly from the CLI using `npm run lint` (after installing the dependency using `npm install`) or integrated with your editor, see: [Related](https://github.com/DavidAnson/markdownlint#related). Furthermore, linting is automatically checked using CI on each PR / for each push.

Some rules have been disabled:

| #                                                                                | Rule             | Why |
| -------------------------------------------------------------------------------- | ---------------- | --- |
| [MD013](https://github.com/DavidAnson/markdownlint/blob/main/doc/Rules.md#md013) | Line length      | - |
| [MD033](https://github.com/DavidAnson/markdownlint/blob/main/doc/Rules.md#md033) | Inline HTML      | Required when using [Images](https://squidfunk.github.io/mkdocs-material/reference/images/). |
| [MD046](https://github.com/DavidAnson/markdownlint/blob/main/doc/Rules.md#md046) | Code block style | Interferes with [Admonitions](https://squidfunk.github.io/mkdocs-material/reference/admonitions/). |
