### setup on local machine:

- use RubyInstaller to install Ruby + Jekyll + Bundler
    - select latest with DevKit from [here](https://rubyinstaller.org/downloads/)
    - run all with default settings, including `ridk install` at end of setup
- open new terminal (to update PATH variable), install Jekyll and Bundler
    - `gem install jekyll bundler`
- navigate to this project's folder, set it up
    - `bundle init` (creates a gemfile)
    - add `gem 'github-pages', group: :jekyll_plugins` to gemfile
    - run `bundle install`
    - run `bundle add webrick`

once everything is set up, you can simply run:
```
bundle exec jekyll serve
```

### todos

- [ ] update cv
- [ ] add pdfs/links to publications where possible
- [ ] copy some projects from old website
- [ ] direct martin-rudorfer.com to this website
- [ ] get a google seo key
- [ ] perhaps add teaching? BGA stuff would be nice
