# Git Clean repo

## See current state
`git status`

## See what would be removed first
`git clean -fdx`

## Discard edits to tracked files
`git reset --hard`

## Remove all untracked (and ignored) files/dirs
`git clean -fdx`

## If someone left stashes (rare, but can show as “not clean” in some checks)
`git stash clear`

## Verify
`git status`
