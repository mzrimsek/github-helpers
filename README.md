github-helpers
======

Utility functions for interacting with github repositories from the command line.

Installation
------

1. Run the following:
```
wget https://raw.githubusercontent.com/mzrimsek/github-helpers/master/.github_helpers
mv .github_helpers ~/
```
2. Configure the file by replacing setting the following environment variables:
  * `GITHUB_USER` with your github username
  * `GITHUB_TOKEN` with a Personal Access Token which you can [generate here](https://github.com/settings/tokens).
    * Permissions required are noted on each function
Add each of these to your `.bashrc` file

3. Add the file to your `.bashrc` file
```
if [ -f ~/.github_helpers ]; then
    . ~/.github_helpers
fi
```
4. Source your `.bashrc`

Functions
------

### github-create
Create and push a new repository
#### Usage
```
github-create <repository_name>
```
If no repository name is provided, you will be prompted for one. If you still proceed without supplying and name, the current working directory will be used as the root of the repository.

If at any point a repository name is provided, whether when initially running the function or after being prompted, the repository will be created in the subdirectory of the name provided. If that directory does not exist it will be created.
