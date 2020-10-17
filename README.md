# datasette-render-local-images

[![PyPI](https://img.shields.io/pypi/v/datasette-render-local-images.svg)](https://pypi.org/project/datasette-render-local-images/)
[![Changelog](https://img.shields.io/github/v/release/kracekumar/datasette-render-local-images?include_prereleases&label=changelog)](https://github.com/kracekumar/datasette-render-local-images/releases)
[![Tests](https://github.com/kracekumar/datasette-render-local-images/workflows/Test/badge.svg)](https://github.com/kracekumar/datasette-render-local-images/actions?query=workflow%3ATest)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/kracekumar/datasette-render-local-images/blob/main/LICENSE)

Render local images in the system using datasette plugin

## Installation

Install this plugin in the same environment as Datasette.

    $ datasette install datasette-render-local-images

## Usage

Render local system images in the datasette displayed HTML.

By default plugin will figure out image and render with
default height and width of the image.

To modify the image size and width, pass the configuration via `metadata.json`

``` python
{
    "plugins": {
        "datasette-render-images": {
            "height": 150,
            "width": 150
        }
    }
}
```

When the local image path is missing or no image specified in the path,
the plugin will not render the value.

## Development

To set up this plugin locally, first checkout the code. Then create a new virtual environment:

    cd datasette-render-local-images
    python3 -mvenv venv
    source venv/bin/activate

Or if you are using `pipenv`:

    pipenv shell

Now install the dependencies and tests:

    pip install -e '.[test]'

To run the tests:

    pytest