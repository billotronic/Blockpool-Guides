# How to set LOCALE

BPL-node only supports the en_US.UTF-8 locale. To see what your current system LOCALE is set to:

```locale```

If you locale is already set to en_US it will look similiar to this:

```
$ locale
LANG=en_US.UTF-8
LANGUAGE=
LC_CTYPE="en_US.UTF-8"
LC_NUMERIC="en_US.UTF-8"
LC_TIME="en_US.UTF-8"
LC_COLLATE="en_US.UTF-8"
LC_MONETARY="en_US.UTF-8"
LC_MESSAGES="en_US.UTF-8"
LC_PAPER="en_US.UTF-8"
LC_NAME="en_US.UTF-8"
LC_ADDRESS="en_US.UTF-8"
LC_TELEPHONE="en_US.UTF-8"
LC_MEASUREMENT="en_US.UTF-8"
LC_IDENTIFICATION="en_US.UTF-8"
LC_ALL=

```

In which case you can precede to install BPL-node

If your LOCALE is anything other en_US it must be changed in order for BPL-node to function. To install this locale on a ubuntu/debian OS enter these commands into the console:

```sudo locale-gen en_US.UTF-8```

then

```update-locale LANG=en_US.UTF-8```

For the changes to take effect reboot the system then recheck your LOCALE in console to ensure it is now set to en_US.

