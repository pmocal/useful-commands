## 1. Keeping sensitive files off of Git

In the case of a `.env` file you will want to make a copy of this file to put back in your local repo before doing the steps below.

To remove a file and the history of it from a Git repository:

```
git filter-branch --tree-filter 'rm -f <path_to_file>' HEAD
```
followed by
```
git push origin --force --all
```

Remember in the case of `.env` files you should deploy to Heroku, temporarily copy the file elsewhere, do the git commands above, then restore the file without any further git checkins. Note that any subsequent commits will once again check in the file to master when you deploy to Heroku. Then the above commands will have to be run again. Additionally, in the `README` for such a repo I should state that users need to compose a `.env` file with certain variables if they would like to run the code on their own.

## 2. Markdown syntax

https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#code


## 3. See the differences between 2 folders

`diff -rq jewelery-co-server jewelery-co-server-old`

## 4. Deploy Vue CLI app on Heroku

https://gist.github.com/hone/24b06869b4c1eca701f9
