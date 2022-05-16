# Getting started

## Developer laptop set-up

### Vagrant

Check out the Abilian Devbox project on GitHub (NB: doesn't exist yet.)

### Linux box

Prefer a Debian or Ubuntu based distribution if you want to use the advice below.

Use the `install.sh` script from Abilian Devbox (NB: doesn't exist yet).

### Mac OS X (Native)

Install [Homebrew](http://brew.sh/).

Install some dependencies:

```
brew install cairo cloc curl fontconfig freetype gdbm git \
   harfbuzz icu4c libffi libmagic libpng node openssl pango \
   pcre pixman pkg-config postgresql python python3 redis wget
```

(TODO: this is actually overkill, since some of these packages are actually dependencies of others.)

### Generic (Python tools)

Install virtualenvwrapper:

```
pip install virtualenvwrapper
```

Then create one virtualenv for each of your projects, activate it when you start working on it, and you're done.

You may need to start PostgreSQL and Redis manually (or use [launchrocket](https://github.com/jimbojsb/launchrocket) if you prefer).
