# Build2 Learn Chennai website 🌎

 [![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT) [WhatsApp](https://chat.whatsapp.com/6lSVfYjlnbmFWOde8dsRsi)
 
 Join the Build2Learn Github Group - https://b2l-chennai.herokuapp.com/


* Build2learn Chennai's public website
  + [Feature](#feature-)
  + [Getting Started (builing the website locally)](#getting-started-builing-the-website-locally-)
     + [Linux](#linux)
     + [Mac OS](#mac-os)
     + [Windows](#windows)
     + [Docker](#docker)
  + [Writing a post](#writing-a-post-)
  + [Updating the feedback form shortlink](#updating-the-feedback-form-shortlink-️)
  + [Website Structure](#website-structure-)
  + [Contributing](#contributing-)
  + [License](#license-)


Welcome to the Build2Learn Chennai public website 🌎 The website is written with [Jekyll](https://jekyllrb.com/) and hosted on [GitHub Pages](https://pages.github.com/).

The website is publicly available on [http://build2learn.in/](http://build2learn.in/).

Feel free to fork ⸑ or star ⭐️ this repo! Contributions are really appreciated. Please have a look at the [Contributing Guidelines](.github/CONTRIBUTING.md) or at the [TODO](#contributing-) list down there. You can easily start having a look at our [Issues](https://github.com/b2l-chennai/build2learn/issues).

## Feature 💅

* Material Designed (based on [hcz-jekyll-blog](https://github.com/codeasashu/hcz-jekyll-blog) theme) 🎨
* Mobile Responsive 📱
* Push Notifications 🔔 (with [OneSignal](https://onesignal.com/))
* [Progressive Web App](https://developers.google.com/web/progressive-web-apps/) ready 🖥
* HTML5 Cache support ♻️
* Awesome Community behind 🤝

## Getting Started (builing the website locally) 🛠

To get starting developing, we really recommend to clone the website locally and start developing on your machine.

This will allow you to **preview what the generated site** will look like in your browser locally. Jekyll comes also with a *auto-regenerate* feature, this will allow you to quickly iterate over different changes to the website (useful if you're touching the CSS files). More info about the *auto-regenerate* feature on the [Jekyll usage page](https://jekyllrb.com/docs/usage/).

### Linux

1. Install [Ruby](https://www.ruby-lang.org/en/) with your package manager.
```
Debian
sudo apt install ruby

ArchLinux
sudo pacman -S ruby
```

2. Clone this repository (you need `git` installed).
```
git clone https://github.com/b2l-chennai/b2l-chennai.github.io.git
cd b2l-chennai.github.io/
```

3. To configure gems user-wide add the following line to your shell configuration files, for example `~/.bashrc` or `~/.zshrc`
```
export GEM_HOME=$(ruby -e 'print Gem.user_dir')
```

4. Open your terminal and install `jekyll` and `bundler`
```
gem install jekyll
gem install bundler
```

5. To run executable gems, without typing the full location, run the following command or add it to your shell configuration files, for example `~/.bashrc` or `~/.zshrc`.
```
PATH=$(ruby -e 'print Gem.user_dir')/bin:$PATH
```

6. To install gems into `GEM_HOME`
```
bundle install
```

7. Serve the website with the following command,
```
bundle exec jekyll serve
```

You should be able to see the local website at [http://127.0.0.1:4000](http://127.0.0.1:4000)

### Mac OS

To be able to build the site locally, you need [Homebrew](https://brew.sh/index.html) installed. [Please follow this link to install Homebrew](https://brew.sh/index.html)

1. Clone this repository (you need `git` installed).
```
git clone https://github.com/b2l-chennai/b2l-chennai.github.io.git
cd b2l-chennai.github.io/
```
2. Open your terminal and install `ruby`, `jekyll` and `bundler` (skip the related command if you already have the package installed).
```
brew install ruby
sudo gem install jekyll
sudo gem install bundler
```
3. Serve the website with the following command
```
bundle exec jekyll serve
```

You should be able to see the local website at [http://127.0.0.1:4000/](http://127.0.0.1:4000/).

### Windows
You must have [git](https://git-scm.com/downloads) for windows installed in your system.

1. Download and install **Ruby** and **Rubygems** using [rubyInstaller for windows](https://rubyinstaller.org/)

2. Using git bash, clone this repository.
```bash
git clone https://github.com/b2l-chennai/b2l-chennai.github.io.git
cd b2l-chennai.github.io/
```
2. On your terminal install `jekyll` and `bundler`
```bash
gem install jekyll bundler
```
3. Serve the website with the following command
```bash
bundle exec jekyll serve
```

You should be able to see the local website at [http://127.0.0.1:4000/](http://127.0.0.1:4000/).

### Docker

1. Be sure to have Docker installed on your local machine
```
Ubuntu
sudo apt-get install docker

ArchLinux
sudo pacman -S docker
```

2. Clone this repository (you need `git` on your machine)
```
git clone https://github.com/b2l-chennai/b2l-chennai.github.io.git
cd b2l-chennai.github.io/
```

3. Run a Docker container with `jekyll/jekyll` image and serve the site
```
docker run --rm -it \
-p 4000:4000 -v "$PWD":/srv/jekyll \
jekyll/jekyll jekyll serve
```

You should be able to see the local website at [http://127.0.0.1:4000](http://127.0.0.1:4000)

This command will download the [`jekyll/jekyll`](https://hub.docker.com/r/jekyll/builder/) image from Docker Hub and build a container from that image.  
Container port 4000 is linked to `localhost:4000`, so that you can access the site from that address.  
Every time this container is executed, it'll automatically do a `bundle install`, thus retrieving all Gem dependencies before building and serving.

## Writing a post 📝

To add a new post to the blog page, you need to create a new file in the [`_post`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_posts) folder. Please follow the naming of the file, like:
```
2018-01-29-hello-world.md
```

The structure of the blog post file should be as following:

```markdown
---
layout: post
title: <TITLE OF YOUR BLOGPOST>
date:   <DATE OF YOUR BLOGPOST LIKE '2018-01-29 13:50:39'>
categories: <LIST OF SPACE SEPARATED CATEGORIES>
---

<BODY OF YOUR BLOGPOST>
```


## Website Structure 🗺

Here a short description of the project structure:

* [`_config.yml`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_config.yml) **Jekyll config file**, used to provide projectwise configuration.
* [`_data`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_data) Contains JSON files used to build pages
    - [`_data/project.json`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_data/project.json) Used to build the [/projects](https://build2learn.in/projects/) page.
    - [`_data/social.json`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_data/social.json) Used to create the social buttons.
    - [`_data/urls.json`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_data/social.json) Used to create the navigation bar.
* [`_includes`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_includes) Static HTML files that will be used to generate web pages
    - [`_includes/analytics.html`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_includes/analytics.html) Google Analyics snippet.
    - [`_includes/css.html`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_includes/css.html) CSS Includes go here.
    - [`_includes/header.html`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_includes/header.html) Header for all pages is here, including the homepage with the big image.
    - [`_includes/footer.html`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_includes/footer.html) Footer for all pages is here.
    - [`_includes/js.html`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_includes/js.html) JS Includes go here.
    - [`_includes/main.html`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_includes/main.html) Main content is here (whatever is between header and footer).
    - [`_includes/meta.html`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_includes/meta.html) META tags go here.
    - [`_includes/navigation.html`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_includes/navigation.html) Navigation menu is here.
    - [`_includes/share-page.html`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_includes/share-page.html) Share buttons (after content) are here.
    - [`_includes/social_links.html`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_includes/social_links.html) Social buttons in the header are generated here.
* [`_layouts`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_layouts) Layout files used to create pages
    - [`_layouts/default.html`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_layouts/default.html) **Default layout**, all the pages follow this structure. All the other layouts will just add elements to this layout.
    - [`_layouts/page.html`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_layouts/page.html) **Page layout**, used to render static pages (like the [About](http://build2learn.in/) page).
    - [`_layouts/post.html`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_layouts/post.html) **Blogpost layout**, used to render blogposts from the [`_posts`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_posts) folder).
    - [`_layouts/posts_by_gategory.html`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_layouts/posts_by_gategory.html) Layout used when user clicks on a specific category.
    - [`_layouts/project.html`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/_layouts/project.html) **Projects layout**, used to display seminars with Cards.
* [`blog/index.html`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/blog/intex.html) Index file for the [blog](https://build2learn.in/blog/) page. Used by the [`jekyll-paginate`](https://jekyllrb.com/docs/pagination/).
* [`category`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/category) Contains one file for every **category**. Please add files here before using new categories in blogposts.
* [`manifests`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/manifests) Contains manifests file for the PWA.
* [`static`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/static) Contains static files served directly by Jekyll (Images, JS, CSS, etc.)
    - [`static/css`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/static/css) CSS and SASS files goes here. `.scss` file starting with double `---` will be built by Jekyll and the resulted `.css` file will be available in the [`static/css/_site`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/static/css/_site) folder. Please note that this project is using [Bootstrap Material Design](https://fezvrasta.github.io/bootstrap-material-design/), feel free to use the CSS classes you need.
    - [`static/img`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/static/img) Images goes here
    - [`static/js`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/static/img) Javascript files goes here.
* [`about.md`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/about.md) **About page**, Markdown file used to create it.
* [`feed.xml`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/feed.xml) XML File used to create the RSS feed.
* [`projects.md`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/projects.md) **Projects page**, Markdown file used to create it. For cards creation refer to the project layout file.
* [`feed.xml`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/feed.xml) XML File used to create the RSS feed.
* [`feedbackform.md`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/feedbackform.md) **Feedback form** redirect page, used to handle the feedback form QR code.
* [`sw.js`](https://github.com/b2l-chennai/b2l-chennai.github.io/tree/master/sw.js) Service Worker used for PWA purpose.

## Contributing 🤝

Feel free to contribute to this project! You can have a look at our [Contribution guidelines](.github/CONTRIBUTING.md) if you don't know how to proceed.

Feel free to [open a issue](https://github.com/b2l-chennai/b2l-chennai.github.io/issues/new) or [submit a new pull request](https://github.com/b2l-chennai/b2l-chennai.github.io/pulls) ❤️

Here a short TODO list:

- [ ] Create the *hall of fame* page to display the projects done and made during the build2learn meets.

## License 📄

This project is licensed under the MIT License - see the [License](License) file for details
