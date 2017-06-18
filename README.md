Every git sotry start with `git init`

1.
vim .git/config


# ADD STUFF
git add .
git add -e
git add -p

# Remove them
git reset
git reset HEAD~

# COMMENT YOU STAGED STUFF
git commit -m ""
git commit
git commit -v
Follow a gide line

# FORGOT SOMETHING?
git commit --amend

# CLEAN YOUR COMMIT?
git rebase -i HEAD~N
N is the number of previous commit you want to work with
Not that you should rebase anything that you pushed, you will create a big mess

# BRANCH
git checkout -b name_branch
git branch

# REMOTE
git branch -a
git push origin master
git push oirigin master:new_feature

git push dev master // origin is just a convention
