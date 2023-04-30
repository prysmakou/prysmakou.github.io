# Static web site

This repository contains a [Jekyll](https://jekyllrb.com/) site served via GitHub Pages.

## Installation (macOS)

1. Install [Homebrew](https://brew.sh) if it is not already present.
2. Install [asdf](https://asdf-vm.com) and add it to your shell:

   ```bash
   brew install asdf
   echo -e '\n. "$(brew --prefix asdf)/libexec/asdf.sh"' >> ~/.bash_profile
   source ~/.bash_profile
   ```
3. Install a Ruby version compatible with GitHub Pages (for example 3.1.4) and set it for the project:

   ```bash
   asdf plugin add ruby
   asdf install ruby 3.1.4
   asdf set ruby 3.1.4
   ```
4. Install bundler and project dependencies:

   ```bash
   gem install bundler
   bundle install
   ```
5. Serve the site locally:

   ```bash
   bundle exec jekyll serve
   ```

## Installation (Ubuntu)

1. Install Ruby and build tools:

   ```bash
   sudo apt-get update
   sudo apt-get install ruby-full build-essential zlib1g-dev
   ```
2. Configure RubyGems to install to your home directory:

   ```bash
   echo '# Install Ruby Gems to ~/.gem' >> ~/.bashrc
   echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
   echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
   source ~/.bashrc
   ```
3. Install bundler and project dependencies:

   ```bash
   gem install bundler
   bundle install
   ```
4. Serve the site locally:

   ```bash
   bundle exec jekyll serve
   ```



