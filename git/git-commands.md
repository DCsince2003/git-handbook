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
| Merge | Combine the independent history and code changes from one branch into another |
| Merge Conflict | A situation where Git cannot automatically reconcile conflicting changes |
| Fork | Create a personal copy of someone else's repository |
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
| `git clone` | Create a local copy of an existing remote repository |

> | $ `git init` <br> Initialized empty Git repository in /path/to/your/project/.git/ |
> | :-- |

> | $ `git remote add <name> <repo_url>` <br> `add` - Add a new remote connection <br> `<name>` - Alias for the repo's url _('origin' is a commonly used name)_ <br> `<repo_url>` - placeholder for the url |
> | :-- |

> | $ `git clone <repo_url>` |
> | :-- |

> [!NOTE]
> To connect a local project to a new GitHub repository, first initialize the local repository with `git init`, <br> then link it to the remote repository using `git remote`.
>
> To create a local copy of an existing remote repository - including its complete commit history and branches, use `git clone`.
#

### Stage, Unstage, and Commit Changes

| Command | Purpose |
| --- | --- |
| `git add` | Stage the changes to be committed |
| `git restore` | Revert the changes or unstage them |
| `git commit` | Track progress and separate different actions in your code |
> <img width="2888" height="964" alt="git add and commit workflow" src="https://github.com/user-attachments/assets/e41fae25-2857-49a5-8ffb-01c533ca394a" />

> | $ `git add README.md` <br> (Stage changes made in the README file) |
> | :-- |

> | $ `git add .` <br> (Stage all changes made in the working directory) |
> | :-- |

> | $ `git add *.css` <br> (Stage every file with .css extension) |
> | :-- |

> | $ `git restore index.html` <br> (Revert the changes made to the index.html file to its previously staged state) |
> | :-- |

> | $ `git restore --staged index.html` <br> (Unstage index.html file) |
> | :-- |

> | $ `git commit` | or | $ `git commit -m "Update README"` |
> | :-- | --- | :-- |
#

### Check Current Status

| Command | Purpose |
| --- | --- |
| `git status` | Check file changes, see staged updates, and plan your next commit |

> | $ `git status` <br> On branch main <br> Your branch is up to date with 'origin/main'. <br><br> nothing to commit, working tree clean |
> | :-- |

> | $ `git status` <br> On branch main <br> Your branch is up to date with 'origin/main'. <br><br> Changes not staged for commit: <br> &emsp; (use "git add \<file>..." to update what will be committed) <br> &emsp; (use "git restore \<file>..." to discard changes in working directory) <br> &emsp;&emsp;&emsp; modified:   email_simulator.py <br><br> Untracked files: <br> &emsp; (use "git add \<file>..." to include in what will be committed) <br> &emsp;&emsp;&emsp; test_run.py <br><br> no changes added to commit (use "git add" and/or "git commit -a") |
> | :-- |
#

### Push The Changes

| Command | Purpose |
| --- | --- |
| `git push` | Send your local commits to a remote repository online |

> | $ `git push origin main` <br> (Push the _main_ branch to the remote _origin_) |
> | :-- |

> | $ `git push` <br> (Push the current branch to its remote _"tracking branch"_) |
> | :-- |

> | $ `git push -u origin <name>` <br> (Push a branch that you've never pushed before) |
> | :-- |
#

### Pull The Changes

| Command | Purpose |
| --- | --- |
| `git fetch` | Download remote changes without modifying your current local branch or files |
| `git pull` | Fetch and merge remote changes into your current local branch automatically |
> <img width="3364" height="924" alt="git push, fetch and pull workflow" src="https://github.com/user-attachments/assets/2dd5cc3b-7962-42a9-acb1-288d3be2303f" />

> | $ `git fetch` <br> (Download all remote updates without changing current branch) |
> | :-- |

> | $ `git fetch origin main` <br> (Download main changes without modifying current branch) |
> | :-- |

> | $ `git pull` <br> (Update current branch with latest remote changes) |
> | :-- |

> | $ `git pull origin main` <br> (Update current branch with latest changes from main) |
> | :-- |
#

### Branching

| Command | Purpose |
| --- | --- |
| `git branch` | Create, list, rename, and delete branches in a Git repository |
| `git switch` | Switch between branches and create new branch when required |

> | $ `git branch` <br> (List all local branches) | or | $ `git branch -r` <br> (List remote branches only) | or | $ `git branch -a` <br> (List local and remote branches) |
> | :-- | --- | :-- | --- | :-- |

> | $ `git branch <new-branch>` <br> (Create a new branch) | or | $ `git switch -c <new-branch>` <br> (Create and switch to a new branch)
> | :-- | --- | :-- |

> | $ `git branch -m <new-name>` <br> (Rename the current branch) |
> | :-- |

> | $ `git branch -d <branch-name>` <br> (Delete a merged branch) |
> | :-- |

> | $ `git switch <branch>` <br> (Switch to an existing branch) |
> | :-- |
#

### Merge your branch

| Command | Purpose |
| --- | --- |
| `git merge` | Merge parallel work while retaining the full development timeline |

> | $ `git merge <branch>` <br> (Merge specified branch into current branch) |
> | :-- |

> [!NOTE]
> Merge Conflict happens when:
> - Changes are made to the same part of a file
> - One branch has deleted a file while the other branch has modified it
>
> Resolve Merge Conflict:
> - _Accept Incoming Changes_ -  Overwrites changes on the current branch with changes from the branch being merged in
> - _Accept Current Changes_ - Keeps changes on the current branch, and ignores changes from the branch being merged in
> - _Accept Both Changes_ - Keeps both branch versions of the changed lines or files
#

## The GitHub Flow

> <img width="2168" height="988" alt="the github flow" src="https://github.com/user-attachments/assets/ed6c238a-1849-44a5-a4e4-39920b00526c" />

#
