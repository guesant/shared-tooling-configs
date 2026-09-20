# Git

## Inspect

```bash
git status
git diff
git diff --staged
git log --oneline --decorate --graph -20
```

## Inspect an object or revision

```bash
git show HEAD
git rev-parse HEAD
git rev-parse --show-toplevel
```

## Branches

```bash
git switch branch-name
git switch -c new-branch
```

## Restore

Restore a working-tree file:

```bash
git restore path/to/file
```

Unstage without changing the working tree:

```bash
git restore --staged path/to/file
```

## Reflog

```bash
git reflog
```

## Worktrees

```bash
git worktree list
git worktree add ../worktree branch-name
```
