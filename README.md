ARCH-DAEMON (SHORT: DAEMON) README
=======================================================================

**(Arch-)Daemon** manipulates services on an Arch Linux system.

Lets say I like to start or stop daemons manually a lot, for example if I never
use `cups` or `httpd` or `mysql`. Normally I'd have to then do this:

    sudo /etc/rc.d/cups start
    sudo /etc/rc.d/httpd start
    sudo /etc/rc.d/mysqld start

It would be nice if we could simplify this, and indeed, this is the niche that
**Arch-Daemon** tries to fill. With Arch-Daemon we can then do this:

    sudo daemon cups httpd mysqld

and all of those services will be started in exactly the same way that we
did it above.


### Usage (taken from `daemon --help`)
    Usage: daemon [-s|-t|-r|-ts] <daemons>
    If no flag is specified, -s is assumed
      --list         -l   list started daemons
      --available    -a   list all available daemons
      --start        -s   start
      --stop         -t   stop
      --restart      -r   restart
      --stop-start   -ts  stop and then start
      --help         -h   display this help
      --version      -v   display the version
      --quit-on-fail -q   quit when a services does not exist
                          or when a service quits with an error

### Other Examples
Sometimes you might want to instead of restarting (for whatever reason)
stop a bunch of services and then start them. In that case you can run
for example:

    $ daemon -ts httpd mysqld
    :: Stopping Apache Web Server                                  [DONE] 
    :: Stopping MySQL Server                                       [DONE] 
    :: Starting Apache Web Server                                  [DONE] 
    :: Starting MySQL Server                                       [DONE] 


### Tips
I like to make `sudo daemon` run without a password, in which case I can also
make an alias for myself:

    alias daemon="sudo daemon"

Then you can save yourself even more typing! ;)

