# Learn-to-git
## brief git commands overview
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
## Setting up a local git repo and pushing it to Github
To create a local git repo you cd into folder and write there git init.
As usual, you go through process of adding new files and commiting them.
Then you'll need to push it to github somehow.
You can do that either by creating a new repo on the site itself or by using a 'gh'.
'gh' is a Github CLI application for managing github repositories.
After you've created a repo, you need to connect to that repo.
'git remote add <name> <link_to_repo>' will connect you to that repo.
Usually you will give origin to the name if it's the first link.
To remove the connection, you need to write 'git remote remove <name>'
You've added the remote connection.
To push to the github repo, you'd write 'git push -u origin <branch_name>'
'-u' specifies that we'll upload to origin by default.
You've pushed your commit to github! Congrats! (my example is Learn-how-to-git-partII)