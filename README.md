# My Systemd Service files

this repo contains systemd service files i write and maintain for my machines. These service files are stored and versioned here just my [dotfiles](https://github.com/fuseteam/dotfiles)

## anbox session-manager

This service file is based on the one [debian](https://salsa.debian.org/zhsj/anbox/-/blob/master/debian/anbox-session-manager.service) ships to automatically start anbox's session-manager on boot.
note that it assumes the snap version of anbox
to make use of it use the following commands:
```
sudo curl https://raw.githubusercontent.com/Fuseteam/systemd-service-files/main/anbox-session-manager.service > /etc/systemd/user/anbox-session-manager.service
systemctl --user start anbox-session-manager
systemctl --user enable anbox-session-manager
```

you can check if anbox's session-manager is running properly with 
```
systemctl --user status anbox-session-manager
```
