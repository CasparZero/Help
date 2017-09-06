Generate SSH Key:

1.Checking for existing SSH keys:
$ls -al ~/.ssh

2.Genreate new ssh key:
$ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

3.Start ssh-agent in the background:
$eval "$(ssh-agent -s)"

4.Configuration:
$vi .ssh/config
Host *
 AddKeysToAgent yes
 UseKeychain yes
 IdentityFile ~/.ssh/id_rsa

5. Add your SSH private key to ssh-agent and stor your passphrase in the keychain:
$ ssh-add -K ~/.ssh/id_rsa

6.Copy the SSH key to your clipboard.
$ pbcopy < ~/.ssh/id_rsa.pub

7.Verify SSH.
$ssh -T git@github.com 

8.Configuration user name and email:
$ git config --global user.name "your name"  
$ git config --global user.email "your_email@youremail.com"  

9. Add local git respository to remote.
$git remote add origin git@github.com:yourName/yourRepo.git

10: Git command:
$git init
$git add . 
$git status
$git commit -m "your comments"
$git push origin master
$git branch
$git remote
$git clone

11. Git create remote respository:
$curl -u 'username' https://api.github.com/user/repos -d '{"name":"RepoName"}'