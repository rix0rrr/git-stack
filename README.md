# 📚 git-stack

work on multiple branches simultaneously

A stack is a set of branches (with corresponding PRs on GitHub), that are
merged together locally so you can continue to work as if the PRs had been
merged already.

    git stack
        If on a stack, show info.
        If not on a stack, show README

    git stack --create [--name ...] [BRANCH...]
        Create a new stack from the given branches and switch to it
        warns if this is going to replace an existing stack

    git stack --add BRANCH
        Add a new branch to the stack and refresh it.

    git stack --patch BRANCH
    git stack --append BRANCH
        Commit the current changes to the given branch. --patch must update
        an old branch. --append must create a new branch.

    git stack --refresh
        Refresh the stack

    git stack --rebase BRANCH
        Rebase and refresh the stack on top of a new base commit.

    git stack --push
        Push all branches in the stack


# Installation

```
git clone git@github.com:rix0rrr/git-stack.git

# Or wherever else you want to install it
sudo ln -s $(PWD)/git-stack/git-stack /usr/local/bin
```
