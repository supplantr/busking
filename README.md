# busking

## dependencies

 * perl
 * File::MimeInfo ([perl module](http://search.cpan.org/dist/File-MimeInfo/))
 * procps{,-ng}

## command-line usage

    usage: xdg-open [file|protocol]

## configuration

`$HOME/.config/busking/config` takes precedence over `/etc/xdg/busking/config`.

See included `config` for an example.

### config options

The argument given to `xdg-open` is appended to `cmd`.

    @regex = cmd

is matched against the argument given to `xdg-open`.

    regex = cmd

is matched against the mimetype of the argument. Use `mimetype -b file`
(provided by File::MimeInfo) to determine mimetype.

    cmd?:terminal

signifies that `cmd` should be executed in either the current terminal or in a
new `terminal` (i.e., `terminal -e cmd`).

    #comment

is a comment. Inline comments are not valid.
