---
description: >-
  There are many Linux commands, and a majority provide documentation for the
  user to read. But how do you access it?
---

# Get help!

### Man-db

When installing a package via `apt-get`, you may have noticed a process that seems to take quite a while:

```text
processing triggers for man-db...
```

This is a super-helpful tool for accessing concise documentation for practically any command, and can be used quite easily. Simply choose a command to read documentation on \(`ls` is a good place to start\), and type `man` followed by the name of the command. For this example, the command is ls:

```bash
man ls
```

An interactive window will then appear, with 3 main headings:

1. `NAME`
2. `SYNOPSIS`
3. `DESCRIPTION`

Keep the following keyboard controls in mind to navigate `man-db`:

| Key | Usage |
| :--- | :--- |
| `Up arrow` | Scroll up one line |
| `Down arrow` | Scroll down one line |
| `Q` | Quit |
| `Page up` | Scroll one page \(this will change based on your window height\) |
| `Page down` | Scroll one page \(this will change based on your window height\) |
| `/` | Enter search mode \(then type your search term and press enter\) |
| `n` | Go to the next search term \(if applicable\) |
| `N` \(shift + n\) | Go to the previous search term \(if applicable\) |

### Built-in help

If there is no `man` page for a certain command, you may find it has a built-in help utility. There are generally 2 cases:

1. The program will print basic information when called with the flag `--help`.
2. The program will print basic information or refer you to its help command when called with no arguments \(keep in mind that some commands such as `cd`just use default parameters, and omitting them will not call a help utility\)

## Order of commands/TL;DR

If you are looking for help with a function use this order to find it:

1. Type `man` followed by the command name
2. Type the command with the flag of `--help`
3. Type the command and see if it refers you somewhere

