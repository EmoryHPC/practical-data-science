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

## Version Control

Our work is always provisional and revisable. This is why we use version control. 

## `.gitignore`

A file saved as `.gitignore`. Note that the period before the name turns this into a hidden file. Your computer can still read it, but you cannot. 

This is an example of a `.gitignore`. The `*` means "any filename." For example, `*.log` tells Git to ignore every file that ends with `.log`, no matter what comes before it.

```
# Ignore Python cache and compiled files
__pycache__/
*.py[cod]

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

## Creativity and Room to Err

