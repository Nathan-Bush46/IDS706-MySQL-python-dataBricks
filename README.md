# IDS-SQL-Python 

[![Docker Image CI Main](https://github.com/Nathan-Bush46/IDS706-MySQL-python-dataBricks/actions/workflows/main.yml/badge.svg)](https://github.com/Nathan-Bush46/IDS706-MySQL-python-dataBricks/actions/workflows/main.yml)

[![Docker Image CI Lint](https://github.com/Nathan-Bush46/IDS706-MySQL-python-dataBricks/actions/workflows/lint.yml/badge.svg)](https://github.com/Nathan-Bush46/IDS706-MySQL-python-dataBricks/actions/workflows/lint.yml)

[![Docker Image CI Test](https://github.com/Nathan-Bush46/IDS706-MySQL-python-dataBricks/actions/workflows/test.yml/badge.svg)](https://github.com/Nathan-Bush46/IDS706-MySQL-python-dataBricks/actions/workflows/test.yml)

[![Docker Image CI Format](https://github.com/Nathan-Bush46/IDS706-MySQL-python-dataBricks/actions/workflows/format.yml/badge.svg)](https://github.com/Nathan-Bush46/IDS706-MySQL-python-dataBricks/actions/workflows/format.yml)

[![Docker Image CI Install](https://github.com/Nathan-Bush46/IDS706-MySQL-python-dataBricks/actions/workflows/install.yml/badge.svg)](https://github.com/Nathan-Bush46/IDS706-MySQL-python-dataBricks/actions/workflows/install.yml)



## Quick Explanation

* See [`video`](https://www.youtube.com/watch?v=rTuY1ctXtiI) for walkthrough.

* Python files that create, query, and test a databricks table using Python and SQL.
    * [`create table`](src/main_workspace/make_table.py): Creates a basic table from data found ['here'](https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset?resource=download)
        * Shows use of some SQL queries
    * [`query`](src/main_workspace/query.py): Creates a table from the other table. Then joins them to create a more intersting table.
    * [`Test`](src/tests/tests.py): Does a basic testing using Python. This tests that the operations on a database behave as expected. 

## Set up instructions using VS code + Docker: 
### Docker
1. For Windows, Mac, and maybe Linux, you download Docker Desktop. links can be found [here](https://docs.docker.com/engine/install/). Follow set up instructions and start the application.

2. In vs code add Dev Containers and Docker extensions 

3. clone repo, restart vs code, and open repo in vs code.

4. should see a pop up to (re)open in devcontainer. Click it and let it run. It takes a bit of time for the first run but is much faster after that. Done.

#### Alternatives to Docker
If you choose not to run docker, use a python virtual environment to prevent conflict with local packages and run the makefile.
 
## Testing

### makefile  
* install

* testing:

    tests all "\*test\*.py" files in src/test/ using py.test then tests all files using py.test --nbval-lax

* lint

* format

* all 

### VS code testing  
1. Can also use the VS-code testing menu in the same way.

## Things included are:

* [`Makefile`](Makefile)

* `Pylint` and `Ruff` for lintning

* `.env`, used to ensure constient imports and give DB info

* `.devcontainer` with [`Dockerfile`](/.devcontainer/Dockerfile), [`postinstall.sh`](/.devcontainer/postinstall.sh), and [`devcontainer.json`](/.devcontainer/devcontainer.json)`

*  [`settings.json`](.vscode/settings.json) for testing

*  A base set of libraries in [`requirements.txt`](requirements.txt)
