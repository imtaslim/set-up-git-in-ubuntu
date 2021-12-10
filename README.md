# set-up-git-in-ubuntu
The Git feature that really makes it stand apart from nearly every other SCM out there is its branching model.

Git allows and encourages you to have multiple local branches that can be entirely independent of each other. The creation, merging, and deletion of those lines of development takes seconds.

So let's set up git....

# First update ubuntu
~~~
sudo apt-get update
~~~
or
~~~
sudo apt update
~~~

# Git Install
~~~
sudo apt install git
~~~

# Check Version
~~~
git --version
~~~

# Genarate SSH key
~~~
ssh-keygen -t rsa -b 4096 -C "your email"
~~~
now go to <strong>home/.ssh</strong> and open the <strong>id_rsa.pub</strong> and copy that whole text and create a SSH key with that text

# Configure git
~~~
git config --global user.email "your mail"
~~~
then
~~~
git config --global user.name "your username"
~~~

# Clone a repository
Copy the ssh clone link of the repository and run
~~~
git clone <ssh clone link>
~~~

# Staging repository
Stage All
~~~
git add --all
~~~
or
~~~
git add -A
~~~
Stage All From Specific Folder
~~~
git add .
~~~
Stage All Without Deleted File
~~~
git add *
~~~

# Now Commit
~~~
git commit -m "<commit messege>"
~~~

# git push
first push
~~~
git push -u origin <branch name>
~~~
otherwise
~~~
git push origin <branch name>
~~~
forcefully
~~~
git push origin <branch name> --force
~~~

# Git pull
~~~
git pull <branch name>
~~~

# Using branch
~~~
git branch
~~~
List all of the branches in your repository. This is synonymous with git branch --list.

~~~
git branch <branch>
~~~
Create a new branch called ＜branch＞. This does not check out the new branch.

~~~
git branch -d <branch>
~~~
Delete the specified branch. This is a “safe” operation in that Git prevents you from deleting the branch if it has unmerged changes.

~~~
git branch -D <branch>
~~~
Force delete the specified branch, even if it has unmerged changes. This is the command to use if you want to permanently throw away all of the commits associated with a particular line of development.

~~~
git branch -m <branch>
~~~
Rename the current branch to ＜branch＞.

~~~
git branch -a
~~~
List all remote branches.
