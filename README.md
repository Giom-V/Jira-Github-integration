# Jira-GitHub integration

This repository is used to test and document the cababilities of the [official integration](https://github.com/integrations/jira) between Github integration and Jira Cloud, and later on with Jenkins

## What works (or not)

### Commits

#### Works
* Commits and Jira issues are automatically linked if the commit contains the id of the id in its title or description 

#### Doesn't work
* 

### Branches

#### Works
* Branch and issue are automatically linked if the branch contains the id of the issue in its name (eg. [TEST-2-link-branch-and-Jira-issue](https://github.com/Giom-V/Jira-tests/tree/TEST-2-link-branch-and-Jira-issue))

#### Doesn't work
* Renaming the branch since we can only do it locally and not on Github
* Commits in the branch are not automatically linked to the issues the branch is linked with (because there could be more than one issue solved in a branch and only some of them in a commit)

### Pull requests

#### Works
* Pull requests from a linked branch are also automatically linked with the issue
* A pull request with the issue id in its title is automatically linked (it can be edited to link or unlink it)
* The status of the pull requests can be seen from Jira

#### Doesn't work
* A pull request with the issue id in its description is NOT automatically linked
* "merge pull request" commits are following the same rules as any commit and are not atomatically linked when the branch (in the case it's linkely taht the issue id was in the name that is by default in the commit) or the pull request
