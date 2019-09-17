# Directories & files in Linux

Linux has a very specific file structure, with certain folders containing certain information. But what are these folders, and how do you traverse them in the command line?

| Location | Purpose | Aliases |
| :--- | :--- | :--- |
| `/` | The **root** directory in Linux, where all folders are stored. Think of this as the equivalent of the _My Computer_ folder on Windows | N/A |
| `/home/USERNAME` | Where all of your personal files are stored. This usually contains `Desktop`, `Downloads`, `Documents`etc | `~/` |
| `.` | A representation of the current directory. For example, if you have a document called `README.md` in your current folder, it could be called `./README.md` | N/A |
| `..` | Similar to `.`, but representing the upper directory. For example, if you wanted to go to the upper directory, you could use `cd ..` | N/A |

### LS

`ls` is the command often taught first to Linux beginners, as it it easy to use and provides information for use in other commands. `ls` lists the contents of a directory, showing all files & folders inside. Here are some examples of regular `ls` usage:

| Command | Usage |
| :--- | :--- |
| `ls` | Lists the contents of the current directory |
| `ls -a` | Lists the contents of the current directory, including files beginning with `.` |
| `ls -l` | Lists the contents of the current directory, with additional information such as date modified and user permissions |
| `ls DIR` | Lists the contents of the directory DIR |
| `ls ..` | Lists the contents of the parent directory |

Some common `ls` flags are:

| Flag | Shorthand | Description |
| :--- | :--- | :--- |
| `--all` | `-a` | Do not ignore entries starting with `.` \(_dotfiles_ are files and folders that are intentionally hidden, usually to reduce clutter_\)_ |
| `-l` | `-l` | Display data in a _long_ format |
| `-S` | `-S` | Sort by size, largest first |

{% hint style="info" %}
Remember that you can stack flags! Try looking into some of the options for each command, and see what outputs you can produce.
{% endhint %}

### CD

One of the commands you will use most often in Linux is `cd`. CD stands for **C**hange **D**irectory, which helps the user to move their current directory. Here are some examples of regular `cd` usage:

| Command | Usage |
| :--- | :--- |
| `cd` | Moves to the home directory |
| `cd ..` | Moves to the parent directory |
| `cd -` | Moves to the last directory. For example, you can use `cd /` to enter the root directory and `cd -` to return to your previous directory |
| `cd DIR` | Moves to the directory DIR |

### MKDIR

To create a folder in Linux, you can use the command `mkdir`. This command is relatively simple, with only basic application:

| Command | Usage |
| :--- | :--- |
| `mkdir DIR` | Creates an empty directory called DIR |
| `mkdir ../DIR` | Creates an empty directory called DIR in the parent directory |

### TOUCH

Similar to `mkdir`, `touch` is a command that creates an empty file at the specified location. Again, this command only has basic applications:

| Command | Usage |
| :--- | :--- |
| `touch test.txt` | Creates an empty file called `test.txt` |
| `touch ../test.txt` | Creates an empty file called `test.txt` in the parent directory |

{% hint style="info" %}
Keep in mind that most of these commands take a path as input, and therefore can be more than just one part. For example, you can use `cd ../../..` to travel many directories at once, or `mkdir ~/test` to create an empty directory in your `home`. Try playing around with more complicated directory usage now, as it will assist you later on with more complex folder structures!
{% endhint %}

