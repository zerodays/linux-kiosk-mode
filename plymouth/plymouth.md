# Plymouth Configuration

1. Install packages `plymouth` and `plymouth-themes`.
2. Add `splash` keyword to `GRUB_CMDLINE_LINUX_DEFAULT` flag inside `/etc/default/grub`.
3. Install any theme by copying its directory to `/usr/share/plymouth/themes/`.
4. Configure plymouth tho use the new theme:
```
# list themes
plymouth-set-default-theme -l

# set new theme
plymouth-set-default-theme -R [theme name]
```