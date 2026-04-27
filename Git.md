# Part 1: The Absolute Essentials (Daily Drivers)
`If you only learn 8 commands, learn these.`

Command	What it does	When you use it
git init	Creates a new repo	Starting a new project
git clone <url> ⭐	Copies a remote repo	Joining an existing project
git status ⭐	Shows what's changed	Before EVERY commit
git add <file> ⭐	Stages changes	Preparing a commit
git add .	Stages all changes (current dir)	Quick staging
git add -A	Stages all changes (entire repo)	Safer than git add .
git commit -m "message" ⭐	Creates a snapshot	Saving your work
git commit -am "message"	Add + commit for tracked files	Speeds up small changes
git log ⭐	Shows commit history	Seeing what happened
git log --oneline --graph	Pretty history with branches	Understanding branch structure
git diff	Shows unstaged changes	"What did I just edit?"
git diff --staged	Shows staged changes	"What's about to be committed?"
---

# Part 2: Branching & Merging (Team Work)
`This is where Git becomes powerful.`

Command	What it does	When you use it
git branch ⭐	Lists local branches	Seeing where you can work
git branch <name>	Creates a branch	Starting a new feature
git branch -d <name>	Deletes a branch (safe)	Cleaning up merged branches
git branch -D <name>	Force deletes a branch	Deleting unmerged work (careful!)
git checkout <branch> ⭐	Switches branches	Moving between features
git checkout -b <name>	Creates + switches	One command for new feature
git switch <branch>	Newer alternative to checkout	More intuitive than checkout
git switch -c <name>	Create + switch (modern)	Preferred for Git 2.23+
git merge <branch> ⭐	Integrates another branch	Bringing feature into main
git merge --abort	Cancels a conflicted merge	When merging goes wrong
git log --graph --oneline --all	Visual branch diagram	Understanding complex history
---

# Part 3: Remote Repositories (Collaboration)
`Working with GitHub, GitLab, Bitbucket.`

Command	What it does	When you use it
git remote -v ⭐	Shows remote URLs	"Where am I pushing to?"
git remote add origin <url>	Adds a remote	Linking local to GitHub
git push origin <branch> ⭐	Uploads your commits	Sharing your work
git push -u origin <branch>	Push + set upstream	First push of a new branch
git push --force ⚠️	Overwrites remote	Rewriting history (dangerous!)
git pull ⭐	Fetch + merge	Getting latest changes
git pull --rebase	Fetch + rebase	Cleaner history (recommended)
git fetch	Downloads without merging	Seeing what's changed remotely
git fetch --prune	Removes deleted remote branches	Cleaning stale references
git clone --depth 1	Shallow clone	Huge repos (faster download)
---

# Part 4: Undoing & Fixing Mistakes
`The "oh no" commands. These separate juniors from seniors.`

Command	What it does	When you use it
git restore <file>	Discards unstaged changes	"Undo my edits since last commit"
git restore --staged <file>	Unstages a file	"I added that file by mistake"
git reset <file>	Older way to unstage	Same as restore --staged
git reset --soft HEAD~1	Undo commit, keep changes	"I forgot to add a file"
git reset --mixed HEAD~1 (default)	Undo commit + unstage	Default reset behavior
git reset --hard HEAD~1 ⚠️	Permanently delete commit	Nuclear option (loses changes!)
git revert <commit> ⭐	Creates inverse commit	Safely undo shared commits
git commit --amend	Edit last commit message or files	"Fix typo in previous commit"
git reflog ⭐	Shows ALL HEAD movements	Finding "lost" commits
git cherry-pick <commit>	Copies a commit to current branch	Taking one specific change
git blame <file>	Who changed each line?	Finding who broke something
---

# Part 5: Stashing (Temporary Work)
`I need to switch branches but I'm not ready to commit.`

Command	What it does	When you use it
git stash ⭐	Saves uncommitted work	Emergency branch switch
git stash push -m "message"	Named stash	Multiple stashes
git stash list	Shows all stashes	"What did I save?"
git stash pop ⭐	Applies + removes latest stash	Restore and clean
git stash apply	Applies without removing	Same stash to multiple branches
git stash drop	Deletes a stash	Cleaning up
git stash clear	Deletes ALL stashes	Nuclear cleanup
git stash branch <name>	Creates branch from stash	When stash conflicts
---

# Part 6: Rebasing (Clean History)
`Controversial but powerful.`

Command	What it does	When you use it
git rebase <branch> ⭐	Replays commits on another branch	Linear history
git rebase -i HEAD~3 ⭐	Interactive rebase (last 3 commits)	Squash, reorder, edit commits
git rebase --continue	Resumes after fixing conflicts	After resolving rebase conflicts
git rebase --abort	Cancels rebase	Return to original state
git rebase --skip	Skips a problematic commit	Rarely used
git pull --rebase	Fetch + rebase instead of merge	Avoid merge commits
Golden rule of rebasing: Never rebase public/shared branches (main/master). Only rebase your own feature branches.
---

# Part 7: Debugging & Inspection
`Finding bugs and understanding history.`

Command	What it does	When you use it
git log -S"text"	Search commits by text	"When did I delete that function?"
git log -L 10,20:file.js	History of specific lines	Who changed that line range?
git bisect start ⭐	Binary search for bugs	Finding which commit broke something
git bisect bad	Mark current commit as broken	Start of bisect
git bisect good <commit>	Mark known good commit	End of bisect
git bisect reset	End bisect session	Clean up
git grep "pattern"	Search tracked files	Faster than OS grep
git show <commit>	Shows commit details	What changed in that commit?
git whatchanged	Older alternative to log	Rarely used now
git shortlog -sn	Commits by author	"Who contributed the most?"
---

# Part 8: Configuration & Aliases
`Make Git work for YOU.`

Command	What it does	When you use it
git config --global user.name "Name"	Sets your identity	First-time setup
git config --global user.email "email"	Sets your email	First-time setup
git config --global core.editor "code --wait"	Sets VS Code as editor	Better commit messages
git config --global alias.co checkout	Shortcut	git co instead of git checkout
git config --global alias.tree "log --graph --oneline --all"	Visual tree alias	git tree
git config --global alias.unstage "reset HEAD --"	Unstage alias	git unstage file.txt
git config --list	Shows all config	Debugging Git behavior
My recommended aliases (put in ~/.gitconfig):

ini
[alias]
    co = checkout
    br = branch
    ci = commit
    st = status
    unstage = reset HEAD --
    last = log -1 HEAD
    tree = log --graph --oneline --all
    lol = log --graph --pretty=oneline --abbrev-commit
---

# Part 9: Advanced (But Still 90% Useful)
`Less common, but clutch when needed.`

Command	What it does	When you use it
git tag	Lists tags	Version releases
git tag -a v1.0 -m "message"	Creates annotated tag	Marking releases
git push --tags	Pushes tags to remote	Sharing releases
git worktree add ../project-fix bugfix	Multiple branches simultaneously	Context switching without stashing
git submodule add <url>	Adds another repo inside yours	Dependency management
git submodule update --init --recursive	Fetches all submodules	Clone with submodules
git clean -fd	Deletes untracked files/dirs	Cleaning build artifacts
git archive --format=zip HEAD	Exports repo without .git	Shipping source code
git rm --cached <file>	Removes from Git but keeps locally	Accidentally committed .env file
git gc	Garbage collection	Repo getting slow
