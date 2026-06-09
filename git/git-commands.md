# Git Commands
Personal notes from practicing Git commands

## Important terms to be familiar with
| Term | Description |
| --- | --- |
| Git | A distributed version control system used to track changes in code |
| GitHub | A web-based platform for hosting Git repositories and collaborating on code |
| Repository _(Repo)_ | A storage location containing a project's files and Git history |
| Remote Repository | Git repository hosted on a server _(like GitHub)_ used to share and sync code |
| Local Repository | Git repository stored on your local device |
| Workind Directory | The current files and folders you are actively editing |
| Staging Area _(Index)_ | A temporary area where changes are prepared before committing |
| Commit | A saved snapshot of the project's state at a specific time |
| Push | Upload your local commits to a remote repository to share your code |
| Pull | Download and merge changes from a remote repository into your local branch |
| Branch | An independent line of development within a repository |
| Main/Master | The primary branch of a repository |
| HEAD | A pointer to the currently checked-out commit or branch |
| Merge | The process of combining changes from one branch into another |
| Merge Conflict | A situation where Git cannot automatically reconcile conflicting changes |
| Pull Request _(PR)_ | A request to review and merge code change |
#

### Basic Difference between Git and GitHub
| Git | GitHub |
| --- | --- |
| A software tool _(command-line program)_ | A web-based platform _(website)_ |
| Installed locally on your computer |  Hosted online in the cloud |
| Tracks history and manages code changes | Stores your Git repositories online so others can collaborate |
| Works completely offline | Requires an internet connection to sync |
#

## Basic commands:
### Initialize, Link, and Clone

| Command | Purpose |
| --- | --- |
| `git init` | Initialize your local repository |
| `git remote` | Link your local repository with a new online repository |
| `git clone` | Create a copy of an existing repository on your local device |

> | $ `git init` |
> | :-- |

> | `git remote add origin <repo_url>` <br> `add` - Add a new remote connection <br> `origin` - _(commonly used)_ Alias for the repo's url <br> `<repo_url>` - placeholder for the url |
> | :-- |

> | `git clone <repo_url>` |
> | :-- |
#
