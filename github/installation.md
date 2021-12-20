# Github ssh key setup

1. [Create ssh key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh) in ~/.ssh

2. [Save in keychain](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#adding-your-ssh-key-to-the-ssh-agent) if you don't want to enter a passphrase on every push

3. [Might need to do](https://gist.github.com/xirixiz/b6b0c6f4917ce17a90e00f9b60566278) `git remote set-url origin git@github.com:username/your-repo.git` if github still prompts to enter username and password. Most likely this is due to using the [HTTPS link instead of SSH](https://stackoverflow.com/questions/6565357/git-push-requires-username-and-password) 
