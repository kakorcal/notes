# Trimming whitespace

[link](https://www.baeldung.com/linux/trim-whitespace-bash-variable)

# Using xargs

[link](https://www.baeldung.com/linux/xargs)

# Using history

Find specific row of history, grab first entry, trim leading space with xargs (should try trimming \n on the end too) then copy command
```
history 1 | grep web | awk '/4755/{$1=""; print $0}' | head -1 | xargs | pbcopy
```

Print match and pipe to less
```
history 1 | grep web | awk '{$1=""; print $0}' | less
```
