
## Installing `git`
### 1. For `Linux` system
install git by:
```.bash
sudo apt-get install git
```


## Configuring SSH
1. Check what's in your .ssh directory
```
ls -al ~/.ssh
```
2. Generate your github account's key locally, try to rename it so you know what is it used for.
```
ssh-keygen -t ed25519 -C "arthur@gmail.com"	

```
>[!note] [I recommended you use the passphrase to add another password when access the account locally]
	
3. See the contents of the public key file, copy all and goto your github account.
```
cat ~/.ssh/id_ed25519_arthur.pub
```
	

4. On you github account page, goto `Setting->SSh Keys->New SSH key`, add it and it's done.
	
5. Test the connection:
```
ssh -T git@github.com
```
>[!note] In your vscode.
    You still need to log in your github account when cloning from a private(not public) repo. 
    Also, you sitll need to set your email and user name when pushing to a repo. <br>

```
git config --global user.email "you@example.com"
git config --global user.name "your_name"  //the name will be used to track your contributions to the repo.
```

