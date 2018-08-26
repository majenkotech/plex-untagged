Plex Untagged
=============

This is a small PERL script to add the label "Untagged" to any Plex Media
Server library items that currently have no labels assigned.

* Note: This only works for films at the moment. TV Programmes fail for some
reason.

There is currently no way to display only items that have no labels assigned
to them in Plex, so this will add a label to them for you to allow you to
find them.

First you must create a label called "Untagged", which you can do by first
manually tagging any media item (in the Sharing section) as Untagged.

Then you can run this script providing it with the name of a library, and it
will scan through that library looking for items with no labels.  It then
adds the label for you.

Usage:

    plex-untagged "My Movies"

The script is currently hard-coded for the Linux location of the Plex
database, but it's simple enough to re-point it to the location on Windows,
OS X, etc.  Just check the first couple of lines.

On Linux (and possibly other systmes too) you need to either run it as root (sudo)
or as the plex user in order to get write access to the database.

Linux Prerequisutes
-------------------

Required PERL libraries:

    apt-get install libdbi-perl
    apt-get install libdbd-sqlite3-perl
