# useful-commands

## 1. Keeping sensitive files off of Git

To remove a file and the history of it from a Git repository:
```
git filter-branch --tree-filter 'rm -f <path_to_file>' HEAD
```
followed by
```
git push origin --force --all
```

Remember in the case of `.env` files that any subsequent commits will once again check in the file to master when you deploy to Heroku. Then the above commands will have to be run again. Additionally, in the `README` for such a repo I should state that users need to compose a `.env` file with certain variables if they would like to run the code on their own.
