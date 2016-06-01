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

Go to [gitbook.com](gitbook.com), and then 'new book'. Now, this is __importante__ make sure you choose the github, then select the github repository you set up.

Great. This should have set up the webhooks needed to update your girbook from github. Let's check that by adding some content.
 


##Step 3: Adding content

##Step 4: Marking it Down



__Maths__

{% math %}
 {\partial{\bf u}\over{\partial t}} + ({\bf u} \cdot \nabla) {\bf u} = - {1\over\rho} \nabla p + \gamma\nabla^2{\bf u} + {1\over\rho}{\bf F} 
{% endmath %}


__code__

Render different languages with eg. 

<div>
```python 
your code here...
```

<div>

```python
def FFT(x):
    """A recursive implementation of the 1D Cooley-Tukey FFT"""
    x = np.asarray(x, dtype=float)
    N = x.shape[0]
    
    if N % 2 > 0:
        raise ValueError("size of x must be a power of 2")
    elif N <= 32:  # this cutoff should be optimized
        return DFT_slow(x)
    else:
        X_even = FFT(x[::2])
        X_odd = FFT(x[1::2])
        factor = np.exp(-2j * np.pi * np.arange(N) / N)
        return np.concatenate([X_even + factor[:N / 2] * X_odd,
                               X_even + factor[N / 2:] * X_odd])

```

##Step 5: Book layout 

Your book will automatically have file called SUMMARY.md and place it in the docs directory. This is what dictates the contents tree of the book (or autogenerate). It looks a bit like this:

```
# Table of content 
* [Getting Started](docs/getting-started.md)
* [API Reference](docs/api-reference.md)
```



##Step 6: Configuration and plugins

Create a book.json in the project’s root. This is used by Gitbook for its settings. Plugins are generally added by pasting an entry snippet into the book.json file. 


```json
{
    "pluginsConfig": {
        "mathjax":{
            "forceSVG": true
        }
    }
}

```

##Step 7: When builds go wrong


###Links, blogs, resources

[](https://medium.com/@gpbl/how-to-use-gitbook-to-publish-docs-for-your-open-source-npm-packages-465dd8d5bfba#.acdr3enfr)

