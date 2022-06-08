# CHAI Project Organisation

This is the GitHub organisation for the CHAI project development. 

# Python Linting/Performance
Most of the backend code is written is Python with a focus on readability and performance. To help with those requirements most of the backend Python code is set up to be used with `pylint` and `perflint`. As with unit testing, the goal is not necessarily to reach 100% coverage and/or linting score. It should be used as a tool to guide proper coding styles, pre-optimise where appropriate, and make explicit when certain coding styles or optimisations are not applied (look for `pylint: disable` statements).

## Enabling Linting/Performance Checks
Linting and performance checks are optional, but **strongly** advised during development. To enable them, use `pip` to install `pylint` and `perflint`. You can then perform a linting and performance check using `pylint --load-plugins perflint [target-file]`. If you are using PyCharm the tool can be integrated. To do so:

 * go to Preferences;
 * open the Tools tab;
 * open the External Tools tab;
 * add a new external tool:
    * give it a Name: *Performance Lint*
    * give it a Description: *Pylint with Performance Lint*
    * set the Program: `$PyInterpreterDirectory$/pylint`
    * set the Arguments: `--load-plugins perflint $FilePath$`
    * set the Working dir: `$ProjectFileDir$`
  
After following these steps you can use Tools -> External Tools -> Performance Lint to run the linting and performance checks straight from within PyCharm.
