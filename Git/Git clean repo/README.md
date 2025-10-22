# Delete Git branch

The Nautilus developers are engaged in active development on one of the project repositories located at `/usr/src/kodekloudrepos/games`. During testing, several test branches were created, and now they require cleanup. Here are the requirements provided to the DevOps team:

On the `Storage server` in Stratos DC, delete a branch named `xfusioncorp_games` from the `/usr/src/kodekloudrepos/games` Git repository.

## 1. Delete a branch named xfusioncorp_games from the /usr/src/kodekloudrepos/games
`cd /usr/src/kodekloudrepos/games`

`git branch`
```console
  master
* xfusioncorp_games
```

`sudo git checkout master`

`sudo git branch -D xfusioncorp_games`
