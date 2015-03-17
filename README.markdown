## Open Health Care website

This is the website at http://openhealthcare.org.uk

### Making edits

*Please do not commit directly to gh pages here - thanks*

Broadly works as per their  [deploy to github](http://octopress.org/docs/deploying/github) instructions.

The [OHC Developer box](https://github.com/openhealthcare/developer) will set you up with everything you
need to start editing / adding blog posts.

### Adding a blog post Quick version 

From the dev vagrant machine, 

    cd /usr/lib/ohc/openhealthcare.org.uk
    rvm use 1.9.3@ohcstatic
    rake new_post["Wombles take over the new season at ENO"]
    
This will create a file in ./source/_posts/yyyy-mm-dd-wombles-take-over.markdown

Go edit that.

You can preview with

    jekyll serve -H 0.0.0.0

Go to http://localhost:4000

### Committing && deploying your new post

    git add .
    git commit -a -m "New post re. Wombles."
    git push origin master
    rake generate
    rake deploy

Begins original octopress documentation:
    

## What is Octopress?

Octopress is [Jekyll](https://github.com/mojombo/jekyll) blogging at its finest.

1. **Octopress sports a clean responsive theme** written in semantic HTML5, focused on readability and friendliness toward mobile devices.
2. **Code blogging is easy and beautiful.** Embed code (with [Solarized](http://ethanschoonover.com/solarized) styling) in your posts from gists, jsFiddle or from your filesystem.
3. **Third party integration is simple** with built-in support for Pinboard, Delicious, GitHub Repositories, Disqus Comments and Google Analytics.
4. **It's easy to use.** A collection of rake tasks simplifies development and makes deploying a cinch.
5. **Ships with great plug-ins** some original and others from the Jekyll community &mdash; tested and improved.

**Note**: Octopress requires a minimum Ruby version of `1.9.3-p0`.

## Documentation

Check out [Octopress.org](http://octopress.org/docs) for guides and documentation.
It should all apply to our current stable version (found in the `master`
branch). If this is not the case, [please submit a
fix to our docs repo](https://github.com/octopress/docs).
