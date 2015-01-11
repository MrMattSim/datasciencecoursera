## SSH setup for automatic github authentication

####Create config file and repo (or change repo settings)
 
```sh
$ touch ~/.ssh/config
$ vi ~/.ssh/config
```

```text
Host github.com-MrMattSim 
	HostName github.com
	User git #this must always be "git"
	IdentityFile ~/.ssh/id_rsa #or whatere was used for
```
* Host is an arbitrary name, used below to refer to this config entry.
* There can be multiple config entries. 
* User must always be 'git'. 
* IdentityFile is whatever was used during ssh setup. Each config can use a  different key, or not.

When creating a local repo, the following command will instruct git to use the config settings:
```sh
$ git clone git@github.com-MrMattSim:MrMattSim/datasciencecoursera.git #[local folder name]
$ git config user.name "MrMattSim"
$ git config user.email "MrMattSim@example.com"
```
If the local repo already exists, then change the remote origin settings, like so:
```sh
$ git remote set-url origin git@github.com-MrMattSim:MrMattSim/datasciencecoursera.git
```
####Check and confirm remote origin config:
```sh
$ git remote -v
origin	git@github.com-MrMattSim:MrMattSim/datasciencecoursera.git (fetch)
origin	git@github.com-MrMattSim:MrMattSim/datasciencecoursera.git (push)
$
```
####One-line commit
Now, when you push from the current repo, you won't need to authenticate each time. <br>
Just, `git commit -a -m 'null' && git push`

[![matt](https://copy.com/WiKwXBzvW7UehxO1 "matt")](http://bymattsim.weebly.com)

---
######Sources & Additional Info:
- [Automatically use correct SSH key for remote git repo (knitatoms.net)](http://knitatoms.net/2013/10/automatically-use-correct-ssh-key-for-remote-git-repo/)
- [Generating SSH keys (help.github.com)](https://help.github.com/articles/generating-ssh-keys/)
