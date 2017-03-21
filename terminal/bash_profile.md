# Editing your ~/.bashrc (non-login shells) or ~/.bash_profile (login shells)

## Bash Script Example
```
## PATH DIRECTORY
# Some Program
export PATH="/usr/local/some_program/bin:$PATH"

# MySQL
export PATH="/usr/local/mysql/bin:$PATH"


## ALIASES
# Some Alias
alias alias_name = "commands"

# Jupyter Notebook
alias jn="jupyter notebook &"
```

## Check PATH
```
$ echo $PATH
```

## Check Aliases
```
$ alias
```
