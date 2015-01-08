## SSH setup for automatic github authentication

####Create config file

```bash
$touch ~/.ssh/config
$vi ~/.ssh/config
```

	#MrMattSim account
	Host github.com-MrMattSim
	    HostName github.com
	    User git #this must always be "git"
	    IdentityFile ~/.ssh/id_rsa #or whatere was used for


#####Sources & Additional Info:
- [Automatically use correct SSH key for remote git repo (knitatoms.net)](http://knitatoms.net/2013/10/automatically-use-correct-ssh-key-for-remote-git-repo/) 
- [Generating SSH keys (help.github.com)](https://help.github.com/articles/generating-ssh-keys/) 
