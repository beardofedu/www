## Write the Docs website

This is the code that powers [www.writethedocs.org](http://www.writethedocs.org). It contains information
about the Write the Docs group, as well as information about writing documentation.

The repo is still in its early stages; feel free to contribute information that you might want to share with the community. To contribute to the Write the Docs website, famililarize yourself with the [Sphinx site generator](http://sphinx.pocoo.org/index.html).

### Prerequisites for previewing the docs locally

You'll probably need `root` privileges to install the prerequisites.

1. Install `python 2.7.x` using your package manager.

2. If your version of Python as shown by `python -V` is <= `2.7.9`:
   1. download and install [pip](https://pip.pypa.io/en/stable/installing/).
   2. install `virtualenv` using your package manager.

### Installing the project requirements

1. In the repository root directory (`www` by default), create a virtual environment for the project requirements by running `virtualenv venv`. More info on [virtualenv](https://virtualenv.pypa.io/en/stable/).

2. Activate the virtual environment by running `source venv/bin/activate` (you'll need to do this every time you come back to the project).

2. In the repository root directory (`www` by default), run `pip install -r requirements.txt` to install sphinx and other requirements.

### Previewing the docs locally

> Remember to activate the virtual environment using `source venv/bin/activate` before running the following commands.

1. In the `docs` directory, run `make livehtml` to view the docs on [http://127.0.0.1:8888/](http://127.0.0.1:8888/).

If you're not seeing new content in the local preview, run `make clean` to delete the generated files, then `make livehtml` to regenerate them.

The Write the Docs website is hosted on [Read the Docs](https://readthedocs.org/projects/writethedocs-www).

### Viewing changes on staging

If you you can't run `make livehtml` locally, or don't want to, you can preview
changes by merging them into the `staging` branch and pushing that to GitHub.

If your feature branch is `changes-to-test` you would do something like:

```
git checkout staging
git pull
git merge changes-to-test
git push
```

Unless there are merge conflicts you need to resolve, when you push those
changes a build is triggered on Read the Docs and when it is finished you can
preview your changes on:

http://writethedocs-staging.readthedocs.io/en/staging/

### Updating the theme or css

If you need to update the theme, the original source is in

https://github.com/writethedocs/website-theme/

and instructions on how to update it are in the [`README.md`](https://github.com/writethedocs/website-theme/pull/3)
