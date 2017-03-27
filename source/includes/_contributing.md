# Contributing

This is a living document.
It is up to all of us to make sure the information it contains is relevant and useful!

We encourage you to contribute, whether you're fixing a typo or adding a new section.

## __Fork__ the repository

_Forking_ is essentially making a copy of a repository.
You can then make changes to it for your own purposes.

The source code for this website can be found [on Github](https://github.com/redacademy/js-fundamentals).

When you visit a repository page on Github, the __fork__ button can be found in the top-right corner.
Click it and choose your account as the place to "fork to".

## __Clone__ your fork of the repo

```sh
cd an/appropriate/directory
git clone git@github.com:YOUR_USERNAME/html-fundamentals.git
cd js-fundamentals
```

_Cloning_ is the term we use for copying code from Github to our local filesystem.

The `clone` command automatically creates a new folder with the repository name; in this case, `js-fundamentals`.

## __Install dependencies__ and __serve__


```sh
# Install:
gem install bundler
bundle install

# Serve
bundle exec middleman server
```

- __Gem__ is a ruby package manager.
- __Bundle__ allows us to install packages based on a list found in a file called `Gemfile`
- __Middleman__ is a lightweight server that runs locally.

Once your server is running, you can visit a local version of the site at [localhost:4567](http://localhost:4567/)!

## Contribute!

This site is written entirely in [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).
Each section has its own file in `/source/includes`. You can update any existing files.

If you'd like to add a new section:

- Create a new file in /source/includes
- Make sure the filename starts with an underscore, ie `_section`
- Tell the site to render the new section by adding it to the `includes` list in `index.html.md`.

## Make a pull request

```sh
git add --all
git commit -m "Made a contribution!"
git push origin master
```

Once you've finished your work, commit your changes and push them to your local repository.

Next:

- Visit your fork on Github - https://github.com/YOUR_USERNAME/js-fundamentals
- Click the __Pull Requests__ tab
- Click the __New Pull Request__ button
- It should automatically compare your fork with the master repository
- Submit your pull request!

## Merge conflicts

You may end up with merge conflicts with the base fork.
To resolve, you'll first have to add the base fork to your local git.

```sh
git remote add upstream https://github.com/redacademy/js-fundamentals.git
```

Then you can get the most recent code from the base for and merge it into your local code.

```sh
git fetch upstream
git merge upstream/master
```

Then you can resolve your conflicts and push back to your fork.
Pull requests update automatically when new commits are pushed.
