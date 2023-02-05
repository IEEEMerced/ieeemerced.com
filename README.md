# ieeemerced.com

This repository holds the source code for our [website](https://ieeemerced.com/). It is currrently hosted using github pages, though it could be trivially hosted elsewhere, since it is a static website generated using [Jekyll](https://jekyllrb.com).

Please note that the [Jekyll theme](https://github.com/IEEEMerced/ieeemerced-jekyll-theme) we use is hosted in a seperate repo and that this repo is mostly intended to contain content specific to our site. 

## Building

To build the website locally, simply clone the repo using

```
git clone https://github.com/IEEEMerced/ieeemerced.com.git
```

### Dependencies

In order to build the website, some [dependencies](https://jekyllrb.com/docs/installation/) will need to be installed.

#### Ubuntu
```
sudo apt-get install ruby-full build-essential zlib1g-dev
```

#### Debian
```
sudo apt-get install ruby-full build-essential
```

#### Fedora
```
sudo dnf install ruby ruby-devel openssl-devel redhat-rpm-config @development-tools
```

#### Arch Linux
```
sudo packam -S ruby base-devel
```

### Configure RubyGems directory

Further, you should configure a local installation directory for RubyGems packages so that they don't need to be installed under the root user. This can be done by adding the following lines to `~/.bashrc`:

```
# Install Ruby Gems to ~/.gems
export GEM_HOME="$HOME/.gems"
export PATH="$HOME/.gems/bin:$PATH"
```

Next, execute your current `~/.bashrc` using

```
source ~/.bashrc
```

### Install Jekyll and Bundler

Finally, install Jekyll and Bundler using

```
gem install jekyll bundler
```

### Build the Site

Now the site is ready to be built. Inside the repository, simply run

```
bundle install
```

to install all dependencies specific to the website. Then, to build and run the website locally use

```
bundle exec jekyll serve
```

The website should now be live at [localhost:4000](http://127.0.0.1:4000/).

## Contributing

If you would like to help with this website, either internally or externally, please clone or fork the repo and submit any changes to the staging branch here. If you find any issues, feel free to report them [here](https://github.com/IEEEMerced/ieeemerced.com/issues/new).