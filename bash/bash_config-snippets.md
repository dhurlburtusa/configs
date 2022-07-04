# bash Config Snippets


## Command Prompt

The `PS1` (Prompt String 1) environment variable controls the first line of the command prompt. The `PS2` environment variable controls the command prompt for the lines after the first.


## History

**HISTCONTROL**

A colon-separated list of values (`erasedups`, `ignoredups`, and `ignorespace`) controlling how commands are saved on the history list.

- `ignorespace` causes line which begin with a space character to not be saved in the history.
- `ignoredups` causes lines which match the previous history entry to not be saved in the history.
- `ignoreboth` is shorthand for `ignorespace` and `ignoredups`.
- `erasedups` causes all previous lines matching the current line to be removed from the history list before that line is saved.

**HISTIGNORE**

A colon-separated list of patterns used to decide which command lines should be saved on the history list. Each pattern is anchored at the beginning of the line and must match the complete line (no implicit `*` is appended). Each pattern is tested against the line after the checks specified by `HISTCONTROL` are applied. In addition to the normal shell pattern matching characters, `&` matches the previous history line.

**HISTSIZE**

The maximum number of commands to remember on the history list. If the value is 0, commands are not saved in the history list.

```sh
HISTCONTROL=erasedups:ignoredups:ignorespace
HISTIGNORE=clear:echo*:exit
HISTSIZE=10000
```
