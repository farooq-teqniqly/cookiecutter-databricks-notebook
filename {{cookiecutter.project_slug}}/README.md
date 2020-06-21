{% set is_open_source = cookiecutter.open_source_license != 'Not open source' -%}
# {{ cookiecutter.project_name }}

![](https://img.shields.io/pypi/v/{{ cookiecutter.project_slug }})

{{ cookiecutter.project_short_description }}

{% if is_open_source %}
- Free software: {{ cookiecutter.open_source_license }}
{% endif %}

## Features

* TODO

## Credits

This package was created with Cookiecutter and the [teqniqly/cookiecutter-databricks-notebook](https://github.com/teqniqly/cookiecutter-databricks-notebook) project template
which is based on the [audreyr/cookiecutter-pypackage](https://github.com/audreyr/cookiecutter) project template.

## Contributing

Contributions are welcome, and they are greatly appreciated! Every little bit
helps, and credit will always be given.

You can contribute in many ways:

###Types of Contributions

####Report Bugs

Report bugs at https://github.com/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/issues.

If you are reporting a bug, please include:

- Your operating system name and version.
- Any details about your local setup that might be helpful in troubleshooting.
- Detailed steps to reproduce the bug.

####Fix Bugs

Look through the GitHub issues for bugs. Anything tagged with "bug" and "help
wanted" is open to whoever wants to implement it.

####Implement Features

Look through the GitHub issues for features. Anything tagged with "enhancement"
and "help wanted" is open to whoever wants to implement it.

####Write Documentation

{{ cookiecutter.project_name }} could always use more documentation, whether as part of the
official {{ cookiecutter.project_name }} docs, in docstrings, or even on the web in blog posts,
articles, and such.

####Submit Feedback

The best way to send feedback is to file an issue at https://github.com/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/issues.

If you are proposing a feature:

- Explain in detail how it would work.
- Keep the scope as narrow as possible, to make it easier to implement.
- Remember that this is a volunteer-driven project, and that contributions
  are welcome :)

####Get Started!

Ready to contribute? Here's how to set up ```{{ cookiecutter.project_slug }}``` for local development.

1. Fork the ```{{ cookiecutter.project_slug }}``` repo on GitHub.
2. Clone your fork locally::
    ```
    $ git clone git@github.com:your_name_here/{{ cookiecutter.project_slug }}.git
    ```
3. Install your local copy into a Pipenv. Assuming you have pipenv installed, this is how you set up your fork for local development:

    ```
    $ cd {{ cookiecutter.project_slug }}/
    $ pipenv --python 3.7 
    $ pipenv install -r requirements_dev.txt
    $ pipenv shell
    ```

4. Create a branch for local development::

    ```$ git checkout -b feature/name-of-your-feature```
    or
    ```$ git checkout -b bugfix/name-of-your-bug-fix```

   Now you can make your changes locally.

5. When you're done making changes, check that your
   tests pass, including testing other Python versions with tox::

    ```$ python setup.py test``` or ```$ tox```

   To get tox, just ```pipenv install``` them into your Pipenv.

6. Commit your changes and push your branch to GitHub::

    ```
    $ git add .
    $ git commit -m "Your detailed description of your changes."
    $ git push origin name-of-your-bugfix-or-feature
    ```

7. Submit a pull request through the GitHub website.

Pull Request Guidelines
-----------------------

Before you submit a pull request, check that it meets these guidelines:

1. The pull request should include tests.
2. If the pull request adds functionality, the docs should be updated. Put
   your new functionality into a function with a docstring, and add the
   feature to the list in README.rst.
3. The pull request should work for Python 3.7 and 3.8, and for PyPy. Check
   https://travis-ci.com/teqniqly/{{ cookiecutter.project_slug }}/pull_requests
   and make sure that the tests pass for all supported Python versions.

####Tips

To run a subset of tests::

    ```$ python -m unittest tests.test_{{ cookiecutter.project_slug }}```

###Deploying

A reminder for the maintainers on how to deploy.
Make sure all your changes are committed (including an entry in HISTORY.rst).
Then run::

```
$ bump2version patch # possible: major / minor / patch
$ git push
$ git push --tags
```

Azure DevOps will then deploy to PyPI if tests pass.
