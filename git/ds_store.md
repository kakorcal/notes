# DS Store file

This file gets created on every directory whenever you use the finder app on Mac to navigate to that directory. This file includes metadata about your machine so it's best to never commit these files into git by adding the following to the .gitignore file:

```
**/.DS_Store
```

As a side note, if you already commited the DS Store file and pushed it to github, you could do the following:

1. Update .gitignore file to ignore DS Store
2. Commit the .gitignore file
3. Do a `git reset --soft` to the commit before you checked in the DS Store file
4. Recommit the changes now this time with .gitignore included
5. `git push -f` to force push the changes. This will remove the old DS Store commit from github.

# Resources

1. [DS Store explanation](https://www.switchingtomac.com/macos/what-is-a-ds_store-file-and-how-to-remove-it/) 
2. [DS Store gist](https://gist.github.com/lohenyumnam/2b127b9c3d1435dc12a33613c44e6308)
3. [git reset --soft](https://stackoverflow.com/questions/448919/how-can-i-remove-a-commit-on-github)
