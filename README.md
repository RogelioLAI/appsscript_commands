# Commit New Changes from VS Code to GitHub and Apps Script

This guide explains how to save new code changes from VS Code, upload them to GitHub using a new branch, merge the changes into the `main` branch using a Pull Request, and finally push the updated code to Apps Script using `clasp`.

---

## 1. Review Your Changes

Before committing, check which files were modified:

```bash
git status
```

This command shows the files that were added, modified, or deleted.

---

## 2. Create a New Branch

Create a new branch for your changes:

```bash
git checkout -b branch-name
```

Replace `branch-name` with a short name that describes your update.

Example:

```bash
git checkout -b update-pull-sheet-code
```

Using a branch is important because the `main` branch is protected, so changes must be merged through a Pull Request.

---

## 3. Add Your Changes

Add all modified files to the commit:

```bash
git add .
```

This stages all current changes so they can be included in the next commit.

---

## 4. Commit Your Changes

Create a commit with a clear description:

```bash
git commit -m "Commit description"
```

Example:

```bash
git commit -m "Updating pull sheet code"
```

The commit message should briefly explain what was changed.

---

## 5. Push the Branch to GitHub

Send your new branch to GitHub:

```bash
git push -u origin branch-name
```

Example:

```bash
git push -u origin update-pull-sheet-code
```

The `-u` option connects your local branch with the remote branch on GitHub. After this, future pushes from the same branch can be done with only:

```bash
git push
```

---

## 6. Create and Merge the Pull Request

After pushing the branch:

1. Go to the GitHub repository.
2. Open a Pull Request from your branch into `main`.
3. Review the changes.
4. Merge the Pull Request.

Once the Pull Request is merged, the changes will be added to the `main` branch.

---

## 7. Move Back to the Main Branch

After the Pull Request is merged, return to the `main` branch in VS Code:

```bash
git checkout main
```

---

## 8. Pull the Latest Changes from GitHub

Update your local `main` branch with the latest changes from GitHub:

```bash
git pull origin main
```

This makes sure your local project has the same code that was merged into GitHub.

---

## 9. Push the Changes to Apps Script

Finally, send the updated code to Apps Script:

```bash
clasp push
```

This uploads the local project files to the connected Apps Script project.

---

## Complete Command Flow

```bash
git status
git checkout -b branch-name
git add .
git commit -m "Commit description"
git push -u origin branch-name
```

After merging the Pull Request on GitHub:

```bash
git checkout main
git pull origin main
clasp push
```
