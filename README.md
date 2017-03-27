# Testing Blog Repo

Just testing to create a repository with settings and content for a static blog using Pelican, and publishing on Github Pages.

Steps to create new post:

1. Create the markdown file in the content folder (sub-folders for archiving should be automatically set, per Pelican config file settings).

2. In the terminal, execute:

        $ pelican content -o output -s pelicanconf.py
        $ ghp-import output


    The `ghp-import output` command updates the local gh-pages branch with the content of the output directory (creating the branch if it doesn't already exist).


3. Push the changes to the remote gh-pages branch:

        $ git push origin gh-pages  

   
4. To serve the page at <http://localhost:8000:>

        $ cd output
        $ python -m http.server 8000 # For Python 3
