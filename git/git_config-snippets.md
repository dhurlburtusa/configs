# git Config Snippets


## Aliases

```sh
git config --global alias.cm 'commit'
git config --global alias.co 'checkout'
git config --global alias.st 'status'
```

Or add the following to the global git config:

```
[alias]
	cm = commit
	co = checkout
	st = status
```


## User Information

```sh
git config --global user.email 'example@user.noreply.github.com'
git config --global user.name 'Your Name'
```

Or add the following to the global git config:

```
[user]
	email = example@user.noreply.github.com
	name = Your Name
```
