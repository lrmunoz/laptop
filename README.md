Modified Laptop
======

This is a fork of [thoughtbot/laptop](https://github.com/thoughtbot/laptop) customized to my personal needs. See the original repo's documentation for details, the rest of this document are my personal notes about my own installation.

Previous steps
--------------

- Encrypt hard drive
- Enable installation of programs from untrusted sources
  You need to enable installation from anywhere, by running in the terminal: `sudo spctl --master-disable`
- Leave only Applications, Desktop, and home folder in Finder favorites
- Customize finder toolbar: Add Quick Info, Quick Look, Actions and Path shortcuts

Programs, utilities, etc. installed by the script
-------------------------------------------------

- Homebrew
- Homebrew Cask
- Homebrew Caskroom-fonts
- OneDrive
- Chrome
- Firefox
- Sublime Text 3
- Spectacle window manager
- Spotify
- RescueTime
- Telegram
- Xcode
- Git (see specific comments)
- SourceTree
- KeepassX
- Intellij
- Slack
- rbenv
- Ruby (via rbenv as needed)
- node
- PhantomJS
- Imagemagick
- Nag
- Postgres app
- Qt5
- Npm
- OneNote
- Adobe Reader
- Syncthing
- Docker
- Omnifocus
- Ansible
- Kitematic
- Steam / Rocksmith
- GPG suite

Note on QT5 on Sierra
---------------------

As of writing this, QT5 (needed for capybara-webkit) doesn't install on Sierra with homebrew. See a workaround here:

https://github.com/thoughtbot/capybara-webkit/wiki/Installing-Qt-and-compiling-capybara-webkit#macos-sierra-1012

If you get an error like `xcode-select: error: tool 'xcodebuild' requires Xcode, but active developer directory '/Library/Developer/CommandLineTools' is a command line tools instance` (probably caused by Homebrew being run before installing Xcode), check the following link:

https://github.com/nodejs/node-gyp/issues/569

Git
---

It is recommended to install a global .gitignore file:

`git config --global core.excludesfile [path]/.gitignore_global`

Oh My ZSH
---------

After running the script for the first time, install [Oh My ZSH](https://github.com/robbyrussell/oh-my-zsh)

It comes with the git plugin preinstalled, so it adds git autocompletion by default

Ruby
----

Ruby versions are handled with rbenv so any specific project has its own independent ruby version & gems

If you need the `pg` gem, in some project, compile it with the Postgres libraries included in the Postgres.app:

`gem install pg -v [gem_version] -- --with-pg-config=/Applications/Postgres.app/Contents/Versions/[version]/bin/pg_config`

Post-install
------------

- Install Oh My ZSH and add plugins (TODO: add to the script to install automatically)

- Login to Chrome to sync bookmarks

- Install printers

License
-------

Laptop is © 2011-2016 thoughtbot, inc.
It is free software,
and may be redistributed under the terms specified in the [LICENSE] file.

[LICENSE]: LICENSE

