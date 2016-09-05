# gixnote

Personal Note

## Prerequiite

* Linux (or Ubuntu 14.04)
* Python 2.7
* Virtualenv(Wrapper)
* For Ubuntu `sudo apt-get install texlive-full`

## Setup New Environment

    mkvirtualenv -p /usr/bin/python2 gixnote
    git clone git@github.com:9gix/gixnote.git
    pip install -r requirements.txt

## Setup Build Directory

    mkdir ../gixnote-build
    cd ../gixnote-build
    git clone git@github.com:9gix/gixnote.git html
    cd html
    git symbolic-ref HEAD refs/heads/gh-pages
    rm .git/index
    git clean -fdx

## Making New Notes

Make the note changes inside the [source](source/) directory.

## Build the Notes

    workon gixnote # just to make sure you are on the right environment
    make html

## View Result

- The built result is located at `../gixnote-build/`. 
- And the WebPages is located at `../gixnote-build/html/`

## Deploy The Web pages

    make deploy

[Verify deployment](http://9gix.github.io/gixnote)
