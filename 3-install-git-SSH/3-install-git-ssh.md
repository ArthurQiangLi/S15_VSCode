# Install Git and Config SSH

## 1. Installing `git`
- For Windows system, simply download it and install it. 

![windows git](image.png)

- For `Linux` system
install git by typing in :  `sudo apt-get install git`


## 2. Configuring SSH
>Official link: https://docs.github.com/en/authentication/connecting-to-github-with-ssh

1. Check what's in your .ssh directory, its same for win and linux
```
ls -al ~/.ssh
 
ls: cannot access '/c/Users/xxxx/.ssh': No such file or directory
```
2. Generate your github account's key locally, try to rename it so you know what is it used for, eg. `git_abc_ssh`.
```
ssh-keygen -t ed25519 -C "abc@gmail.com"	

//It may throw the two generated files to desktop in Win10.
```
>[!note] [I recommended you use the passphrase to add another password when access the account locally]
	
3. See the contents of the public key file, copy all and goto your github account.
```
cat ~/.ssh/id_ed25519_arthur.pub
```
	

4. On you github account page, goto `Setting->SSh Keys->New SSH key`, add it and it's done.

5. Log in your github account and config your account for current working environment.
```
git config --global user.email "you@example.com"
git config --global user.name "your_name"  //the name will be used to track your contributions to the repo.
```
	
5. Test the connection:
```
ssh -T git@github.com
```
>[!note] In your vscode.
    You still need to log in your github account when cloning from a private(not public) repo. 
    Also, you sitll need to set your email and user name when pushing to a repo. <br>


