# Starting out with Git
To actually use Git, you will first require a git account, [Github](https://github.com/). If you need to install git, follow the official [Git Guide](https://github.com/git-guides/install-git).
You will probably need to link up git with access tokens or your SSH Keys, then you can clone the repository to your local machine. ([Tutorial](https://www.youtube.com/watch?v=yVP3sYgd0bY)). To gain access to the repository shoot me a quick text containing your Github account name or email, then I can invite you to the repository as a Developer.

# Using Git
You can either use git from your command line or find various applications that provide a more understandable interface for you (such as [VSCode](https://code.visualstudio.com/?_exp_home=e855cfac50) or [Fork](https://git-fork.com/)).

# Important Git Commands

| git command                   | action                         |
| ----------------------------- | -----------------------------  |
| - git clone *repository name* | Clones the remote repository to your local machine |
| - git pull | fetches changes from current remote branch and merges them with local changes |
| - git add . | Adds all changed files to next commit |
| - git add *filepath* | Adds changed file to next commit |
| - git add *filepath* | Adds changed file to next commit |
| - git commit -m "*commit message*" | Commits changes !locally! with a commit message |
| - git push | Pushes local changes to remote |
| - git branch *branch name* |  creates a new local branch with the branch name |
| - git checkout *branch name* | checks out said branch. Committed changes on another branch are not migrated to this branch |
| - git push --set-upstream origin *branch name* | pushes branch, as well as changes committed to it |
| - git restore . | revert local changes (excluding local commits) |
| - git revert *commit name* | reverts local commit |
| - git reset | reset local changes to master |

All of these commands are typically found within your application of choice or can be executed from your command prompt.

## Order of commands
Typically when working with other people on a project you want to Pull -> Commit -> Push. Preserving this order means that before you push you are up to date and have no merge conflicts to resolve when pushing. Git will warn you about changes that conflict with your local files when pulling, and having to fix a merge issue when pushing can become a bit of a headache.

## Creating Commits
Sizes of commits can vary, however ideally all commits contain a unique prefix or identifier and only actually modify one aspect of the software. Typically the following are used:
-feat: A new feature / change to this branch
-ref: A refactoring of existing objects (code, variable values, optimizations, ...)
-fix: fix of a bug
I have found these to be enough for most of the projects I have worked on, but on occasion you might need to come up with something new (e.g. minor changes that are too small to be considered a feature but too unique to be considered a refactor, just go with your gut when you find yourself in this situation). A commit message then typically looks like this:  "feat: Created Movement Component and appended it to the Character". 
Ideally only commit files you know you made changes to. Also as this is a private project, while I encourage keeping clean commits I can appreciate that game development becomes frustrating on occasion and have seen a fair share of commit messages representing this.


## Branching
Typically Branches are created for major changes, such as Game Design implementation, Optimization, etc. You use these to isolate your work from the main branch, resulting in less merge conflicts. Your use case for a branch will be somewhat similar to the previously mentioned creation of commits (where you focus on one major feature, refactor or fix per branch). Also, you don't need to pull every branch, only the one you are currently working on. One branch (typically "main") is the master branch. Ideally you work as little as possible on this branch, only using it for small changes and branch merges. It captures the current state of the project, and ideally always builds without compilation errors.

## Merging
Merging is ideally fairly simple. You pull or push, and if you desire to merge two branches, you use the [Git Website](https://github.com/) or your GUI application. !When merging a branch onto main, make sure you pull from main first! Also, merges are on completion local changes first (unless you are using the website), and need to be pushed.

### Resolving Merge Conflicts
Ack! an error has occurred. These happen when written code conflicts between two commits. Git will try to solve this for non binary files (e.g. Code), but these solves aren't always perfect and binary files (e.g. images) always result in merge conflicts. (This especially sucks with Unreal Engine, as blueprints are currently stored in binary). When these occur, Git (or your GUI) will show you the origins of the conflicts, where you can choose what version to keep. Once you have worked through all the files, the merge conflict is resolved. These changes are however only local and need to be pushed.

# Some final words
Tysm for reading all of this! I implore you to try out some of the mentioned commands, especially getting the hang of the commits is important. Notably one of the benefits of versioning is the ability to undo changes (aside from a few), so making mistakes is far from the end of the world. Shoot me a text if you need help with anything!