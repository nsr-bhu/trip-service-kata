
# Commands

## Test output 

$ python -m pytest -v 
$ python -m pytest -v --no-header

## Continue draaien 

```
$ pytest-watcher .
```

## Coverage

*Tools*

```
$ pip install pytest-cov
$ ptw --  -v --no-header --cov-report html:cov --cov=tripservice 
$ ptw --  -v --no-header --cov-report lcov:lcov.info --cov=tripservice 
```

*Configuratie*

Coverage geregeld in pyproject.toml + instelling op coverage-gutter extension waar de lcov.info te vinden is.

```
## pyproject.toml
[tool.coverage.run]
source = ["./service/"]
omit = ["./test/"]

[tool.pytest.ini_options]
addopts = "-v --no-header --cov --cov-report lcov:./cov/lcov.info" 
# more options:
##--cov-report=term --cov-report html:./cov/index.html --cov-report lcov:./cov/lcov.info"
```

https://jasonstitt.com/perfect-python-live-test-coverage

## Alias

# TODO

* Eigen git repo voor begin.
* coverage in gutter aan de praat.
** TODO pytest-watch werkt niet goed, pytest-wachter wellicht beter...maar nu geen coverage meer in gutter.
 