---
layout: posts
title: Local testing of GitHub Pages on MacOS
author: me
words: 470
excerpt: I can't believe this took me so long to debug.
tags: 
  - tutorial
---
The procedure isn't that bad, but certain resources create conflicts that are a little hard to track down. 

After you've already set up a Jekyll site on GitHub Pages, these are steps to help check it locally to avoid waiting for GitHub to publish it to make sure everything looks good.

## Resources

- Jekyll docs: [Jekyll on macOS](https://jekyllrb.com/docs/installation/macos/).
- GitHub docs: [Testing your GitHub Pages site locally with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll).
- Moncef Belyamani: [The fastest and easiest way to install Ruby on a Mac in 2024](https://www.moncefbelyamani.com/how-to-install-xcode-homebrew-git-rvm-ruby-on-mac/#how-to-install-different-versions-of-ruby-and-switch-between-them)

## Part 1: Setting up packages

1. Install Homebrew
	1. `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
	2. Or download from the PKG file on GitHub [here](https://github.com/Homebrew/brew/releases/tag/4.4.15)
2. Install `chruby` (comes with Bundler)
	1. `brew install chruby ruby-install`
	2. `ruby-install ruby 3.3.4`
		1. This step takes a very long time (10 minutes? 20 minutes??)
	3. Follow applicable terminal instructions to source `chruby` install of the default macOS Ruby
		1. `echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc`
		2. `echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc`
		3. `echo "chruby ruby-3.3.5" >> ~/.zshrc # run 'chruby' to see actual version`
	4. Check `ruby -v`
3. `bundle update github-pages`

## Part 2: Launching the website

1. `cd WEBDIR`
2. `bundle install`
3. `bundle exec jekyll serve`
4. Go to http://127.0.0.1:4000 aka http://localhost:4000. 

## Error handling

If everything goes perfect, the above steps will probably take around 20 minutes. Here are things that tripped me up:

### Following the Jekyll docs creates a version conflict with GitHub Pages

The latest supported version of Jekyll and Ruby (described int he Jekyll docs) are not consistent with the [GitHub Pages dependencies](https://pages.github.com/versions/). Moncef Belyamani provides steps to install a new version of Ruby and get everything squared away. As of Jan 06, 2025, the version of Ruby to use is 3.3.4. The steps are abbreviated here:

1. `ruby-install 3.3.4`
2. Quit and restart the terminal. 
3. `chruby 3.3.4`
4. `cd WEBDIR`
5. `echo "3.3.4" >> .ruby-version`
6. Add `ruby File.read(".ruby-version").strip` to the Gemfile. 

### Updating doesn't remove old conflicts

After I figured out that `bundle update github-pages` was correct, I kept get an old error about `?tainted` not being a valid command. This is because of an old conflict with `liquid-4.0.3` when the new dependencies require `liquid-4.0.4`. Manual uninstallation was required. 

1. `gem uninstall -aIx`
2. `bundle update github-pages`

### Missing webrick Gem

Running the site with `bundle exec jekyll serve` can create an error due to `webrick` being missing. 

1. `bundle add webrick`
2. Rerun `bundle exec jekyll serve`