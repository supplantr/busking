# busking

## dependencies

 * perl
 * File::MimeInfo ([perl module](http://search.cpan.org/dist/File-MimeInfo/))
 * procps{,-ng}

## command-line usage

    usage: xdg-open [file|directory|protocol]

## configuration

`$HOME/.config/busking/config` takes precedence over `/etc/xdg/busking/config`.

See included `config` for a working example.

### config options

    # comment

is a comment. Inline comments are not valid.

    terminal = app

must precede regex definitions.

    app->term

signifies that app is to be launched in the terminal defined above.

    @ regex = app

is matched against the argument given to `xdg-open`.

    regex = app

is matched against the mimetype of the argument.

**note:** Use `mimetype -b FILE` (provided by File::MimeInfo) to determine
          mimetype.
