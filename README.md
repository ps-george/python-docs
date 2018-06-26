# python-docs
Reusable code for setting up Sphinx and a github.io website for a repository.

## First time setup

1. Fill in the parameters in [docs/PARAMS.yml](docs/PARAMS.yml).
2. Adjust the parameters in [docs/Makefile](docs/Makefile) to match those in [docs/PARAMS.yml](docs/PARAMS.yml)
3. Create a gh-pages branch
```bash
git checkout --orphan gh-pages
git rm --cached -r
git push -u origin gh-pages
```
4. Run [make_docs.py](docs/make_docs.py)

After the first time setup, all you need to run is `python make_docs.py`
