# Installing Homebrew for MacOS 2020 M1 Chip Monterrey 12.0.1

1. Go to homebrew [site](https://brew.sh/) and run the command below:

```
Installs homebrew into /opt folder
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2. Run shellenv script that comes with homebrew to set $PATH be: '/opt/homebrew/bin:/opt/homebrew/sbin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin'

```
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/kennethkorcal/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

