# useful-commands

To remove a file and the history of it from a Git repository:
`git filter-branch --tree-filter 'rm -f <path_to_file>' HEAD`
followed by
`git push origin --force --all`

But remember that any subsequent commits will once again check in the .env file to master when you deploy to Heroku so you will have to run these commands again. Additionally, in the README I should state that users need to compose a .env file to run the code on their own.
