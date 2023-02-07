# Create a Git Repo, add it as remote

In order to be able to "save to git" a local folder, Git must be initialised inside so changes could be tracked, and linked to a remote repository as the destination.

## Quick Example

- Head over to [Github](https://github.com), log-in, click on your avatar image [top right] and chose `Your Repositories`.

- Obviously click on the [New] button, give your repo a name and check the 'Private' option.

From the empty new repo, `< > Code` page copy the remote line

```bash
git remote add origin https://github.com/username/reponame.git
```

- On your machine, go inside your folder and initialise Git

```bash
cd /home/username/Documents/calepin
git init  
```
- Paste the copied line from Github

- You can check any time the remotes with

```bash
git remote -v
```
It will sho the remote's name and linked GitRepo

- First Push. 

```bash
git add . 
git commit -m "FirstCommit"
git push --set-upstream origin master
```
For the next times, `git push` on the last line will be enough.
It's more or less the same pattern with Gitlabs or BitBucket



## RTFM

[Docs at git-scm.com](https://git-scm.com/doc)
[Same, but external links](https://git-scm.com/doc/ext)
