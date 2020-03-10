# About

This package provides command line access to Encapsia over the REST API.

All of these are designed to work with server 1.5 and beyond.

## Autocomplete

Setup autocomplete using the instructions found on <https://github.com/click-contrib/click-completion>

## Tests

See the `walkthrough_tests` directory for bash scripts which exercise the CLI.

Run them e.g. with:

    bash walkthrough_tests/all.sh --host <host> --example-plugin-src ../inf-ice-example-plugin/

Note that these tests are *not* self-verifying; they just provide helpful coverage, assurance, and working documentation.

## Release checklist

* Run: `black .`
* Run: `isort`
* Run: `flake8 .`
* Ensure "tests" run ok (see above). Also capture output and commit with:
    `bash walkthrough_tests/all.sh --host <host> --example-plugin-src ../inf-ice-example-plugin/ 2>&1 | ansi2html -f 80% >WALKTHROUGH.html`
* Ensure git tag, package version, and `enacpsia_cli.__version__` are all equal.