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

You might create draft notes, experimental code, or half-finished ideas as you work. By adding these to a `.gitignore`, they will stay on your computer but won't be shared with others. This way, your creative "spaghetti code" can stay part of your creative process without turning into a stressy spaghetti ball for someone else.

```
# Ignore Python cache and compiled files
__pycache__/
*.py[cod]

# Ignore specific files
count_test.py
test_scatter_plot.py
```

## GitHub Issues


We can write GitHub issues in such a way that 

![GitHub Issue 1](https://github.com/EmoryHPC/practical-data-science/blob/main/github/images/github_issue_1.png?raw=true)



![GitHub Issue 2](https://github.com/EmoryHPC/practical-data-science/blob/main/github/images/github_issue_2.png?raw=true)


flowchart LR
  %% Style
  classDef step fill:#eef,stroke:#88a,stroke-width:1px,rx:8,ry:8
  classDef store fill:#efe,stroke:#6a6,stroke-width:1px,rx:8,ry:8

  %% Main steps
  A[Scrape Wikipedia]:::step -->|raw .txt\n/data/raw/*.txt| B[LLM Translation]:::step
  B -->|translated .txt\n/data/translated/*.txt| C[Regex Date Extraction]:::step
  C -->|dates.csv\n/data/dates/dates.csv| D[(Dataset Store)]:::store

  %% Scraping lane
  subgraph S[Scraping]
    A --> S1[HTTP fetch + throttle]
    S1 --> S2[Parse HTML → plain text]
    S2 --> S3[Write files + manifest.json]
  end

  %% Translation lane
  subgraph T[Translate]
    B --> T1[Chunking (3–4k tokens, overlap)]
    T1 --> T2[Prompt: literal, preserve numerals]
    T2 --> T3[LLM API + metadata (model, version)]
  end

  %% Extraction lane
  subgraph E[Extract]
    C --> E1[Regex with prefix guards\n(e.g., No. 1999, § 2001, Vol. 3)]
    E1 --> E2[Regex with suffix guards\n(e.g., 2000 kg, 30 mph, 60 Hz)]
    E2 --> E3[Normalize to ISO dates\n+ source offsets]
  end






