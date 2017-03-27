# blog-test
Testing Blog Repo

Just testing to create a repository with settings and content for a static blog using Pelican, and published on Github Pages.

Steps to create new post:

1. Create the markdown file in the content folder (sub-folders for archiving should be automatically set, per Pelican config file settings)

2. In the terminal, execute:

        pelican content -o output -s pelicanconf.py
        ghp-import output


3. Check git status. Add and commit the markdown file to the master branch. Note: it seems this step may not be required as it is possibly handled by ghp-import? See [here](https://github.com/getpelican/pelican/blob/master/docs/tips.rst#publishing-to-github) 


4. Finally, push the changes to the gh-pages branch from the local repo:

        git push origin gh-pages  

   
To serve the page at <http://localhost:8000:>

    cd output
    python -m http.server 8000 # For Python 3


