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
| Branch | An independent line of development within a repository |
| Main/Master | The primary branch of a repository |
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

> | $ `git init` <br> Initialized empty Git repository in /path/to/your/project/.git/ |
> | :-- |

> | `git remote add origin <repo_url>` <br> `add` - Add a new remote connection <br> `origin` - _(commonly used)_ Alias for the repo's url <br> `<repo_url>` - placeholder for the url |
> | :-- |

> | `git clone <repo_url>` |
> | :-- |

> [!NOTE]
> If you have a local repo and want to link it with a new github repo then use `git init` to initialize your local repo <br> and then `git remote` to link it with the remote repo.
>
> If you want to import a copy of an already existing remote repo to your local workspace then import them using `git clone`.
#

### Stage, Unstage, and Commit Changes

| Command | Purpose |
| --- | --- |
| `git add` | Stage the changes to be committed |
| `git restore` | Revert the changes or unstage them |
| `git commit` | Track progress and separate different actions in your code |

> | `git add README.md` <br> (Stage changes made in the README file) |
> | :-- |

> | `git add .` <br> (Stage all changes made in the working directory) |
> | :-- |

> | `git add *.css` <br> (Stage every file with .css extension) |
> | :-- |

> | `git restore index.html` <br> (Revert the changes made to the index.html file to its previously staged state) |
> | :-- |

> | `git restore --staged index.html` <br> (Unstage index.html file) |
> | :-- |

> | `git commit` | or | `git commit -m "Update README"` |
> | :-- | --- | :-- |
#

