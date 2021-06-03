# manjaroSetup
`

1. sync Firefox
2. reverse scroll for touchpad
3. allow all packages
4. `sudo pacman -Syy`
5. install gnome-terminal
6. ctrl+alt+t `gnome-terminal`
7. `sudo pacman -S vim`
8. `sudo pacman -S yay`
9. NVM:
  * `sudo pacman -S nvm`
  * `echo 'source /usr/share/nvm/init-nvm.sh' >> ~/.bashrc`
  * `exec $SHELL`
  * `nvm install --lts`
  * `nvm alias default ` + version number
10. DOCKER:
  * `sudo pacman -Syu`
  * `sudo pacman -S docker`
  * `sudo systemctl start docker.service`
  * `sudo systemctl enable docker.service`
  * `sudo usermod -aG docker $USER`
  * `pacman -S docker-compose`
  * `reboot`




