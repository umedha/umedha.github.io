+++
title = "Migrating my website to Hugo + Academic"
author = ["Mark S. Handcock"]
date = 2022-04-20
tags = ["Workflow"]
draft = false
+++

After many years with a hand written website in HTML, I moved to using the [Hugo](https://gohugo.io/) framework with the 
[Academic theme](https://sourcethemes.com/academic/).
The motivation for this is the work of [Qingyuan Zhao](http://www.statslab.cam.ac.uk/~qz280/post/migrating/) who deserved the credit for both creating the template and also publishing it so that others can benefit from it. Thank you, Qingyuan Zhao!

## The Hugo framework with the Academic theme

Based on Qingyuan's work, I decided to use Hugo as it is an efficient language expressing
the best aspects of markdown. The Academic theme for Hugo is well suited for
the websites of academic researchers.

It helps to have Hugo installed locally as you can compile the website and see what you will get. Installing Hugo in Mac OS X is
straightforward with [homebrew](https://brew.sh/). Simply run

```sh
brew install hugo
```
### Creating a local website

First, clone my repository or Qingyuan's. I put mine in "handcock.github.io". Then rename it to \<git hub ID\>.github.io

You can preview the website by running

```sh
hugo server --baseURL http://localhost:1313/
```

from the website directory (e.g., "handcock.github.io"). This builds the website and creates a
local web server to host it. It generates a link (the default is <http://localhost:1313/>)
which can be pasted into a web browser. In the background, the hugo
server also detects any change to the content and updates the website
automatically.

### Making it your website

The files are all writen as text files in markdown. The `content` sub-folder contains all the Markdown files
for website content.

```text
├── content
│   ├── authors
│   ├── featured
│   ├── group
│   ├── home
│   ├── post
│   ├── project
│   ├── publication
│   ├── research
│   ├── talk
│   └── teaching
```

Most of its sub-directories correspond to a
section of my webpage (take a look at it); in particular, `home` corresponds to the
homepage of your website. Another unique folder is the `authors`,
which contains basic information about the website owner and all other
authors (not needed for a personal website). The `publication` corresponds to each of my publications.

Basically, you will edit the text files in each of these sub-directiries to change them to ones that are for you (as now they are all for me!).

See [its documentation](https://sourcethemes.com/academic/docs/get-started/) for more information.

### Creating a public website

Commit your website as a repository on github (with \<git hub ID\>.github.io as a name).

After successfully committed, go to your repository and click on the “Settings” on the top right, then scroll down to the Github Pages section.
Then  click on the published link.
