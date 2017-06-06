# archlinux-update-modules

This script manages /usr/lib/modules on arch linux. Just run this script
whenever you like, e.g. after an upgrade or after rebooting, in order to keep
/usr/lib/modules in a sensible state.

When being run the following tasks are done:

1. The modules directory for the running kernel is restored from the pacman cache.

2. Any old obsolete module directories are removed. Obosolete directories are
those that are neither used by the running kernel nor managed by pacman itself.

The user is asked before each filesystem change, i.e. before each sudo-command.
Please run this script as an ordinary user.
