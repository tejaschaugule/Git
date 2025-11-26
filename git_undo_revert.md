# Git Undo and Revert Commands

This document provides common Git commands to **undo changes**, **unstage files**, and **revert commits**.

---

## 1. Undo changes in the working directory

If you have modified a file but **haven’t staged it** yet, you can restore it to the last committed version:

```bash
git checkout -- <filename>
```

**Example:**

```bash
git checkout -- test.txt
```

---

## 2. Revert changes in the staging area

If you have staged a file using `git add` but **haven’t committed it**, you can unstage it while keeping your changes in the working directory:

```bash
git reset <filename>
```

**Example:**

```bash
git reset test.txt
```

* The file is removed from the staging area
* Your edits remain in the working directory

### Unstage all staged files:

```bash
git reset
```

---

## 3. Revert a commit

If you want to undo a commit but **keep Git history intact**, use `git revert`:

```bash
git revert <commit-id>
```

* This **does not remove the old commit**
* Creates a **new commit** that reverses the changes of the specified commit

---

## 4. Remove the last commit (not pushed yet)

If you want to completely remove the **most recent commit**:

```bash
git reset --hard HEAD~1
```

* Deletes the last commit and all changes in it from the working directory
* ⚠ Warning: This is destructive — changes will be lost

If you want to **keep the changes** but remove the commit:

```bash
git reset --soft HEAD~1
```

* Commit is removed
* Changes remain staged in the working directory

---

## Summary of Commands

| Stage/Goal                     | Command                  | Effect                         |
| ------------------------------ | ------------------------ | ------------------------------ |
| Undo working directory changes | `git checkout -- <file>` | Restore last committed version |
| Unstage a file                 | `git reset <file>`       | Remove from staging            |
