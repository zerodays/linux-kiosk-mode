# Hide Grub

Edit `/etc/default/grub` and add:
```
GRUB_DEFAULT=0
GRUB_TIMEOUT=0
GRUB_TIMEOUT_STYLE=hidden
GRUB_HIDDEN_TIMEOUT=0
GRUB_HIDDEN_TIMEOUT_QUIET=true
GRUB_DISABLE_OS_PROBER=true
GRUB_RECORDFAIL_TIMEOUT=0
GRUB_BACKGROUND=""
```

**NOTE**: Remember to leave `GRUB_DISTRIBUTOR` and `GRUB_CMDLINE_LINUX_DEFAULT` alone. Check for any duplicates.

Then run `update-grub` and reboot.