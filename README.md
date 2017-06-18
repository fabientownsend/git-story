# Git Story
List of the command covered
``` cmd
git add . // will staged all the files
git add -e // will staged all previously staged files
git add -p // will let you select what you want to stage
git commit -m "" // write the message of your commit
git commit -v // let you the diff and write your commit
git commit --amend // merge the last add to previous commit
git reset HEAD~ // remove last commit
git reset // unstage files
```

## Commit guideline
1. Commit is composed of a subject and body separated by a blank line
2. Short subject (under 50 characters)
3. Capitalise subject dn not full stop
4. Subject answer "what"
5. Body answer what/whym not how, the code does

## Initialisation
Every git sotry start with `git init`

The current repository is empty, let's create a new file:

``` cmd
$touch README.md
```

## Basic add & Commit
Let's start with a pretty simple command that you must already use.

``` cmd
$git add .
$git commit -m "Initialisation of the project"
```

Well, we commit an empty file it's not really useful right? Let's fix that.

``` cmd
$echo "#I'm Learning Git!" > README.md
$git status
$git add .
// here we want to add it to our previous commit
$git commit --amend
```

## Add & Commit Granularity
Let's add more information.

``` cmd
$echo "I'm learning git and it's really great" << README.md // here we add a new line
$touch main.rb
$echo "You can run the program with Ruby with `ruby main.rb`" // here we add a new line
$git add -e // Here we add only staged file
$git commit -v
// the you realise you commit more line that you want
$git reset HEAD~
// let's create two distinct commit
$git add -p // for the initial commit
$git commit -v
$git add -p // for the code commit
$git commit -v
```

# Clean Your Commit?
``` cmd
$echo "puts "Hello world!" >> main.rb
$git add .
$git commit -m "Add message to software"
git rebase -i HEAD~3 // Here we can refactor our commit
```
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
