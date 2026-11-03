# SPIN 2027

Website for SPIN 2027, based on the [SPIN 2026 repository](https://github.com/SPIN-web/SPIN2026).
Built with Jekyll for https://spin-web.github.io/SPIN2027/.

Program chairs: Emily Yu (z.yu@liacs.leidenuniv.nl) and Carlos Esteban Budde (cesbu@dtu.dk).
Abstract submission deadline: January 21, 2027.
Paper submission deadline: January 28, 2027. All deadlines are AoE (anywhere on Earth). SPIN takes place April 14–15, 2027, co-located with ETAPS 2027 in Copenhagen, Denmark. Other dates, committees, speakers,
and submission details are awaiting confirmation.

## Basic Setup

The website is made with [Jekyll](https://jekyllrb.com) and hosted on [GitHub pages](https://docs.github.com/en/pages/). It should work out-of-the-box by pushing the respective changes to the `main` branch of the repository.

It is recommended to develop and test this site locally with the built-in web server of the toolchain. This guide is for Unix-like systems and has been tested on Arch Linux (September 2024).

Install [Ruby](https://www.ruby-lang.org), e.g., with the standard package manager of your distribution, make sure the binary `bundle` of its [package manager](https://bundler.io/) is available.

Set up `bundle` to use a user-writable directory for installing dependencies, cf. [this Stack Overflow question](https://stackoverflow.com/questions/40385493/how-to-run-bundle-install-as-normal-user).
You may want to persist this as part of your shell configuration.

    export GEM_HOME="$(ruby -e 'puts Gem.user_dir')"
    export PATH="$GEM_HOME/bin:$PATH"

Install the dependencies for the website (once)

    bundle install

Run the built-in webserve and point your browser to the "Server address" as shown

    bundle exec jekyll serve

The running webserver will monitor changes to the file system and update the pages automatically. Any changes should therefore be visible upon browser refresh.

## Updating the Website

File `_config.yml` contains the main configuration, including the title and URL.

Sources for the individual pages are in subdirectory `_pages`. They are formatted with [Markdown](https://www.markdownguide.org/).
The engine used to process the pages is currently configured to [Kramdown](https://kramdown.gettalong.org/).

## Header photograph

[Nyhavn-panorama.jpg](https://commons.wikimedia.org/wiki/File:Nyhavn-panorama.jpg)
by Scythian, used under [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).
Original resolution: 3583 × 1321. The photograph is displayed with a responsive CSS crop;
the original image file is unchanged.
