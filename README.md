passdmenu
=========

A small python frontend to [pass](http://www.passwordstore.org) wrapping [dmenu](http://tools.suckless.org/dmenu/).

Currently only tested with Python 3.4.

Example usage as [i3](http://i3wm.org) keybindings:

    bindsym $mod+Shift+i exec passdmenu.py -P -fn "Droid Sans Mono-10"
    bindsym $mod+Mod1+i exec passdmenu.py -uPt -fn "Droid Sans Mono-10"

Help:

    usage: passdmenu.py [-h] [-t] [-r] [-u] [-P] [-s STORE] [-d XDO_DELAY]
                        [-B PASS_BIN] [-D DMENU_BIN]
    
    A dmenu frontend to pass. All passed arguments not listed below, are passed to
    dmenu. If you need to pass arguments to dmenu which are in conflict with the
    options below, place them after --. Requires xclip in default mode.
    
    optional arguments:
      -h, --help            show this help message and exit
      -t, --type            Use xdotool to type the username and/or password into
                            the currently active window.
      -r, --return          Presses "Return" after typing. Forces --type.
      -u, --user            Copy/type the username.
      -P, --pw              Copy/type the password. Default, use -u -P to copy
                            both username and password.
      -s STORE, --store STORE
                            The path to the pass password store. Defaults to
                            ~/.password-store
      -d XDO_DELAY, --delay XDO_DELAY
                            The delay between keystrokes. Defaults to xdotool's
                            default.
      -B PASS_BIN, --pass PASS_BIN
                            The path to the pass binary. Defaults to /usr/bin/pass
      -D DMENU_BIN, --dmenu DMENU_BIN
                            The path to the dmenu binary. Defaults to
                            /usr/bin/dmenu
