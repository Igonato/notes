# GitHub CLI

## Creating a New Repo

General `gh repo` usage:

```bash
# Create a repository interactively
gh repo create

# Create a new remote repository and clone it locally
gh repo create my-project --public --clone

# Create a remote repository from the current directory
gh repo create my-project --private --source=. --remote=upstream
```

Useful aliases:

```bash
# Create a remote repository from the current directory using the
# current directory name as the repo name
alias ghcr='\
    git init; \
    gh repo create $(basename "$PWD") --source=. --remote=origin'
alias ghcrp='ghcr --private'
alias ghcro='ghcr --public'  # o for Open Source

# Command that was used to create this repo
ghcro -d "Personal software development notes: snippets, shell commands, etc..."
```