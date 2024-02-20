# QA472-Draft

Drafting documentation for the QA472

## View documentation

Docs are being hosted (for now) at [https://excitonlabs.github.io/QA472-Draft](https://excitonlabs.github.io/QA472-Draft).

## Install mkdocs for Windows

**It is not necessary for users to follow these steps. This short guide is for internal use.**

The installation process is quite straightforward and well documented here https://www.mkdocs.org/user-guide/installation/

Once Python is installed, install mkdocs using Python's package manager pip,

    pip install mkdocs
    pip install mkdocs-material
    
These two lines get mkdocs and then material theme we will be using.

## Editing the documentation locally

Go to GitHub and clone the repository to you local disk, change directory in the command prompt to the root of the repository.

For example,

    cd "X:\QuantAsylum\QA472"
    
Start the hot-reloading server by typing

    python -m mkdocs serve
    
Open a browser at http://localhost:8000, you should see the documentation webpage running locally on you PC. When you save a file change should appear instantly. Sometimes the process crashes and hot-reloading breaks. This normally occurs when editing the mkdocs.ymk configuration files rather than content. If that occurs simply kill the server and reload it.

## Pushing changes to production

After editing the markdown files verify locally the changes are correct.

Make a commit to the master branch using Git.

Ask git for the status this should highlight any edited files

    git status
    
Add new files and those that have been edited,

    git add edited_file_1.md
    git add edited_file_2.md
    git add new_file_1.md

Now make a commit,

    git commit -m "Updated section in preamp1"
    
Push those changes to the master branch

    git push
    
We have update the documentation markdown files but we have not yet updated the production website.

Next type,

    python -m mkdocs gh-deploy

mkdocs will handle all the deployment for us, in around 60s or less  the new changes will be live (you might need to clear your browser's cache to view them).