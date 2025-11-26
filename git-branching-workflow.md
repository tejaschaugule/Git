# Git Branching Workflow

## 1. Check the Current Branch
```bash
git branch
```
- Lists all branches in your local repository.  
- The branch with `*` is your current branch.

## 2. Create a New Branch
```bash
git branch <branch-name>
```
- Creates a new branch from your current branch.  
**Example:**
```bash
git branch feature-branch
```

## 3. Switch to the New Branch
```bash
git checkout <branch-name>
# or
git switch <branch-name>
```

## 4. Create Files in the New Branch
- Now you can create or modify files in the new branch.

## 5. Add and Commit Changes
```bash
git add <file-name>
git commit -m "Your commit message"
```
- **Note:**
- Before adding and committing, the new file is **not visible in other branches**.  
- After committing, the changes exist only in the current branch.

## 6. Merge Branches
```bash
git checkout master
git merge <branch-name>
```
- Merges the specified branch into the current branch (`master` in this example).  
- **Note:** Always checkout the branch where you want to merge changes before merging.

## 7. Push Code to Central Repository
```bash
git push -u origin master
```
- Pushes your local changes to the remote repository.

## 8. Delete a Branch
```bash
git branch -d <branch-name>   # Safe delete (only if merged)
git branch -D <branch-name>   # Force delete
```

✅ **Tip:** Always make sure your changes are committed before switching branches to avoid losing work.
