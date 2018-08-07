# Contributing to Repositories in Source-aasf
So you're interested in contributing Source-aasf? Excellent, we love your input! We want to make contributing to projects as easy and transparent as possible, whether it's:

- Reporting a bug
- Discussing the current state of the code
- Submitting a fix
- Proposing new features
- Becoming a maintainer

## We Develop with Github
We use github to host code, to track issues and feature requests, as well as accept pull requests.

## We Use [Github Flow](https://guides.github.com/introduction/flow/index.html), So All Code Changes Happen Through Pull Requests
Pull requests are the best way to propose changes to the codebase (we use [Github Flow](https://guides.github.com/introduction/flow/index.html)). We actively welcome your pull requests:

1. Fork the repo and create your branch from `master`.
2. If you've added code that should be tested, add tests.
3. If you've changed APIs, update the documentation.
4. Issue that pull request!


## Essential git commands
A full git tutorial is beyond the scope of this document but this list describes the few git commands you are likely to encounter while contributing:

- `git fetch` gets the latest development version of Astropy, which you will use as the basis for making your changes.
- `git branch` makes a logically separate copy of Astropy to keep track of your changes.
- `git add` stages files you have changed or created for addition to git.
- `git commit` adds your staged changes to the repository.
- `git push` copies the changes you committed to GitHub
- `git status` to see a list of files that have been modified or created.

## Workflow Overview

These, conceptually, are the steps you will follow in contributing to repositories on Source-aasf:

- Fork a repository and clone it locally.
- Make a new feature branch; you will make your changes on this branch.
- Follow The editing workflow to write/edit/document/test code - make frequent, small commits.
- Push changes to feature branch on your fork.
- From GitHub, Ask for your changes to be reviewed to let the maintainers know you have contributions to review.
- Make a pull request from GitHub.
- Revise and push as necessary in response to comments on the pull request. Pushing those changes to GitHub automatically updates the pull request.

## Detailed Workflow
* ## Fork a repository and clone it locally.
Suppose you are interested in contributing to `my-project` repository on source-aasf. When you fork it, you will have the repoisitory as 'your-github-username/myproject'
To clone this locally, in your terminal window, run
```bash
git clone https://github.com/your-github-username/my-project.git
cd my-project
```
Now you have a local clone of project repository for development. You should also add the upstream repository. To do this, run
```bash
git remote add upstream https://github.com/source-aasf/my-project.git
```
Now if you run
```bash
git remote
```
```
origin
upstream
```
If you get this output, it means you have set up local repository correctly.


* ## Make a new feature branch
When you are ready to make some changes to the code, you should start a new branch. Branches that are for a collection of related edits are often called ‘feature branches’.
Making a new branch for each set of related changes will make it easier for someone reviewing your branch to see what you are doing.

Choose an informative name for the branch to remind yourself and the rest of us what the changes in the branch are for. Branch names like add-ability-to-fly or buxfix-for-issue-42 clearly describe the purpose of the branch.
Always make your branch from my-project/master so that you are basing your changes on the latest version of the repository.
```bash
# Update the mirror of trunk
git fetch astropy

# Make new feature branch starting at astropy/master
git branch my-new-feature astropy/master
git checkout my-new-feature
```

* ## Make changes to the code.
Then, to stage these changes run
`git add .` if you want to add all changed files or `git add <file_names>` if you want to add specific files
Then commit your changes with a meaning full message
`git commit -m "added new feature"`
and then push these changes to your fork
`git push origin my-new-feature`

* ## Make a pull request
On GitHub, on your forked repo, switch your branch from dropdown menu to my-new-feature
You will see the message of how many commits your branch is ahead of upstream/master
Now click on Pull Request, enter a title for the set of changes, and some explanation of what you’ve done. If there is anything you’d like particular attention for, like a complicated change or some code you are not happy with, add the details here.

* ## Revise and push as necessary

You may be asked to make changes in the discussion of the pull request. Make those changes in your local copy, commit them to your local repo and push them to GitHub. GitHub will automatically update your pull request.
