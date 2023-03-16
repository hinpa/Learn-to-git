# Learn-to-git
## brief git commands overview
"git clone" clones the repo from cloud to your local machine
"git status" will show you changed files and files that are staged for commit
"git commit" will commit changes in your local git repo. First -m is for the commit name (it is advised to write names as clear as possible). Second -m is for description of that commit.
"git add" will make file to be staged for commit
"git restore --staged *file_name*" will make file not to be staged for commit
you can also write '.' instead of *file_name*. It will stage all changed and added files to commit
"git restore *file_name*" will restore the unchanged version of the file
"git push *repo*" will push your local git into cloud
before you can commit any changes, you have to identify yourself
"git config --global user.email *email*"
"git config --global user.name *name*"
before you can push changes into github you have to generate an ssh key, load public version on github
and add this ssh key to your ssh-agent
now I will use git push *repo* with the branch to commit to and keyword 'origin'
## Setting up a local git repo and pushing it to Github
To create a local git repo you cd into folder and write there git init.
As usual, you go through process of adding new files and commiting them.
Then you'll need to push it to github somehow.
You can do that either by creating a new repo on the site itself or by using a 'gh'.
'gh' is a Github CLI application for managing github repositories.
After you've created a repo, you need to connect to that repo.
'git remote add *name* *link_to_repo*' will connect you to that repo.
Usually you will give origin to the name if it's the first link.
To remove the connection, you need to write 'git remote remove *name*'
You've added the remote connection.
To push to the github repo, you'd write 'git push -u origin *branch_name*'
'-u' specifies that we'll upload to origin by default.
You've pushed your commit to github! Congrats! (my example is Learn-how-to-git-partII)
## Branching. Merging. Conflicts.
So, you'd also want to create branches. They provide a good version control.
For example, you may want to write code implementing a new feature in your program.
We all know that it takes time to wrtie a good clean and safe code. Of course, you wouldn't want to mess up your main branch. So you need a different space to write that code in.
That's why you'd create "feature" branch where you do all this work on your new feature.
All commits to the branch are local.
To create a new branch, you write 'git checkout -b *branch_name*' (it will also move you to that branch).
All files from the branch you're creating from will be also in the new branch.
To move between branches you write 'git checkout *branch_name*'.
To see all branches you have you write 'git branch'
So, imagine you've done all the work and now you want to merge, let's say, 'feature' to 'main'.
'git merge *branch_name*' will merge *branch_name* into the branch you're currently in.
If you want to merge it in github, you will need to pull a request (PR for short). The team of devs will review your code, comment some lines and the code will just go through a check.
If everything is fine, the PR will be merged.
When branching, there may be a conflict. It happens when the same parts of files are changed.
In this case, you will see something like 'merge conflict'.
In the file, where there is conflict, you will see '<<<<<<<<<<<<', '>>>>>>>>>>' and '========='.
The '=======' will separate the change from the current branch and incoming branch.
The '<<<<<<<' is the current branch change.
The '>>>>>>>>>>' is the incoming change.
You or the team will just need to change the code so that it satisfies you or a team of devs.
When you've done the change, you do a commit: 'git commit -am 
