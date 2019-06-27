# How To Delete Multiple Local Branches in Git

From https://medium.com/@rajsek/deleting-multiple-branches-in-git-e07be9f5073c

Check what will be deleted first:
`git branch | grep "<pattern>" `

Delete (with force - be careful!)
`git branch | grep "<pattern>" | xargs git branch -D`
