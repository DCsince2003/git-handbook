# Git Bash Commands
Personal notes from practicing Git Bash commands

## Important terms to be familiar with
| Term | Description |
| --- | --- |
| File | A container that stores some content inside (text, image, video files, etc.). |
| Directory | In the context of Command Line, _Folders_ are referred to as _Directories_. It's a container that holds files and other directories. |
| Path | A path is a digital address that tells the computer where a file or directory is located. |
| Current Directory | The directory you are currently inside (also known as Working Directory). |
| Command | An instruction you give to the computer. |
| Terminal | The text-based interface where user types the commands (e.g. Windows Terminal, Git Bash). |
| Shell | The program that understands and executes those commands (e.g. Powershell, Bash). |
> `User --> Terminal --> Shell --> Operating System`
#

### Basic Difference between CLI and GUI
| Command Line Interface (CLI) | Graphic User Interface (GUI) |
| --- | --- |
| Text-based Interface | Visual/Graphical Interface |
| Faster for repetitive tasks |  Intuitive and User-friendly |
| Consumes very little system memory and processing power | Requires Graphic Processing |
| Great for automation and development | Excellent for multimedia tasks like photo editing, gaming, etc.|
#

> #### My First Command:
> $ ` echo "Hello, World!" ` - Prints ***Hello, World!*** on the screen.😀 I guess it's a habit now.😄
#

## Basic commands:
### Quick overview and navigation

| Command | Purpose |
| --- | --- |
| `pwd` _(print working directory)_ | Show current directory |
| `ls` _(list)_ | List files and sub-directories inside your current directory |
| `cd` _(change directory)_ | Move to a different directory |

> | $ `pwd` <br> `/C/Users/thewe` |
> | :-- |

> | $ `cd Desktop` <br> $ `cd git-bash-practice` | or | $`cd Desktop/git-bash-practice` |
> | :-- | --- | :-- |

> | $ `ls` <br> `music-library/    recipe/    scavenger-hunt/` |
> | :-- |
#
### Creating new file and directory

| Command | Purpose |
| --- | --- |
| `mkdir` _(make directory)_ | create a new directory within the current directory |
| `touch` | Create a new file within the current directory |
| `code` | Open a new file within the VS Code editor |

> [!NOTE]
> `code` - works only when VS Code is installed
>
> use `charm` for pycharm, `atom` for atom, `subl` for sublime, etc.

> | $ `mkdir new-dr` <br> $`cd new-dr` <br> `/C/Users/thewe/Desktop/git-bash-practice/new-dr` |
> | :-- |

> | $ `touch wishlist.txt` <br> $ `ls` <br> `wishlist.txt`|
> | :-- |

> | $ `code pattern.py` |
> | :-- |
#
### Reading and Writing

| Command | Purpose |
| --- | --- |
| `echo` | write or append text directly to the terminal or a file |
| `cat` | read and display the contents of a file or write to another file |

> | $ `echo "Hello, World!" > greet.txt` <br> (Automatically create a new file if it does not exist) | ➜ | $ `cat greet.txt` <br> `Hello, World!` |
> | :-- | --- | :-- |

> | $ `echo "Hello, Friend!" > greet.txt` <br> $ `cat greet.txt` <br> `Hello, Friend!` <br> (replace the text in greet.txt with the new text) | or | $`echo "Hello, Friend!" >> greet.txt` <br> $ `cat greet.txt` <br> `Hello, World!` <br> `Hello, Friend!`  <br> (append the new text at the end of greet.txt) |
> | :-- | --- | :-- |

> | $ `cat wishlist.txt > to-do-list.txt` <br> (replace the text in to-do-list.txt with the text in wishlist.txt) | or | `cat wishlist.txt >> to-do-list.txt` <br> (append the text in wishlist.txt at the end of to-do-list.txt) |
> | :-- | --- | :-- |
#
### Moving, Renaming and Removing

| Command | Purpose |
| --- | --- |
| `mv` _(move)_ | move or rename files and directories |
| `rm` _(remove)_ | remove files and directories |
| `rmdir` _(remove directory)_ | remove empty directories |

> | $ `mv old-name.txt new-name.txt` <br> (file old-name.txt is renamed to new-name.txt) | ➜ | $ `cat old-name.txt` <br> `cat: old-name.txt: No such file or directory` |
> | :-- | --- | :-- |

> | $ `mv greet.txt ../directory-b` <br> (file greet.txt is moved to directory-b within parent directory) | ➜ | $ `cd ../directory-b` <br> $ `ls` <br> `greet.txt` |
> | :-- | --- | :-- |

> | $ `rm greet.txt` <br> (file greet.txt is removed) | ➜ | $ `cat greet.txt` <br> `cat: greet.txt: No such file or directory` |
> | :-- | --- | :-- |

> | $ `rmdir empty-dir/` <br> (directory empty-dir is removed) | ➜ | $ `cd empty-dir` <br> `bash: cd: name: No such file or directory` |
> | :-- | --- | :-- |

> | $ `rm -r directory-a/` <br> (directory-a is removed along with all its files) | ➜ | $ `cd directory-a` <br> `bash: cd: name: No such file or directory` |
> | :-- | --- | :-- |

> [!NOTE]
> If the second argument of `mv` is an existing file name then it will be overwritten and original file will be removed
>
> e.g. Suppose both greet.txt and wish.txt exists
>
> | $ `cat greet.txt` <br> `Hello, World!` | and | $ `cat wish.txt` <br> `Hello, Friend!` |
> | :-- | --- | :-- |
> 
> | $ `mv greet.txt wish.txt` | ➜ | $ `cat wish.txt` <br> `Hello, World!` | and | `cat: greet.txt: No such file or directory` |
> | :-- | --- | :-- | --- | :-- |
#
### Copying

| Command | Purpose |
| --- | --- |
| `cp` _(copy)_ | copy file or directory content |

> | $ `cp greet.txt ../directory-b/` <br> (Create a copy of greet.txt in directory-b) | ➜ | $ `cd ../directory-b` <br> $ `ls` <br> `greet.txt` |
> | :-- | --- | :-- |

> | $ `cp -r directory-a/ directory-b/` <br> (Create a copy of directory-a in directory-b) | ➜ | $ `cd directory-b` <br> $ `ls` <br> `directory-a/` |
> | :-- | --- | :-- |

> | $ `cp greet.txt wish.txt` <br> (Overwrite the contents of wish.txt with those in greet.txt) |
> | :-- |

> [!NOTE]
> If the second argument of `cp` is a file that does not exist then a new file will be automatically created.
>
> If the file already exists then its contents will be overwritten.
#
