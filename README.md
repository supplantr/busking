# busking

## dependencies

* perl
* File::MimeInfo ([perl module](http://search.cpan.org/dist/File-MimeInfo/))
* procps{,-ng}

## command-line usage

    usage: xdg-open [file|directory|protocol]

## configuration

__$XDG_CONFIG_HOME/busking/busking.conf__ takes precedence over __/etc/xdg/busking/busking.conf__.

See included busking.conf for a working example.

### busking.conf options:

    # comment

is a comment. Inline comments are not valid.

    terminal = app

must precede regex definitions.

    app->term

signifies that app is to be launched in the terminal defined above.

    @ regex = app

is matched against the argument given to xdg-open.

    regex = app

is matched against the mimetype of the argument.

Use __mimetype -b FILE__ (provided by File::MimeInfo) to determine mimetype.
