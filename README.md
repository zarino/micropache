# micropache

Starts an Apache webserver in the current directory.

Built to quickly run PHP sites on a Mac, using the system Apache binary, but without messing with virtualhosts and the default system config files.

## Installation

    cd /usr/local/bin
    git clone https://github.com/zarino/micropache.git

`/usr/local/bin` is on the default `$PATH` in OS X 10.10 Yosemite, but if you’re on an older version of OS X you might need to manually add it to your `$PATH`.

## Usage

    cd ~/some/web/directory
    micropache

The contents of `~/some/web/directory` will now be available at
<http://localhost:8000> (or the first available port above that).

You can specify the port you want to run the server on:

    micropache --port 4000
    micropache --port 80

Serving on ports below 1024 will require an administrator password.

Server logs will be output to the console. Press `Ctrl-C` to stop the server.
