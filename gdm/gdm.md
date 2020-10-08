# GDM Configuration

1. To enable GDM autologin, add the following lines to `/etc/gdm3/daemon.conf`:
```
# Enable automatic login for user
[daemon]
AutomaticLoginEnable = true
AutomaticLogin       = user
```

2. Set sway as the default session. Edit `/var/lib/AccountsService/users/user` and set:
```
XSession=sway
``` 