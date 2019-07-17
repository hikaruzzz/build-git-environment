# How to build github environment, and push your first repository.
## 1 Create a new repository in github(with no README.md)
## 2 Create Git SSH Key  
* download Git and istall
* set git user.name, user.email  
run in git bash `git config --global user.name your_github_name`  
run in git bash `git config --global user.email your_github_email`  
* create key  
run in git bash `ssh-keygen -t rsa -C "your_github_email"`   
use the 3 enter bottom instead keyword(use empty keyword), then you will get 2 file(id_rsa & id_rsa.pub)(C:\User\.ssh\)  
caution:  
`if /id_rsa already exists.`  
`Overwrite (y/n)? yes`  
* add key to ssh  
run in git bash `ssh-agent bash`  
run in git bash `ssh-add ~/.ssh/id_rsa`  
* add public key to github  
[go to github setting]("https://github.com/settings/keys")  
open the file id_rsa_pub,and copy the message to SSH keys，the title could be custom.
## 3 Repository create
* test the connection
run `ssh -T git@github.com`
* clone git to local folder
go to local folder need to be saved repository  
and right-click, click `Git Bash`  
run `git clone http://github.com/xxxxxxxxxxxxxxxx/xxx.git`
* initial new repository   
go to clone git floder    
run `git init`   
* create README.md
run `touch README.md`
move some file into that floder. and   
run `git commit -m "my first commit"`   
* remote add origin  
run `git remote add origin http://github.com/xxxxxxx/xxxx.git`  
run `git push -u origin master`   

## 4 How to use git daily
* go to clone git folder
* run `Git Bash` in that folder(right-click)
* change file
* run `git add .`
* run `git commit -m "test commit"`
* run `git push -u origin master`

* to add new repository  
run `git remote add origin http://github.com/hikaruzzz/myRepository/xxx.git`
