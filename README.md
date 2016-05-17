## klug.ir/*BLOG*
\- This repository contains the source code for [klug.ir/blog](http://klug.ir/blog) web site.

\- Feel free to fix typos or make clarifications with a pull request (PR).

\- Contents are converted from Markdown to HTML manually by [Hugo](http://gohugo.io/) static site generator and located in [gh-pages](https://github.com/kermanlug/blog/tree/gh-pages) branch using [this deploy script](https://github.com/X1011/git-directory-deploy).

---
### Posts
- Each post must be located in `content/post`
- `<date>-<post-title>.md` is the naming structure for blog posts.
- A post should be started with the below snippet (called 'frontmatter') at the beginnig:

        +++
        author = "AUTHOR"
        categories = [ "CATEGORY" ]
        date = "YYYY-MM-DDThh:mm:ss+03:30"
        description = "DESCRIPTION"
        featured = ""
        featuredalt = ""
        featuredpath = "/img"
        linktitle = ""
        title = "TITLE"
        type = "post"
        +++

    `YYYY-MM-DD` should be in Gregorian date. `hh:mm:ss` refers to time and don't touch `03:30` which is [Iran UTC time offset](https://en.wikipedia.org/wiki/UTC%2B03:30). You may also see `04:30` that is because of detected summer clock on author's OS.
    When you are still working on your post, add `draft = true` somewhere in frontmatter. Once completed, ensure it’s no longer a draft: `hugo undraft content/post/<file-name>.md` or simply replace 'true' with 'false' or remove that line.

- Images should be kept in `static/img` directory following this naming structure: `<post-name>-<image-title>.jpg`. You can use common formats as in jpeg (jpg), png and gif.

- Since the repo size is limited to 1 GB, It's not recommended to host videos. You can use video streaming services such as Aparat, Youtube, Vimeo, etc.

### @Staff
If you'd like to publish a post, there are 3 plans to do it:

- Plan A+: Dealing with git and command line
- Plan A: Create a post online.
- Plan B: Scroll down to find!

#### Plan A+

1. Install Hugo: [Archlinux (AUR)](https://aur.archlinux.org/packages/hugo-git)/[Ubuntu (16.04)](http://packages.ubuntu.com/xenial/hugo)/['.deb' Packages](https://github.com/spf13/hugo/releases) (optional, recommended)

2. Fork the master repo into your GitHub account. Clone it. Navigate there.

    - Optional: Add upstream as a remote to your local clone:

        `git remote add upstream https://github.com/kermanlug/blog.git`

        (_upstream_ here is just a name, arbitrary. It's just the most common name used in this context.)

        then:

            git fetch upstream #fetches all changes from the original repo 
            git checkout -b new_thing upstream/master #creates a new branch based on the master branch's status of upstream as it was the last time you ran fetch.
            git rebase upstream/master #reapplies all commits of the current branch that are not in the master branch of upstream on top of the master branch of upstream, again upstream/master being master as it was at last time you fetched. Read more: http://stackoverflow.com/a/7244456
        
3. Run `hugo new post/<date>-<post-title>.md`. A new Markdown source would be created within the `content/post` directory. If hugo is not installed, create `<date>-<post-title>.md` manually within `content/post`.

4. Open the new created file in your editor, edit the frontmatter and write your post. You can use a barebone editr, a feature-rich editor or even a wysiwyg (*live*) Markdown editor to work with your post. Here are some Markdown editor:
 
  - [UberWriter](http://uberwriter.wolfvollprecht.de/)/[Haroopad](http://pad.haroopress.com/)/[Remarkable](http://remarkableapp.net/)/[Atom extension](https://atom.io/packages/markdown-preview-plus)/[GitBook](https://www.gitbook.com/editor)/[Emacs Markdown Mode](https://github.com/defunkt/markdown-mode)/etc as native desktop clients.
  - Browser Plugings: [Markdown Preview Plus (Chrom/Chromium)](https://chrome.google.com/webstore/detail/markdown-preview-plus/febilkbfcbhebfnokafefeacimjdckgl) | [Markdown Viewer (FF)](https://addons.mozilla.org/en/firefox/addon/markdown-viewer/)
  - [StackEdit](https://stackedit.io/editor)/[Dillinger](http://dillinger.io/)/[(GitHub-Flavored)_Markdown_Editor](http://jbt.github.io/markdown-editor/)/[Pen](http://sofish.github.io/pen/) as online editors.
  - If you need to draft them in cloud, try [Markable](https://markable.in/).

5. It’s a good idea to preview your work by running: `hugo server`. This will run a full functioning web server while simultaneously watching your file system for additions, deletions or changes. If everything is fine, open a browser to http://localhost:1313/blog/, so that you can see updates as you are working on the post.

6. Add and commit the new post in master branch:

        git add content/post/<POST_NAME>
        git commit -m "<YOUR_DESCRIPTION_HERE>, $(date)"
        git push origin master #Push to your repo

7. Sign in to GitHub and send a [PR](https://help.github.com/articles/using-pull-requests/), wait to be merged.

##### Plan A
You can try GitHub web UI to create a page if you don't feel free with command line! Visit [conten/post](https://github.com/kermanlug/blog/tree/master/content/post) page, take a look at around, you'll see a **_New file_** button, press it. Insert your Markdown contents there, commit it and finish your work by sending a [PR](https://help.github.com/articles/using-pull-requests/).

##### Plan B
None of the above? Simply send your `.md` file to `hello [AT] klug [DOT] ir`.
