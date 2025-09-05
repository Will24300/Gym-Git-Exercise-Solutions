# GIT Exercise

## Bundle 1

### Exercise 1

```bash

# initialize a git repository
$ git init                  # Create a new empty Git repository in the current folder

$ git status                # Show current status (changes, untracked files, branch info)

$ git branch -m master main # Rename the default branch from "master" to "main"

$ git status                # Check the branch name again and repository status

$ git add .                 # Stage all changes in the current directory for commit

$ git status                # Confirm that files are staged

$ git commit -m "Add new files" # Save staged changes into Git history with a commit message

$ git remote add origin https://github.com/Will24300/gym-exercise1.git # Connect local repo to GitHub
git branch -M main          # Force rename branch to "main" (capital M overwrites if exists)
git push -u origin main     # Push main branch to GitHub and set it as the upstream

$ git checkout -b div       # Create and switch to a new branch called "div"

$ git branch -m div dev     # Rename branch "div" to "dev"

$ git push origin dev       # Push "dev" branch to GitHub

$ git checkout -b test      # Create and switch to "test" branch

$ git push origin test      # Push "test" branch to GitHub

$ git checkout dev          # Switch back to "dev" branch

$ git branch -d test        # Delete the "test" branch locally

$ git push origin --delete dev  # Delete the "dev" branch on GitHub

```

### Exercise 2

```bash

$ git add home.html         # Stage home.html

$ git stash                 # Save staged changes temporarily (removes from working dir + staging)

$ git add about.html        # Stage about.html

$ git stash                 # Save about.html changes temporarily

$ git add team.html         # Stage team.html

$ git stash                 # Save team.html changes temporarily

$ git status                # Check working tree status

$ git stash list            # Show list of stashes (saved changes)

$ git stash pop stash@{1}   # Apply stash number 1 and remove it from stash list

$ git status                # Check what changes came back

$ git stash list            # Show remaining stashes

$ git stash pop stash@{1}   # Apply the next stash (new stash index after pop)

$ git status                # Verify applied changes

$ git add .                 # Stage all applied files

$ git push                  # Push committed changes to GitHub

$ git stash list            # Show if stashes remain

$ git stash pop stash@{0}   # Apply the last stash in the list

$ git reset --hard          # to rest all over my files


```

## Bundle 2

### Exercise 1

```bash
$ git checkout -b ft/bundle-2   # Create and switch to branch "ft/bundle-2"

$ git status                    # Check working directory status

$ git add services.html         # Stage services.html file

$ git commit -m "Add services file"  # Commit new services file

$ git push origin ft/bundle-2   # Push "ft/bundle-2" branch to GitHub

$ git checkout main             # Switch back to main branch


```

### Exercise 2

```bash
$ git checkout main             # Switch to main branch

$ git pull                      # Get the latest changes from GitHub

$ git checkout -b ft/service-redesign   # Create new branch "ft/service-redesign"

$ git status                    # Check changes status

$ git add .                     # Stage all changes

$ git commit -m "Update service page"   # Commit update

$ git push origin ft/service-redesign   # Push "ft/service-redesign" branch

$ git checkout main             # Switch to main branch

$ git add .                     # Stage main branch changes

$ git commit -m "Add changes to service page" # Commit on main branch

$ git push                      # Push changes to GitHub main

$ git checkout ft/service-redesign   # Switch to redesign branch

$ git pull                      # Update branch with remote changes

$ git merge main                # Merge main into ft/service-redesign (possible conflicts)

$ git add .                     # Stage resolved files

$ git commit                    # Finish merge commit

$ git push origin ft/service-redesign   # Push merged branch to GitHub


```

## Bundle 3

### Exercise 1

