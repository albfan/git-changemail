# git-changemail

Replace an user from the repo.

## background

I've had so many headaches about authors and committers, that finally I managed to built this script.

read [this](http://stacktoheap.com/blog/2013/01/06/using-mailmap-to-fix-authors-list-in-git/) for real stories about people collaborating on git.

##Installation

Download and symlink to your path

```bash
$ git clone git@github.com:albfan/git-changemail.git
$ cd git-changemail
$ ln -s $PWD/git-changemail ~/bin/
```

## usage

`git changemail` or `git changemail -h` must show you how to use it

## examples

Change author matchings on current branch

    $ git changemail -a old@email.com -n newname -m new@email.com

Change author and committer matchings on \<branch\> and \<branch2\>. Pass `-f` to filter-branch to allow rewriting backups

    $ git changemail -b old@email.com -n newname -m new@email.com -- -f <branch> <branch2>

Show existing users on repo

    $ git changemail --show-both





