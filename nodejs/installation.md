# Installation

* Install NVM with the [official installer](https://github.com/nvm-sh/nvm)

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | zsh
```

* Or use [homebrew](https://www.youtube.com/watch?v=AEuI0PBvgfM)

```
brew install nvm
```

You should create NVM's working directory if it doesn't exist:

```
  mkdir ~/.nvm
```

Add the following to ~/.zshrc or your desired shell
configuration file:

```
  export NVM_DIR="$HOME/.nvm"
  [ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && \. "/opt/homebrew/opt/nvm/nvm.sh"  # This loads nvm
  [ -s "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion
```

You can set `$NVM_DIR` to any location, but leaving it unchanged from `/opt/homebrew/opt/nvm` will destroy any nvm-installed Node installations upon upgrade/reinstall.

Restart the terminal and run `nvm help` to check that nvm exist then you could the latest LTS node version:
```
nvm install --lts
nvm use --lts
```

# Misc

1. How NPM can [break the internet](https://www.theregister.com/2016/03/23/npm_left_pad_chaos/)

