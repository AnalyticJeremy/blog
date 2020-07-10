# Any Means Necessary
## a data science site by me, AnalyticJeremy

I wanted to make a blog so I'd have a place on-line to stash some of the various data analyses that I make in my spare time.  But who wants
to fool around with making a whole blog site somewhere?  So instead I'm just using my GitHub repository to store my blog.  And thanks to
[Hugo](https://gohugo.io/), I can make it look great!

I decided the blog would need a stupid name, and all the cool kids make some sort of statistics-related pun.  So my blog is called "Any Means Necessary"...
because, like, means are super important in statistics.

### Workflow
(These notes are for me... to remind me how I set this thing up and how to make new posts.  Since I post so infrequently, I need to leave myself
some breadcrumbs. So please remember that the following is a conversation with myself.)

#### Initial Setup
- Install R, RStudio, and common packages (duh!)
- Install [blogdown package](https://bookdown.org/yihui/blogdown/installation.html)
- Don't forget RMarkdown package!
- You also need to install [pandoc](https://pandoc.org/installing.html) on your machine

#### The GitHub Setup
The setup for blogdown / Hugo isn't quite as nice as it was under the original Jekyll scheme.  There are now *two different repositories*.
There's this one call "blog" where we store all of the config files, templates, theme files, etc.  When the site is built, it puts the
output into a different folder, which is mapped to the "analyticjeremy.github.io" repository.  That's where the actual site that GitHub
serves to the web is stored.

So remember... make changes/additions in this repository, rebuild the site, and then push *both* repositories back to GitHub.

The initial check-in for this repository was made with only minor changes to the `config.toml` file.  Everything else (including
the "beautifulhugo" theme) should be stock.  From there, we will make further customizations, but we can track them in Git so
we'll have a record of what we did.

#### Running Locally
Want to view the site locally as you're writing your posts?  Of course you do!  There's a fancy way to do that from within RStudio,
but it bombs out when you try it.  But Yihui Xie [seems to be aware of this](https://bookdown.org/yihui/blogdown/rstudio-ide.html)
potential problem.

To work around it, just author the documents in RStudio.  But start up plain R console and use `blogdown::serve_site()` from there.
That will launch a local web server and open the compiled site in a regular browser window.

#### Authoring New Posts
This part is *much* easier than under the old Jekyll system.  In RStudio, just open the R project for the blog, go to the "Add Ins" menu
and select "New Post".  As you save it, the preview site will be automatically regenerated.

#### Customizations
 - Copied and tweaked "/themes/beautifulhugo/layouts/index.html" to "/layouts/posts/list.html" so I could have a separate index
 page for listing all of the blog posts
 - Modified "/themes/beautifulhugo/layouts/index.html" to make more of a general landing page for the site.  Made it two columns
 and added my GitHub projects