```bash
# Create and switch to a new branch called "ft/team-page"
$ git checkout -b ft/team-page

# Stage the new file team.html for commit
$ git add team.html

# Commit the staged changes with a message
$ git commit -m "Add team page"

# Push the ft/team-page branch to the remote repository (origin)
$ git push origin ft/team-page


# Switch back to the main branch
$ git checkout main

# Create and switch to a new branch called "ft/contact-page" from main
$ git checkout -b ft/contact-page

# Switch back to the ft/team-page branch
$ git checkout ft/team-page

# Show a short, one-line history of commits on the current branch
$ git log --oneline

# Switch again to the ft/contact-page branch
$ git checkout ft/contact-page

# Apply the changes from a specific commit (a5a66b6) made in another branch
$ git cherry-pick a5a66b6

# Check the status of the working directory and staging area
$ git status

# Stage all changes (new, modified, deleted files)
$ git add .

# Commit staged changes with a message
$ git commit -m "Copy team page "

# Push ft/contact-page branch with its commits to the remote
$ git push origin ft/contact-page


# Create and switch to a new branch called "ft/faq-page"
$ git checkout -b ft/faq-page

# Stage the new file faq.html
$ git add faq.html

# Commit the staged file
$ git commit -m "Add faq page"

# Push ft/faq-page branch to the remote
$ git push origin ft/faq-page


# Switch back to the ft/team-page branch
$ git checkout ft/team-page

# Show commit history in short form for ft/team-page
$ git log --oneline

# Undo the changes introduced by commit a5a66b6 by creating a new "revert commit"
$ git revert a5a66b6

# Push the new revert commit to the remote ft/team-page branch
$ git push origin ft/team-page


```

### Exercise 2

```bash

$ git checkout ft/faq-page                 # switch to existing feature branch
$ git checkout -b ft/home-page-redesign    # create and switch to new branch for redesign work
$ git checkout main                        # move to main branch
$ git status                               # check branch status and changes
$ git add index.html                       # stage index.html file
$ git commit -m "Add index file"           # commit index.html with message
$ git push                                 # push main branch to remote
$ git checkout ft/home-page-redesign       # switch back to redesign branch
$ git rebase main                          # reapply redesign commits on top of updated main
$ git add .                                # stage all modified files
$ git commit -m "Add features to home page" # commit redesign changes
$ git push origin ft/home-page-redesign    # push redesign branch to remote

```

## Bundle 4

### Exercise 1

```bash
# Switch to the main branch
$ git checkout main

# Add a new remote named "git-copy" pointing to another GitHub repo
$ git remote add git-copy https://github.com/Will24300/git-copy.git

# List all configured remotes (should now show "origin" and "git-copy")
$ git remote

# Stage the file home.html for the next commit
$ git add home.html

# Commit the staged changes with a message describing them
$ git commit -m "add some changes"

# Push the current branch (main) to the default remote "origin"
$ git push origin

# Push the same branch to the second remote "git-copy"
$ git push git-copy

```

### Exercise 2

```bash
$ git checkout -b ft/footer
# Create and switch to a new branch called 'ft/footer' from the current branch.

$ git add foo.html
# Stage the file 'foo.html' to include it in the next commit.

$ git commit -m "foo html"
# Commit the staged changes with the message "foo html".

$ git add foo.html
# Stage 'foo.html' again (likely after making new edits).

$ git commit -m "Add title"
# Commit the new staged changes with the message "Add title".

$ git push origin ft/footer
# Push the 'ft/footer' branch and its commits to the remote repository.

$ git checkout main
# Switch back to the 'main' branch.

$ git checkout -b ft/squashing
# Create and switch to a new branch called 'ft/squashing' from 'main'.

$ git merge --squash ft/footer
# Merge changes from 'ft/footer' into 'ft/squashing' as a single squashed commit
# (does not create merge commits; instead stages all changes at once).

$ git commit -m "footer changes squashing"
# Commit all the squashed changes as one commit with a descriptive message.

$ git push origin ft/squashing
# Push the 'ft/squashing' branch and its commit to the remote repository.


```

## Bundle 5

### Exercise 2

```bash

$ git add .
# Stage all modified, new, and deleted files in the current directory for the next commit.

$ git status
# Show the current status of the working directory and staging area
# (which files are staged, unstaged, or untracked).

$ git commit -m "Change the main title"
# Commit all staged changes with the message "Change the main title".

$ git push
# Push the current branch and its commits to the remote repository.



```
