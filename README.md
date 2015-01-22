# The script for brightness control in Ubuntu for Lenove B-series
This script helps Ubuntu users who use Lenovo B5** laptops to solve the issue _when the brightness buttons do not work._

## Install
```bash
# allow writing into the file that controls the brightness
sudo chmod a+w /sys/class/backlight/intel_backlight/brightness
# download the script;
# the destination might change but make sure it's covered by the $PATH variable
sudo wget --output-document=/usr/local/bin/bri https://github.com/rom-melnyk/lenovo-b-brightness/bri
```
## Usage
Just do `bri --help` and you'll see possible options.
**TL;DR**
Use `bri +` or `bri -` to increase or decrease the brightness; set the value directly with `bri <number>` (the `number` is usually in 1..1000).

## Convenient usage
Go to **Control panel > Keyboard > Keyboard Shortcuts > Custom Shortcuts** and bind two custom commands:
* `bri +` to the _BrightnessUp_ key (usually _Fn + &uarr;_) and
* `bri -` to the _BrightnessDown_ key (usually _Fn + &darr;_).
After you restart your desktop environment the keys should be working.

## Tested on
* Ubuntu 13.04 up to 14.10
* Mint 17.0, 17.1

## Credits
Roman Melnyk <email.rom.melnyk@gmail.com>

## Thanks to:
[AskUbunt](http://askubuntu.com/) for the idea
