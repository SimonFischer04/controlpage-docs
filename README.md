# ControlPage-Docs

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

TODO

## ---WIP---
