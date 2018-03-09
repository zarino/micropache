# micropache

Starts an Apache webserver in the current directory.

Kind of like `python -m SimpleHTTPServer` or `jekyll serve`,
but for Apache and PHP.

Works with the default Apache installed on your Mac, or with
custom Apaches installed via package managers like Homebrew.

## Installation

    cd /usr/local/bin
    git clone https://github.com/zarino/micropache.git

`/usr/local/bin` is on the default `$PATH` in OS X 10.10 and above,
but if you’re on an older version of OS X you might need to manually
add it to your `$PATH`.

## Usage

    cd ~/some/web/directory
    micropache

The contents of `~/some/web/directory` will now be available at
<http://localhost:8000> (or the first available port above that).

Server logs will be output to the console. Press `Ctrl-C` to stop the server.

You can specify the port you want to run the server on:

    micropache --port 4000
    micropache --port 80

Serving on ports below 1024 will require an administrator password.

By default, the server will run as whatever user and group your version
of Apache would normally run as (usually `_www` and `_www`, respectively).
If you want to specify a custom user/group, you can request them by name:

    micropache --user www-data --group www-data

Or by ID:

    micropache --userid 520 --groupid 20

Or, if you just want the server to run as _your_ current user:

    micropache --as-me
