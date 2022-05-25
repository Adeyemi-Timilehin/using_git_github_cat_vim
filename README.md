# using_git_gitlab_cat_vim

### cat is used to read a file;usage cat file_name
### vi is used to modify a file and save the file using :wq at the end to save :q! to navigate out without saving
 git commit -am "message" add file and commit
 git push origin master
git reset --hard for cleaning up
git push origin master --force< dangerous to use>

git ls-tree --full-tree -r HEAD to look at the repository file


### Best practices
##### commit early,commit often
##### pull frequently from upstream (git pull origin master) <So as to reduce merge/ conflicts>
#### use gitignore
##### samples-> .project, .settings bin/ *.class, **bin( subdir)


Line -Ending

core.autocrlf
git init
git config core.autocrlf input
git add .

git commit -m "message"


###Forcing git to pull out o the repository
git checkout -b 'other'
rm sample.java
git add .
git commit -m 'message'
git checkout master 

Branch Naming convention
$git branch -b bug/123/menu-issue
$git branch -b feat/123/new-email-feature
Type of Change/Change Number/Short Name

Best Practice for writing Commit Message 
use text editor
git config --global core.editor "/usr/bin/gedit"
git commit without the -m flag will cause editor to open
git config commit.template


Team member
Maintainer->perform commits * integrates pull requests * INherit contributor permissions
Contributor-> clone repositories * Lack commit privileges * Submit pull requests

sudo apt-get update
sudo apt-get install -y curl openssh-server ca-certificates
curl -sS https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh | sudo bash
sudo EXTERNAL_URL=http://localhost:80/ apt-get install gitlab-ce

Step by step:

sudo -e /etc/gitlab/gitlab.rb
Change external_url from yourdomain.com to yourdomain.com:9999
9999 -> Port you want it to run
sudo gitlab-ctl reconfigure
Share
Improve this answer
Follow


