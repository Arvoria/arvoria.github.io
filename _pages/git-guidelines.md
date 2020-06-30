---
layout: docpage
title: Git Usage Guideliens
subtitle: Best practices and default usage of Git
tags: [git]
---

# Introduction

[Git](https://git-scm.com/) is the tool used by the Arvorian Industries to track
our software projects. Every project is uploaded onto our [Github
organization](https://github.com/Arvoria/) to view the projects one has to be a
member of the organization. Membership is usually awarded to developers of the
Arvorian Industries. Contact Shane or Julian to request membership.

## Target Audience
The audience of this document are users of Git in order to modify existing
Arvorian repositories. Either by uploading or altering ROBLOX model files or
programs stored in a repository.

## Benefits of Git
One may ask what the benefits of Git are, since one can write software with or
without it. To better understand the benefits we must note that every change in
software is in essence a separate revision. Git tracks every change on a
per-commit basis. Performing changes on a per-commit basis allows for better
quality management and versioning because each change (or commit) can be
reviewed individually.

## Installation
To be able to use Git it should be downloaded from the
[website](https://git-scm.com/downloads). Select your OS and while installing
make sure the git.exe (or just git for MacOS/Linux) is available on the command
line, by adding Git's binary folder to PATH.

### Git GUI tools
There are a variety of Git GUI tools available with highly varying quality. Me
(Julian) found that GitKraken is one of the few GUI based Git interfaces that
actually represent the inner workings of Git. 

Using other tools like Git Desktop as provided by Github gives the user a skewed
vision of the reality of Git. Since Git is a powerful tool it allows for
mismanagement of Git repositories. It is important for the user to know what
effects of a given GUI button are, in order to manage his repository
effectively.

Therefore GitKraken is the *only* recommended Git GUI tool by the Arvorian
Industries. Using other Git GUI's is essentially forbidden, unless it is
explicitly whitelisted in this document by the AI leadership. We are open for
suggestions.

### Authentication
There are two ways that one can Git can authenticate itself for a server. Using
a username and password combination or using a public key. At Arvorian
Industries we strictly recommend using keys to authenticate yourself.

This is because of submodules for which one has to authenticate himself as well
in order to clone them. Having mixins of https:// and ssh:// protocols in a
repository is not treated well by Git. Because of that we uniformly use ssh://,
use this protocol when cloning an Arvorian Git repository.

# Using Git
## Terminology
### Unstaged changes
An unstaged change is a change that is introduced by a text editor or other
programs. Unstaged changes are in essence what is introduced when someone
modifies source code.

### Staging
The next step after introducing unstaged changes are staged changes. What is the
difference between an unstaged and staged change? In essence a staged change is
a change that is selected to be committed.

### Committing
When someone performs a commit, paired with a message, he takes all staged
changes and puts them in 'one unit of change', called a commit. Commits are what
can be shared with others. Usually done by pushing it to a remote repository.

### Push and pull
Commits can be pushed to a remote. And be pulled from a remote. A cloned
repository usually only has one remote called origin. By typing `git push` and
`git pull`, it typically pushes or pulls all commits across all branches to
origin.

### Branches


### Merging


## Best Practices
### Small and coherent commits
Since a commit can be regarded to as 'one unit of change' it is best when they
have a logical coherency and are at best small. This allows for flexibility by
the repository maintainer, since he can more easily cherry pick commits and more
importantly it allows for a better merging experience.

### Review your code before committing
This is where a tool like GitKraken is really useful. Since it easily allows the
user to inspect his changes on a per-file basis, simply by opening them in his
GUI. Sometimes IDE's, for example VSCode does this, highlight lines of code when
they have unstaged changes.

Reviewing your own changes allows you to have a more fresh view on what you are
actually adding. You can focus only on the differences you have introduced as
highlighted by the Git GUI. You will not be distracted by the imperfections of
the whole codebase, merely only by your own contributions, which is something
you should fix.