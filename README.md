### `WARNING`
These functions can be very dangerous! 

#### 'C302 Chromebook slow charging issue on linux`
Linux limits the charge rate to a trickle so charging goes from taking an hour to over 10. I'm not sure why are when this happens it just does. 

The current solutin is to remove the power. Suspend the device attach the power, wait a few seconds then bring the device out of sleep. Then it's back charging at full rate. 

Note: I did try the functions setting the current but I got errors and the battery disapeared completely. 

### `suspend from cAsus.bashrc`
Just stick the suspend alias into your bashrc. Then run suspend whenever you you need to plug in your charger. 


### 'THE FOLLOWING IS AT YOUR OWN RISK'
For full details visit http://kmkeen.com/cAsus-tweaks/

Notes on requirements:

### `cAsus.bl-adjust.sh`

Quadratic ramp, takes "up/down" as an argument.  Requires `xosd`, `terminus-font` and `cAsus.backlight.conf`.

### `cAsus.tablet-mode.c`

Requires `xosd`, `terminus-font` and `xorg-input`.  Build with

    gcc -O2 -lm cAsus.tablet-mode.c -o cAsus.tablet-mode

### `cAsus.vol-adjust.sh`

Takes "up/down/toggle" as an argument.  Requires `xosd`, `terminus-font` and `alsa-utils`.

### `cAsus.status.sh`

Requires `xosd` and `terminus-font`.

### `cAsus.auto-suspend.sh`

Optionally uses `xosd` and `terminus-font`.  Requires [xprintidle](https://aur.archlinux.org/packages/xprintidle/).

### `charge_current` (from `cAsus.bashrc`)

Takes a number between `0` and `3456` as an argument, setting the milliamp charge rate of the battery.  Requires `ec-utils` and a properly configured `sudoers`.

### `charge_until` (from `cAsus.bashrc`)

Takes a number between `0` and `100` as an argument, charging the battery until it reaches that percent capacity.  Charge rate may be specified with the `CHARGE_MA` environment variable.

