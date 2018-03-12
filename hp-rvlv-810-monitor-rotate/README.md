# Rotate monitor on HP Revolve 810

HP Revolve 810 has pretty nice pivot monitor so the laptop is easily transformed to a tablet.

The script rotates the display and transforms the touchscreen coordinate matrix to conform screen layout.



## Install

1. Download the script. The destination might change but make sure it's included in the `$PATH`:  
   ```
   sudo wget --output-document=/usr/local/bin/monitor-rotate https://raw.githubusercontent.com/rom-melnyk/linux-scripts/master/hp-rvlv-810-monitor-rotate/monitor-rotate
   ```
1. Make the file executable; pay attention to the file destination:  
   ```
   sudo chmod a+x /usr/local/bin/monitor-rotate
   ```
1. _Optional:_ map the `monitor-rotate` command to `<Super>-O` key which corresponds to the tumbler near to the power one.  
   You can map the command to another key combination as well.



## Usage

```
$ monitor-rotate --help
   Usage:        monitor-rotate [WAY]
                 monitor-rotate [-h|--help]

   WAY           optional. One of normal, right, inverted, left.
                 Can be also n, r, i, l.
                 If omitted, next rotation clockwise is applied.

   --h, -help    Shows help screen.
```



## Tested on

* Mint 18.0+ with Cinnamon



## Thanks to:

[LinuxAppFinder](https://linuxappfinder.com/blog/auto_screen_rotation_in_ubuntu)
[mildmojo@GitHub](https://gist.github.com/mildmojo/48e9025070a2ba40795c)

