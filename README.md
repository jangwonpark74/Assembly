# Assembly

## XMIG Install

## Machine Id Setup
sudo systemd-machine-id-setup
sudo dbus-uuidgen — ensure
cat /etc/machine-id

## Basic Font Install
sudo apt -y install x11-apps xfonts-base xfonts-100dpi xfonts-75dpi xfonts-cyrillic

## Display setup for ddd application
  DISPAY=:0 ddd <program_to_debug> 


