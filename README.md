`daily` is a simple tool to keep a daily log of activities, using git to keep
history.

You can enable GPG support by doing the following:

1. Starting daily with `GPG=1` in the environment
2. Having your editor transparently open gpg files. For example, in vim, you
   can use [vim-gnupg][].

My primary motivation for making this was that I used [iDoneThis][] for a long
time, but now I need to store sensitive entries that should not leave my local
computer.

[iDoneThis]: https://idonethis.com/
[git]: http://git-scm.com/
[vim-gnupg]: https://github.com/jamessan/vim-gnupg

## Usage

    # Edit today's entry
    daily

    # Edit the entry for Dec 1 2014
    daily 2014-12-01

    # Set up git to push somewhere if you want it
    # You can issue arbitrary git commands using `daily git`
    daily git remote add origin <origin>
