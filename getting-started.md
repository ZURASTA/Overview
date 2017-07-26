Getting Started
===============

This document contains the instructions to get up and running with what you may need for the various projects. If this is your first time using one of our projects, run through this guide and you should be good to go. :)

This document is aimed at team members, but may provide information useful to others who are simply interested in a project we develop.


Communications (Team)
=====================

If you're on the team, we will communicate on slack at: http://zurasta.slack.com


Project Management (Team)
=========================

We are using Waffle for managing most of our tasks, the board can be found at: https://waffle.io/ZURASTA

For some additional things we will use our Trello.


Documentation
=============

An online portal for all of our project documentation can be found at: http://docs.zurasta.io


Tools
=====

Development Environment
-----------------------

Any tools used to assist with the development, configuration, and setup.


### Package Management

For handling the installation of the various tools, much of this guide will use a package manager to achieve that.

#### Mac OS X

This guide will use the package manager Homebrew, this can be installed by following the instructions at: http://brew.sh

Alternatively if you use another package manager like MacPorts, the brew related commands that you'll see in the guide can usually be substituted with the equivalent `sudo port install` command.

#### Debian/Ubuntu Linux

Assumes you are using the apt package manager. This should be the default package manager on the system.


### Editor

How you might wish to configure your editor.

#### Atom (Windows/Mac/Linux)

Elixir packages:

* [atom-elixir](https://atom.io/packages/atom-elixir)
* [language-elixir](https://atom.io/packages/language-elixir)

Erlang packages:

* [language-erlang](https://atom.io/packages/language-erlang)
* [autocomplete-erlang](https://atom.io/packages/autocomplete-erlang)

Elm packages:

* [language-elm](https://atom.io/packages/language-elm)
* [elm-format](https://atom.io/packages/elm-format)

GraphQL packages:

* [language-graphql](https://atom.io/packages/language-graphql)

R packages:

* [language-r](https://atom.io/packages/language-r)


Development Stack
-----------------

Tools/software our projects will often depend on.


### Elixir

To install Elixir follow the installation instructions at: http://elixir-lang.org/install.html

#### Mac OS X (Homebrew)

```bash
brew install elixir
```

#### Linux

If you're unable to get the required Elixir version installed on your environment using the suggested instructions for your given distro (some of the package managers don't stay up to date). Another option is to use to follow this guide: https://gist.github.com/rubencaro/6a28138a40e629b06470


### Elixir Documentation (Optional)

For documentation we sometimes use SvgBob. If you're planning on generating a local copy of the docs, you may need to install these.

#### 1. Install Rust

To install Rust follow the instructions at: https://www.rust-lang.org/en-US/install.html

#### 2. Install SvgBob

```bash
cargo install svgbob
```

#### 3. Install Goon

To install Goon follow the instructions at: https://github.com/alco/goon

#### 4. Setup (Mac OS X)

Add the following to your bash resource (`.bashrc`) or profile (`.bash_profile`) file.

```bash
source $HOME/.cargo/env
export PATH=$PATH:~/goon
```


### PostgreSQL

To install PostgreSQL other than the ways provided below see: https://wiki.postgresql.org/wiki/Detailed_installation_guides

#### Debian/Ubuntu Linux

```bash
sudo apt-get install postgresql
```

Change the postgres user's password to `postgres`. As our projects commonly use `postgres` for the user and password for development and test builds.

```bash
sudo -i -u postgres
psql
ALTER ROLE postgres WITH PASSWORD 'postgres';
```

#### Mac OS X (Homebrew)

```bash
brew install postgresql
```

Create the postgres user, and setup db.

```bash
createuser -s postgres -P # when prompted for password, enter: postgres
```

Note: Whenever running a project you will need to make sure the db instance is running. To do this you will need to run the following:

```bash
postgres -D /usr/local/var/postgres
```


### PostGIS

To install the PostGIS extension other than the ways provided below see: http://postgis.net/install/

This should be done after installing PostgreSQL.

#### Debian/Ubuntu Linux

```bash
sudo apt-get install postgis
```

#### Mac OS X (Homebrew)

```bash
brew install postgis
```


### R

To install R follow the installation instructions at: https://cran.r-project.org

#### Mac OS X (Homebrew)

```bash
brew tap homebrew/science
brew install Caskroom/cask/xquartz
brew install r
```


### Elm

To install Elm follow the installation instructions at: https://guide.elm-lang.org/install.html
