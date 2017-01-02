# The script for brightness control in Ubuntu for Lenove B- and V-series
This script helps Ubuntu users who use Lenovo B5xx laptops to solve the issue _when the brightness buttons do not work._

## Install
1. Allow writing into the file that controls the brightness.  
   As the file is reset each time on system boot, we need to do some tricks here:
   add following line to the `/etc/rc.local` before the `exit 0` line:  
   ```
   chmod a+w /sys/class/backlight/intel_backlight/brightness
   ```
2. Download the script. The destination might change but make sure it's covered by the `$PATH` variable:  
   ```
   sudo wget --output-document=/usr/local/bin/bri https://raw.githubusercontent.com/rom-melnyk/lenovo-b-brightness/master/bri
   ```
3. Make the file executable; pay attention to the file destination:  
   ```
   sudo chmod a+x /usr/local/bin/bri
   ```
4. Restart.

## Usage
Just do `bri --help` and you'll see possible options.  
**TL;DR**
Use `bri +` or `bri -` to increase or decrease the brightness; set the value directly with `bri <number>` (the `number` is usually in 1..1000).

## Convenient usage
Go to **Control panel > Keyboard > Keyboard Shortcuts > Custom Shortcuts** and bind two custom commands:
* `bri +` to the _BrightnessUp_ key (usually _Fn + &uarr;_) and
* `bri -` to the _BrightnessDown_ key (usually _Fn + &darr;_).
  * On Mint 17.1 you need to remove original _BrightnessUp_/_BrightnessDown_ keybindings (in **Keyboard Shortcuts > System > Hardware** section) to make your shourtcuts work.  
   If you cannot remove original shoorcuts, replace 'em with something you'll never use.

After you restart your desktop environment the keys should be working.

## Tested on
* Ubuntu 13.04 up to 14.10
* Mint 17.0, 17.1, 18.1 both with Cinnamon
* Fedora 25 (assiging of `bri` commands to \<IncreaseBrightness\>/\<DecreaseBrightness\> buttons does not work however command itself works fine. So you can change screen brightness from terminal)

## Credits
Roman Melnyk <email.rom.melnyk@gmail.com>

## Thanks to:
[AskUbuntu](http://askubuntu.com/) for the idea
