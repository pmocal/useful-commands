# useful-commands
just keeping some useful commands here

To remove a file and the history of it from a Git repository:
`git filter-branch --tree-filter 'rm -f <path_to_file>' HEAD`
followed by
`git push origin --force --all`
