# Learn-to-git
"git clone" clones the repo from cloud to your local machine
"git status" will show you changed files and files that are staged for commit
"git commit" will commit changes in your local git repo
"git add" will make file to be staged for commit
"git restore --staged <file_name>" will make file not to be staged for commit
you can also write '.' instead of <file_name>. It will stage all changed and added files to commit
"git restore <file_name>" will restore the unchanged version of the file
"git push <repo>" will push your local git into cloud
before you can commit any changes, you have to identify yourself
"git config --global user.email <email>"
"git config --global user.name <name>"
before you can push changes into github you have to generate an ssh key, load public version on github
and add this ssh key to your ssh-agent
now I will use git push <repo> with the branch to commit to and keyword 'origin'
## Subheader