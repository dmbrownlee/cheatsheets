# git Quick Reference
Main site (git): [git-scm.com](https://git-scm.com/)
Main site (GitHub): [GitHub]()
Quick and easy tutorials: [GitHub Guides](https://guides.github.com/)

## Terminology
Term | Definition
--- | ---
<code>git</code> | A distributed version control system.
version control system (VCS) | The software used to facilitate the practice of Software Configuration Management (SCM).</br>A VCS manages multiple versions (aka revisions) of files in a project.
Software Configuration Management (SCM) | The practice of managing software configurations over time to facilitate</br>j the devolopment of software in a controlled, repeatable way.
software configuration | A snapshot of all the files in a software project at a particular point in time.</br>Software configurations are identified by commit IDs.
repository | The data storage area of a VCS where all versions of all files and the commit metadata are stored.
remote | Another repository that synchronizes files with the local repository.
workspace | A local copy of a particular software configuration which you can edit
staging area | A place to store edited files temporarily prior to commiting them to the repository.  The staging area is also called the "cache".
commit | The act of creating a new software configuration reference by an commit ID.</br>This new configuration includes all the changed files placed in the staging area</br>and all unchanged files.
GutHub | An application service provider that provides hosting for git repositories, both free and for paid subscriptions.</br>In cloud terminology, this is hosted git repositories using the Software as a Service (SaaS) model.

## Creating a remote repository on GitHub

### Create a new, empty repository
You can create a new, empty repository by clicking the + in the upper left corner of the GitHub page header and choosing "New Repository" from the pop-up menu that appears. For a quick tutorial that includes working with the new repository, see [Hello World](https://guides.github.com/activities/hello-world/)


### Fork (copy) an existing repository
If you want to contribute to an existing project, start by making a fork (copy) of the project.  You then work with your copy as the remote repository.  Because your fork and the original project have a common ancestor, you can share your changes with the original project through pull requests.  For more information, see [Forking Projects](https://guides.github.com/activities/forking/)

## Creating a local repository and initial workspace
Get started with your local repository with these command.

git command line | Description
--- | ---
<code>git clone *\<repo URL\>*</code> | This creates a local git repository which is a copy of your remote GitHub</br>repository. You can work with the local copy even when disconnected and</br>push changes in your local repo to GitHub to share with others. This also</br>checks out a workspace (directory where you edit files) in the current</br>directory. Example:</br><code>git clone https://github.com/dmbrownlee/cheatsheets.git</code>
<code>git config *[--global]* user.name "*your name*" | Use the --global option to apply this configuration change to all git</br>workspaces on the local system or run this within a workspace to change</br>the setting for just that workspace.  This sets how your name will</br>appear in commits.  Keep in mind this is publically visible if you are</br>pushing changes to a public repository on GitHub.
<code>git config *[--global]* user.email "*your email address*" | Use the --global option to apply this configuration change to all git</br>workspaces on the local system or run this within a workspace to change</br>the setting for just that workspace.  This sets how your email address</br>will appear in commits.  Keep in mind this is publically visible if you are</br>pushing changes to a public repository on GitHub. It is **strongly**</br>recommended you set this to *your_github_username*@users.noreply.github.com</br>to avoid sharing your actual email address with spammers and other creeps.
<code>git config *[--global]* -l | Use the --global option to list your current config

## File states within your workspace
State | Description
--- | ---
Untracked | New files in your workspace.  These files do not yet exist in the repo. If you never want to add them to the repo, you can add them to the ```.gitignore``` file in the root of the workspace to prevent them from appearing in your status output.
Modified | These files have changes in your workspace that have not been staged for commit.
Staged | These files have changes that will be saved to the repo on the next commit.
Commited | These files are unchanged from the version stored in the repo.  These files do not appear in the output of ```git status```.

## Working with your repo
You will use these commands often.

git command line | Description
--- | ---
<code>git pull</code> | Sync the contents of the remote repository down to your local repository. If there are changes in your local repository which have not been pushed to the remote repository, manual intervention may be required to merge the new content.
<code>git status</code> | Get the status of files in the current workspace.
<code>git diff *file*</code> | Show how the verion of *file* in the workspace differs from the version stored in the local repo.
<code>git restore *file*</code> | Checkout the version of *file* stored in the repository and discard the changes to *file* in the workspace.
<code>git add *file*</code> | Copy the modified version of *file* in the workspace to the staging area for the next commit.
<code>git diff --cached *file*</code> | Show how the verion of *file* in the staging area differs from the version stored in the local repo.
<code>git commit -m "*message*"</code> | Commit all the files in the staging area to the repo as a single change with a descriptive message for the log.
<code>git log --oneline --graph --decorate</code> | Shows a compact history of commits in the repo.
<code>git log --oneline --since "$(date -v0H -v0M -v0S -v-7d)"</code> | Shows a compact history of commits over the last 7 days.
<code>git log --stat</code> | Shows more detailed information about the commit history.
<code>git push</code> | Sync the contents of your local repository up to the remote repository. If there are changes in your local repository which have not been pushed to the remote repository, manual intervention may be required to merge the new content.
