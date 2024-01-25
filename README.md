# 📚 git-stack

work on multiple branches simultaneously

A stack is a set of branches (with corresponding PRs on GitHub), that are
merged together locally so you can continue to work as if the PRs had been
merged already.

    git stack
        If on a stack, show info.
        If not on a stack, show README

    git stack -N|--new [--name ...] [BRANCH...]
        Create a new stack targeting the current commit as base, adding the
        given branches initially as patches. Warns if this is going to replace
        an existing stack

    git stack -c|--commit BRANCH
        Commit the currently staged changes to the given branch, either
        adding onto an existing BRANCH or creating a new one off of the current
        stack's base.

    git stack -x|--extract SRC DST
        Take the currently staged changes, apply them to SRC, and apply them
        in reverse to DST. This moves changes from SRC to DST. DST can be
        either an existing or new branch.

        Obtain these changes by (for example) running one of these commands:

            git checkout -p 1234abcd~
            git checkout STACK-base path/to/my/file

    git stack -d|--delete [--name ...]
        Delete a given stack.

    git stack -A|--add BRANCH
        Add a new branch to the stack and refresh it.

    git stack --remove BRANCH
        Remove a branch from the stack and refresh it.

    git stack -r|--refresh
        Refresh the stack

    git stack -R|--rebase BRANCH
        Rebase and refresh the stack on top of a new base commit.

    git stack -o|--reorder [--name ...]
        Edit the stack configuration in $EDITOR (vim), then refresh.

    git stack -P|--push
        Push all branches in the stack



# Installation

```
git clone git@github.com:rix0rrr/git-stack.git

# Or wherever else you want to install it
sudo ln -s $(PWD)/git-stack/git-stack /usr/local/bin
```
