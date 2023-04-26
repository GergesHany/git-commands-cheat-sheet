## A Cheat Sheet for Git Commands 


## sessions to learn git

- [Ahmed Hossam](https://www.youtube.com/watch?v=Dty7VkzHvbI&t=369s)
- [Ahmed Sami](https://www.youtube.com/watch?v=Q6G-J54vgKc&t=5425s)

<hr>

## Content

- [Install Git](#Install-Git)
- [Git Terminologies](#Git-Terminologies)
- [Git Configuration](#Git-Configuration)
- [Set Up a Git Repository](#Set-Up-a-Git-Repository)
- [Local File Changes](#Local-File-Changes)
- [Declare Commits](#Declare-Commits)
- [Branching](#Branching)



<hr>

### Install Git

Open your terminal and run these commands

```bash
sudo apt update
sudo apt upgrade
sudo apt install git
```

<hr>

## Git Terminologies
| Git Command | Description |
| - | - |
| Bare Repository    | A branch is an active area of development in Git. The most recent commit shows the tip of the branch. |
| Branch | A branch is an active area of development in Git. The most recent commit shows the tip of the branch. |
| Blame | Describes the last modification to every line in the file. Shows Revision, Author & Time. |
| Checkout | This refers to the process in which any given commit is selected from the repository and the state of the associated file and the directory tree is recreated in the working directory. |
| Commit | This is a single point in Git history which holds the information about a changeset. |
| Detached Head | The state in which a specific commit is checked out instead of a branch. |
| Fetch | Fetching means to get latest changes in the branch and the local/remote repos. |
| Hash | A named reference to the Commit at the tip of a Branch |
| Head | A named reference to the Commit at the tip of a Branch |
| Index | A collection of files with state information. |
| Merge | To bring out the content of another Branch in the current Branch. |
| Master | The default development Branch in Git |
| Origin | The default Upstream Repository |
| Pull Request | Suggests changes into the Master Branch |
| Push | Pushes new changes after Committing them |
| Repository | A collection of Commits, Branches and Tags to identify Commits. |
| Working Tree | The tree of actual checked out files |

<hr>

## Git Configuration
| Git Command | Description |
| - | - |
| git config --global user.name `"Your Name"`    |  Set the username to be used for all actions |
| git config --global user.email `"Your email"`   | Set the email to be used for all the actions. |
| git config –global alias. | Create a shortcut for the Git command. |
| git config –system core.editor | Set the text editor for all the command actions. |
| git config –global –edit | Open global configuration file in the text editor for manual editing. |
| git config –global color.ui auto | Enable helpful colourization of command line outputs. |

<hr>

## Set Up a Git Repository
| Git Command | Description |
| - | - |
| git init | Initialize an empty Git repo in the current project. |
| git clone (Repo URL) | Clone the repository from GitHub to the project folder. |
| git clone (Repo URL) (Folder ) | Clone the repository into a specific folder. |
| git remote add origin (`https://github.com/username/(repo_name).git`) | Create a remote repo pointing on your existing GitHub repository. |
| git remote | Shows the name of remote repositories. |
| git remote -v | Shows the name and the URL of the remote repositories. |
| git remote rm (remote repo name) | Removes the remote repository. |
| git remote set-url origin (git URL) | Changes the URL of the repository. |
| git fetch | Get the latest changes from the origin but not merge. |
| git pull | Get the latest changes from the origin and merge them. |



<hr>

## Local File Changes
| Git Command | Description |
| - | - |
| git add (file name) | Add the current changes to the file to staging.  |
| git add . | Add the whole directory changes to staging (no delete files). |
| git add -A | Add all new, modified and deleted files to staging. |
| git rm (file_name) | Removes the file and untracks (stop tracking) it. |
| git mv  (file_name) (new_file_name) | Changes the filename and prepare it for Commit. |
| git checkout <deleted file name> | Recovers the deleted file and prepares it for Commit |
| git status | Shows the status of the modified files. |
| git ls-files –other –ignored –exclude-standard | Shows the list of all ignored files. |
| git diff | Shows unstaged changes in the index and the working directory. |
| git diff –staged | Shows file differences between staging and the last file version. |
| git diff (file_name) | Shows changes in a single file compared to the last Commit. |

<hr>

## Declare Commits
| Git Command | Description |
| - | - |
| git commit -m “(message)” | Commit the changes with a message |
| git commit -am “(message)” | Add all changes to staging and commit them with message |
| git checkout <commit hash> | Switch to the provided commit |
| git show <commit hash> | Outputs metadata and content changes of the specified commit |
| git reset <commit hash> | Undo all commits after this commit. Preserving changes locally |
| git reset --hard <commit hash> | Discard all history and changes back to the given commit |
| git reset --hard Head | Discard all local changes in working directory |
| git log | Show history of changes |
| git log -p | Shows the full display of each commit |
| git log -oneline | Shows the list of commits with only message |
| git log --follow (file_name) | List all the history for the current file |
| git blame (file_name) | Shows all changes with name of user |
| git stash | Temporarily saves all modified tracked files |
| git stash pop | Restores the most recently stashed files |
| git stash list | List all stash changedsets |
| git stash apply | Apply the latest stashed contents |
| git stash drop | Discard the most recently stashed files |
| git stash apply (stash id) | Re-Apply a specific stash content by ID |
| git stash drop (stash_id) | Drop a specific stash content by ID |
| git push | Push changes to the Origin |
| git push origin (branch_name) | Push branch to the Origin |
| Git push -f origin (branch_name) | Force push the changes to the origin |
| git tag (tag_name) | Define tag for a version |

<hr>  
  
## Branching
| Git Command | Description |
| - | - |
| git branch | Shows the list of all branches |
| git branch <branch_name> | Create a new branch |
| git branch -a | List all branches local and remote |
| git branch -m <old_name> <new_name> | Rename the branch |
| git checkout -b <branch_name> | Create a branch and switch to it |
| git checkout -b <new_branch_name> origin/<branch_name> | Get a remote branch from origin to the local directory |
| git branch -d <branch_name> | Delete a specified branch |
| git merge <branch_name> | Merge the current branch into master(first checkout to master) |
| git rebase <branch_name> | Take all the changes of the branch and restate on other. |
| git rebase <base> | Rebase the current branch onto base. Base can be a commit ID or branch name. |
| git fetch remote <branch_name> | Fetches the specific branch from the repository |
| git diff <branch_name>..<branch_name> | Shows the differences of two branches |
| git pull --rebase | Fetch the remote’s copy of current branch and rebases it into the local copy |
| git push --all | Push all of your local branches to the specified remote |  
