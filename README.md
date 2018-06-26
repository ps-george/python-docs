# python-docs
Reusable code for setting up Sphinx and a github.io website for a repository.

## First time setup

1. Fill in the parameters in [docs/PARAMS.yml](docs/PARAMS.yml).
2. Adjust the parameters in [docs/Makefile](docs/Makefile) to match those in [docs/PARAMS.yml](docs/PARAMS.yml)
3. Create a gh-pages branch
```bash
git checkout --orphan gh-pages
git rm --cached -r .
git commit -m "Initial commit" --allow-empty
git push -u origin gh-pages
```
4. Install pip requirements (ideally in a virtualenv)
```bash
virtualenv -p python3 venv
source venv/bin/activate
pip install -r docs/require.txt
```
5. Run [make_docs.py](docs/make_docs.py)
```bash
python docs/make_docs.py
```

After the first time setup, all you need to run is `python make_docs.py`
