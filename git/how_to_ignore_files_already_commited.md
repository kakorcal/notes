# How to .gitignore files when they were already commited

1. Update .gitignore with the new changes and commit

2. Remove all files from git cache

```
git rm -r --cached .
```

3. Add all files back to staging and commit them

```
git add -A
git commit -m 'updated ignored files'
```

Note that you'll still be compromised given that someone could've already cloned the project with the content you needed ignored. [LINK](https://egghead.io/lessons/git-git-ignore-a-file-that-has-already-been-committed-and-pushed)
 

