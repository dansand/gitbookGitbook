# gettingstarted

This is a tutorial on how to create a minimal gitbook with github integration. This workflow will set up a gitbook from an existing github repository, this way the webhooks enabling syncing get automatically created and you can edit your book from the the github or gitbook.com end.


##Step 1: github

Create a github repository...[](https://help.github.com/articles/creating-a-new-repository/)

* When you create a github repository you can choose a customised gitbook `.gitignore` file. 
* Add a license if one of the default options is suitable
* Click `create repository`
* Make sure to add a readme.md file (add readme button)

The repository’s main README.md is going to be the book’s introduction.

##Step 2: gitbook.


##Step 3: Adding content

##Step 4: Book layout 

Your book will automatically have file called SUMMARY.md and place it in the docs directory. This is what dictates the contents tree of the book (or autogenerate). It looks a bit like this:

```
# Table of content 
* [Getting Started](docs/getting-started.md)
* [API Reference](docs/api-reference.md)
```



##Step 4: Configuration and plugins

Create a book.json in the project’s root. This is used by Gitbook for its settings.

