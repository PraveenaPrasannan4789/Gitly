# Git Stash
Purpose: Temporarily save your uncommitted changes without committing them, so you can switch branches or pull updates.

# Save current changes
git stash

# Save changes with a message
git stash save "WIP: working on login form"

# List all stashes
git stash list

# Apply the most recent stash
git stash apply

# Apply a specific stash
git stash apply stash@{2}

# Drop a stash after applying
git stash drop stash@{0}

# Apply and remove from stash in one go
git stash pop





# Creating a New Branch Under Main Branch
# Switch to main branch
git checkout main

# Pull latest changes (optional)
git pull origin main

# Create a new branch and switch to it
git checkout -b feature/login-form

# Push branch to remote
git push -u origin feature/login-form







# Resetting a Commit
Soft reset: Keep changes in working directory, just undo last commit.

# Undo last commit but keep changes staged
git reset --soft HEAD~1

Mixed reset: Undo last commit and unstage changes (default).

# Undo last commit, changes remain in working directory but unstaged
git reset HEAD~1

Hard reset: Delete last commit and discard changes completely.

# Warning: deletes commit and local changes
git reset --hard HEAD~1