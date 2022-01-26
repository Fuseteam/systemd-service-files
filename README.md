# My Systemd Service files

this repo contains systemd service files i write and maintain for my machines. These service files are stored and versioned here just my [dotfiles](https://github.com/fuseteam/dotfiles)

## anbox session-manager

This service file is based on the one [debian](https://salsa.debian.org/zhsj/anbox/-/blob/master/debian/anbox-session-manager.service) ships to automatically start anbox's session-manager on boot.
note that it assumes the snap version of anbox

to make use of it download by right clicking below and selecting "save link as"

[![download](https://github.com/Fuseteam/systemd-service-files/blob/main/images/download.jpg)](https://raw.githubusercontent.com/Fuseteam/systemd-service-files/main/anbox-session-manager.service)

save it in your downloads folder and run the following commands:
```
sudo mv ~/Downloads/anbox-session-manager.service /etc/systemd/user/anbox-session-manager.service
systemctl --user enable --now anbox-session-manager
```

you can check if anbox's session-manager is running properly with 
```
systemctl --user status anbox-session-manager
```

## Synapse

synapse is a semantic launcher that takes advantage of zeitergeist to open recent files and to launch applications


to make use of it download by right clicking below and selecting "save link as"

[![download](https://github.com/Fuseteam/systemd-service-files/blob/main/images/download.jpg)](https://raw.githubusercontent.com/Fuseteam/systemd-service-files/main/synapse.service)

save it in your downloads folder and run the following commands:
```
sudo mv ~/Downloads/synapse.service /etc/systemd/user/synapse.service
systemctl --user enable --now synapse
```

if synapse is runnning properly you should be able to trigger it with it's shortcut, that is ctrl+space
