# micropache

Starts an Apache webserver in the current directory, accessible at http://localhost on port 80.

Built to quickly run PHP sites on a Mac, using the system Apache binary, but without messing with virtualhosts and the default system config files.

## Installation

    cd /usr/local/bin
    git clone https://github.com/zarino/micropache.git

`/usr/local/bin` is on the default `$PATH` in OS X 10.10 Yosemite, but if you’re on an older version of OS X you might need to manually add it to your `$PATH`.

## Usage

    cd ~/some/web/directory
    micropache

Micropache will ask for your root password, since the Mac’s built-in `httpd` daemon must run as root.

Server logs will be output to the console. Press `Ctrl-C` to stop the server.