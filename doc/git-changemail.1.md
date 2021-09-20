# NAME

**git-changemail** - Replace an user from repo history

# SYNOPSIS

| *git* *changemail* [-a|--author | -c|--committer | -b|--both]
|            [-n|--name] [-m|--mail] [--dry-run]
|            [--show-authors] | [--show-committers]
|            [--show-both] | [-h|--help]

# DESCRIPTION

Allow to replace authors and committers from commit history

# OPTIONS

-a, --author
:   Old author email. Change MODE to AUTHOR.

-c, --committer
:   Old committer email. Change MODE to COMMITER.

-b, --both
:   Define old author and committer at same time

-n, --name
:   Sets the new name for actual MODE.

-m, --mail
:   Sets the new email for actual MODE.

--dry-run
:   Shows what changes would be done.

--show-authors
:   Shows all authors on repo.

-a, --add=REGEX
:   Add REGEX to target file (must take care of shell expansion) though as a verbose command for scripting.

-h, --help
:   Shows this help.

# FILES

.git/info/exclude

:   Per-repo excludes.

.gitignore

:   Shared repo ignores.

# EXAMPLES

$ git-changemail -a old@email.com -n newname -m new@email.com
: change author matchings on current branch

$ git-changemail -b old@email.com -n newname -m new@email.com -- -f <branch> <branch2>
: change author and committer matchings on <branch> and <branch2>. Pass `-f`
: to filter-branch to allow rewriting backups

$ git-changemail --show-both
: show results

# REPORTING BUGS

Issue tracker: <https://github.com/albfan//git-changemail/issues>

# AUTHOR

Alberto Fanjul <albertofanjul@gmail.com>

# SEE ALSO

**git(1)**, **git-filterbranch(1)**
