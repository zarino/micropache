# micropache

Starts an Apache webserver in the current directory, accessible at
http://localhost on port 8000 (or first available port above that).

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

If you need to run on port 80 (eg: for hassle-free WordPress hosting)
pass the `--port80` command line argument. The `httpd` process will be
run with `sudo`. You will be asked for an administrator password.

Server logs will be output to the console. Press `Ctrl-C` to stop the server.
