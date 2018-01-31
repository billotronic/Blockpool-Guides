# Blockpool Troubleshooting

## BPL-Node

### Setting the proper locale

BPL-node only supports the en_US.UTF-8 locale. To install this locale on a ubuntu/debian OS enter these commands into the console:

```sudo dpkg-reconfigure locales```

Use the DOWNARROW to navigate to en_US.UTF-8 UTF-8 and select it by pressing SPACEBAR. Press TAB to get to OK and hit ENTER

[Screen](../Screens/t.locales.dkpg.JPG)

Select en_US.UTF-8 as the system default and select OK

[Screen](../Sreens/t.locales.dkpg2.JPG)

After which it will generate your new system locale

[Screen](../Screens/t.locales.gen.JPG)

Next update your system locales by entering this in the console:

``` sudo update-locale``` 

and restart Postgresql:

```sudo service postgresql restart```

## BPL-Desktop