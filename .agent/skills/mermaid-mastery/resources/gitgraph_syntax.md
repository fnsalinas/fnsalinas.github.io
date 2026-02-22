# GitGraph Syntax

## Syntax
```mermaid
gitgraph
   commit
   commit
   branch develop
   checkout develop
   commit
   commit
   checkout main
   merge develop
   commit
   commit
```

## Commands
- `commit`: Create a new commit node
  - `id: "message"`
  - `type: HIGHLIGHT | REVERSE | NORMAL`
  - `tag: "v1.0"`
- `branch name`: Create new branch
- `checkout name`: Switch to branch
- `merge name`: Merge branch into current
- `cherry-pick id`: Cherry pick commit
