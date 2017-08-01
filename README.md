# Basic_git_svn_workspace

These are my starter templates for .bashrc and .gitconfig that I find pretty useful for environments in which you often use git and svn.
Tweak as needed for your project, host or environment.

The prompt will have the format:
user@server [(svn|git details) [*]] dirpath $

- 'user' in green or red color depending on whether the username is root.
- 'server' in blue color.
- 'git details' = (git:reponame:branchname[*]) in purple color. There is an asterisk if there are uncommited changes.
- 'svn details' = (svn:reponame [*]) = in purple color. There is an asterisk if there are uncommited changes.
- dirpath = in blue color (only show the last 3 dirs).
- Trailing $ = in green or red color depending on exit code of previous command. 




When in a normal directory, your prompt would look like this:

```
mujihina@kotatsu /var/log $
```


When in a directory with a git repository, your prompt would look like this:
```
mujihina@kotatsu (git:databasesweeper:master) ~/repos/dbsweeper $ echo 'test' >> file
mujihina@kotatsu (git:databasesweeper:master *) ~/repos/dbsweeper $
```


When in a directory with an svn repository, your prompt would look like this:
```
mujihina@kotatsu (svn:hooksrepo) ~/repos/svnhooks $ echo 'test' >> file
mujihina@kotatsu (svn:hooksrepo *) ~/repos/svnhooks $
```

## git aliases
There are a few aliases I find handy:
- git lg
- git last
- git st
- a few more

They just provide some pretty formatting and/or shortcuts for us lazy typers.

## Notes
- Sure, you could include even more git/svn details like how many commits ahead/behind you are, svn rev numbersetc. But I find it's not worth the performance hit after every single command, or the extra clutter. Just seeing a '*' usually tells me most of what I need, but tweak as needed.
- You could, if you want to, add a check to change the color of the server depending on whether it is a production/staging environment, infrastructure,how critical it is, etc.
