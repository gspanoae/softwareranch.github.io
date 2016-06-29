# **[sofwareranch.github.io](https://softwareranch.github.io/)** - **Under Construction**

The articles and source code on this project are open source and can be freely used under the conditions of the CC BY-SA license (see [below](#licenses)). Code is licensed under MIT.

## Development Setup

1) Check Jekyll prerequisites at: <https://jekyllrb.com/docs/installation/#requirements>

2) Install Jekyll (<https://jekyllrb.com>): 

```shell
    $ gem install jekyll
```

3) Install GitHub-Pages (<https://github.com/github/pages-gem>):
    
```shell
    $ gem install github-pages
```

4) Install Rouge (<https://github.com/jneen/rouge>):
    
```shell
    $ gem install rouge
```

5) Clone this repo

6) Start Jekyll server
    
```shell 
    $ jekyll serve
    # => A development server will run at http://127.0.0.1:4000/
    # Auto-regeneration: enabled. Use --no-watch to disable.
```

## Technology Used

- [Jekyll](http://jekyllrb.com): A simple, blog-aware, static site generator for personal, project, or organization sites.
- [GitHub Pages Ruby Gem](https://github.com/github/pages-gem): A simple Ruby Gem to bootstrap dependencies for setting up and maintaining a local Jekyll environment in sync with GitHub Pages.

```shell
    # Bundler provides a consistent environment for Ruby projects by tracking and installing the exact gems and versions that are needed. 
    $ gem install bundler
    # Bundler ensures that the gems you need are present in development, staging, and production.
    $ bundle install
    # Update the gems specified (all gems, if none are specified), ignoring the previously installed gems specified in the Gemfile.lock. 
    # In general, you should use bundle install to install the same exact gems and versions across machines.
    $ bundle update github-pages
    # Checks your GitHub Pages site for common DNS configuration issues
    $ github-pages health-check
```

- [Rouge](http://rouge.jneen.net/): Extendable code highlighter written in pure Ruby. Default syntax highlighter for Jekyll.
- [GitHub Pages](https://pages.github.com): GiHub websites for you and your projects.
- [Sass](http://sass-lang.com/): Professional, mature, and stable CSS extension language.

## Licenses

- Content: [CC BY-SA](https://creativecommons.org/licenses/by-sa/4.0/)
- Code: [MIT License](http://opensource.org/licenses/MIT)
