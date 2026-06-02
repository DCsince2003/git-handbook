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
> | :-- | --- | --- |
> 
> | $ `pwd` <br> `/C/Users/thewe/Desktop/git-bash-practice` |
> | :-- |

> | $ `ls` <br> `music-library/    recipe/    scavenger-hunt/` |
> | :-- |
#
### Creating

| Command | Purpose |
| --- | --- |
| `mkdir` _(make directory)_ | create a new directory within the current directory |
| `touch` | Create a new file within the current directory |
| `code` | Open a new file within the VS Code editor |
> [!NOTE]
> `code` - only for VS Code 
>
> use `charm` for pycharm, `atom` for atom, `subl` for sublime, etc.

> | $ `mkdir new-dr` <br> $`cd new-dr` <br> `/C/Users/thewe/Desktop/git-bash-practice/name` |
> | :-- |
