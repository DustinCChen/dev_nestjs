# dev_nestjs
## bug fixed
* Q:PS D:\workdir\nodedev\github\dev_nestjs> git add .
error: 'lesson1/backend/' does not have a commit checked out
fatal: adding files failed
* A:create `lesson1\backend` directory in remote repo,and git clone it,then repeat the push process. 
# git operation
```sh
# Initial config
git config --global user.name "dustin.chen"
git config --global user.email "648023262@qq.com"
git config --global color.ui auto

# set SSH Key
ssh-keygen -t rsa -C "648023262@qq.com"
cat ~/.ssh/id_rsa.pub # add SSH Key

# push to remote repo
git clone https://github.com/DustinCChen/dev_nestjs.git
cd dev_nestjs/
git add .
git commit -m "my first commit"
git push -u origin main
# sync remote repo update to local repo
git remote add origin https://github.com/DustinCChen/dev_nestjs.git
git pull origin main
git status
git checkout -- .

```