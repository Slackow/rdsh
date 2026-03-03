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

Read through the source code (`rdsh`) to understand your options.

## Installation
1. Add it to your path
- Pip install it globally `pip install rdsh`
- Or manually download `sudo curl -fsSL "https://raw.githubusercontent.com/Slackow/rdsh/HEAD/rdsh" -o /usr/bin/rdsh`
2. Use it as your login shell (recommended)
- Run `sudo bash -c "which rdsh >> /etc/shells"`
- Run `chsh -s "$(which rdsh)"`
3. copy `rdshenv` into `~/.rdshenv`, and configure it however you like.
- `curl -fsSL "https://raw.githubusercontent.com/Slackow/rdsh/HEAD/rdshenv" -o ~/.rdshenv`
4. add another env (recommended)
- `curl -fsSL "https://raw.githubusercontent.com/Slackow/rdsh/HEAD/rdshenv" -o ~/.rdshenv2`