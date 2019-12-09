% GIT(shell) Um Pages | Um Pages
%
% August 23, 2018
# NAME
git --

# EXAMPLES

## Reset local repository to same state as remote origin

`git fetch origin`
`git reset --hard origin/master`

## Get commit counts by author
`git shortlog -s -n`

## Get commit counts by author, email
`git shortlog -s -n -e`

## Edit name of the current branch
`git branch -m <name>`

## List remote Git branches and the last commit date for each branch.
for branch in `git branch -r | grep -v HEAD`;do echo -e `git show --format="%ci %cr" $branch | head -n 1` \\t$branch; done | sort -r

Source: https://gist.github.com/jasonrudolph/1810768

## Show GitHub style branch diff for merge commit
1. git show {commit} --> pick Merge commit ids
2. git diff {commit1}...{commit2} --shortstat

## Show one commit in difftool
`git difftool abc123~1 abc123`

## Show what files have changed since commit
`git diff --name-only master {commit}`

## Show what files have changed since commit for specific folder
`git diff --name-only master {commit} {folder}`

## Remove untracked files
`git clean -n` then `git clean -f`

# LINKS

https://github.com/git-tips/tips

https://stackoverflow.com/questions/7251477/what-are-the-differences-between-double-dot-and-triple-dot-in-git-dif


