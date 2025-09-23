# Practical GitHub for Researchers and Students of Data Science

Why GitHub?

Repository (more commonly called a "repo") and version control tool 

## Setup

Installation of Git (the underlying ENTER)
Create GitHub account 

## GitHub Loop

It helps to think of the process of working with Git and GitHub as a cycle: you begin by making a copy of the project, then move through a series of steps whenever you write code. 

First clone the code onto you machine. You can clone 

Using SSH: 

```
git@github.com:EmoryHPC/practical-data-science.git
```

or using HTTP: 

```
https://github.com/EmoryHPC/practical-data-science.git
```

Both work, except that GitHub only allows transaction using SSH. 

If you have downloaded the repository using SSH, you can now 

![GitHub Loop Image](https://raw.githubusercontent.com/EmoryHPC/practical-data-science/main/github/images/github_loop.png)

Working with GitHub mirrors the rhythm of a day:

* Start of the day → Always pull from the repository before you begin. This ensures you're working with the most up-to-date code.
* End of the day → Always push your code when you finish. This saves your progress and makes it available for others to use.

```
cd practical-data-science
```


```
git pull origin main
```

```
git add .
```

or be more selective:

```
git add file.py file.R /folder/file.sh
```

```
git commit -m "Meaningful commit message here"
```


```
git push origin main
```

branches 

```
# Sync
git pull origin main  

# Branch
git checkout -b my-feature-branch  

# Work
git add .
git commit -m "Add new analysis script for X"  

# Push
git push origin my-feature-branch  
```


SHOW COMMANDS FOR PULL STAGE COMMIT PUSH 
PUT TERMINAL IMAGES 


## Version Control

Our work is always provisional and revisable. This is why we use version control. 

## Ignoring Files

A file saved as `.gitignore`. Note that the period before the name turns this into a hidden file. Your computer can still read it, but you cannot. 

This is an example of a `.gitignore`. The `*` means "any filename." For example, `*.log` tells Git to ignore every file that ends with `.log`, no matter what comes before it.

```
# Ignore Python cache and compiled files
__pycache__/
*.py

# Ignore virtual environments
venv/
.env/

# Ignore system files
.DS_Store

# Ignore logs and temp files
*.log
*.tmp

# Ignore whole directories
data/
```

describe .gitignore_global

## Creativity and Room to Err

You might create draft notes, experimental code, or half-finished ideas as you work. By adding these to a `.gitignore`, they will stay on your computer but won't be shared with others. This way, your creative "spaghetti code" can stay part of your creative process without turning into a stressy spaghetti ball for someone else.

```
# Ignore specific files
count_test.py
test_scatter_plot.py
```

Full: 


```
# Ignore Python cache and compiled files
__pycache__/
*.py

# Ignore virtual environments
venv/
.env/

# Ignore system files
.DS_Store

# Ignore logs and temp files
*.log
*.tmp

# Ignore whole directories
data/

# Ignore specific files
count_test.py
test_scatter_plot.py
```


## GitHub Issues

A GitHub Issue documents and tracks work to be done, including tasks or bugs. Because each issue keeps a history of conversation, it doubles as a record of why certain choices were made 

We can enhance them with labels 


One issue with multiple problems. The advantages are that this approach keeps related tasks grouped together in a single record. It is easier to see a big picture of what needs to be done, and there are fewer issues to write and manage, which can save time. The disadvantages are that it is harder to track progress if some tasks are completed and not all (I cannot close issues along the way to track progress), discussions about different subtasks can get tangled together, and it is difficult to assign subtasks to different people if responsibilities are split. 

![GitHub Issue 1](https://github.com/EmoryHPC/practical-data-science/blob/main/github/images/github_issue_1.png?raw=true)

We can write GitHub issues in such a way that there is one issue per problem. 

Pros:

Each issue is tightly scoped, so it’s easy to close when finished.

Easier to assign to different contributors.

Provides a clear historical record of each piece of work.

Works better with automation (e.g., linking issues to pull requests, tracking metrics).

Cons:

Can feel repetitive if the issues are nearly identical.

May create a flood of issues that seem overwhelming without good labeling.
 

![GitHub Issue 2](https://github.com/EmoryHPC/practical-data-science/blob/main/github/images/github_issue_2.png?raw=true)





