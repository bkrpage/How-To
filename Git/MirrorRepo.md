# Mirroring a Git Repo

How to mirror a git repo to a new git service, as described here: https://stackoverflow.com/a/43077618

Clone / mirror existing repo:
``` 
	git clone --mirror https://github.com/account/repo.git cloned-repo
	cd cloned-repo
	git push --mirror {URL of new (empty) repo}
```

Now, suppose you want to keep the source and destination repos in sync for a period of time. For example, there's still activity within the current remote repo that you want to bring over to the new/replacement repo.

```
	git clone -o old https://github.com/account/repo.git my-repo
	cd my-repo
	git remote add new {URL of new repo}
```

To pull down the latest updates (assuming you have no local changes):
```
	git checkout {branch(es) of interest}
	git pull old
	git push --all new
```
