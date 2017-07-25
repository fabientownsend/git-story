# Git Story Part II
Lis of the commands covered

## Branch
``` bash
git branch
git branch -a
git branch name_of_branch
git checkout -b name_of_branch
git checkout name_of_branch
git branch -d name_of_branch
git branch -D name_of_branch
```

## Mergin
``` bash
git merge feature
git rebase feature
git rebase master feature
git merge --ff feature
git merge --no-ff feature
```

## Remote
``` bash
git remote add origin htt://url.com
git remote -v
git push origin name_of_branch
git push origin :name_of_branch
git push remote new_branch:master
```

Let's check the current branch:
``` bash
$git branch
$git branch -a
```

We can create a branch
``` bash
$git branch name_of_branch
$git branch
```

As we can se we aren't in this new branch, we need to manually switch on it:
``` bash
$git checkout name_of_branch
$git branch
```

Otherwise you can do
``` bash
$git checkout -b second_branch
$git branch
```

Now you can to delete these branch
``` bash
$git checkout master
$git branch -d name_of_branch
$git branch -D second_branch // force the delete
```

How do we merge our new feature to or master branch?
``` bash
$git checkout -b new_feature
$touch feature.rb
$git add .
$git commit -m "New feature"
$git checkout master
$git merge new_feature
```

As the master can be update when you work on a branch, you may need to update
your branch

``` bash
$git branch second_feature
$echo "print "hello world" > feature.rb
$git add .
$git commit -m "Update feature"
$git checkout second_feature
$git rebase master
```
