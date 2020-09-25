`nota` is a simple tool to make and organise notes, using git to keep history,
and your favourite editor for editing.

You can enable GPG support by doing the following:

1. Adding `GPG=1` to `$XDG_CONFIG_HOME/nota`, if `$XDG_CONFIG_HOME` is set, or
   `~/.config/nota` if it isn't. You can set this as an environment variable
   instead, if you prefer.
2. Having your editor transparently open gpg files. For example, in vim, you
   can use [vim-gnupg][]. You can also set a different `PGP_EDITOR`.

You can also use read-only mode (which will just display the contents of the
note) using `NOTA_READ_ONLY=1`.

My primary motivation for making this was that I used [iDoneThis][] for a long
time, but now I need to store sensitive entries that should not leave my local
computer.

[iDoneThis]: https://idonethis.com/
[git]: http://git-scm.com/
[vim-gnupg]: https://github.com/jamessan/vim-gnupg

## Usage

    # Edit today's entry (in format YYYY-MM-DD)
    nota

    # Edit the entry from yesterday/today/4 days ago
    nota (yesterday|today|'4 days ago')

    # Edit the entry for Dec 1 2014
    nota 2014-12-01

    # Edit an entry called "foo"
    nota foo

    # Set up git to push somewhere if you want it
    # You can issue arbitrary git commands using `nota git`
    nota git remote add origin <origin>

# nota-todo-reminder

nota-todo-reminder is a small script calling `notify-send` that outputs the
contents of the nota entry called "todo" if it still contains anything. This
allows you to use nota to remind you of todo entries using a systemd timer,
cron script, or similar. Create a note called "todo" and run it to see how it
works.
