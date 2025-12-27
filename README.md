# RDSH - Random Shell

RDSH is a shell that picks a random shell on your system and runs with it.
By default it uses login shells defined under `/etc/shells`

You can modify the shells by creating a `~/.rdshenv` file

if you define multiple envs (e.g., `~/.rdshenv`, `~/.rdshenv2`, `~/.rdshenv3`),
RDSH will run one at random.

RDSH will also look for a system wide config (`/etc/rdshenv*`) and run one at random.

The `-l` and `-n` options exist,
`-l` for listing the selection of shells, and `-n` for picking one without executing it.

The shell is entirely written in bash.

please add it to your path, or even better, use it as your login shell `chsh -s "$(which rdsh)"`.

Read through the source code to understand your options.