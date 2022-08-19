# [Brew bundles](https://github.com/Homebrew/homebrew-bundle)

Uses / generates a Brewfile that records all installed casks / formulae so that it could be ported over to other machines.

```
brew bundle dump --describe
cat Brewfile
```

You could run this command todo a software update + clean brew update
```
sudo softwareupdate -ia -verbose && brew bundle -v && brew cleanup && brew doctor -v
```


# Resources

1. [LINK](https://www.youtube.com/watch?v=-VP2NVv3LHg)

