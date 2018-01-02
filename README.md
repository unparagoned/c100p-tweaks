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

