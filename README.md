# manjaroSetup
`

1. sync Firefox
2. reverse scroll for touchpad
3. allow all packages
```
sudo pacman -Syy
```
5. install gnome-terminal
6. ctrl+alt+t `gnome-terminal`
```
sudo pacman -S vim`
```
```
sudo pacman -S yay
```
### NVM:
---
```
sudo pacman -S nvm`
```
```
echo 'source /usr/share/nvm/init-nvm.sh' >> ~/.bashrc`
```
```
exec $SHELL`
```
```
nvm install --lts`
```
```
nvm alias default ` + version number
```
```
npm i -g npm`
```
```
npm i -g yarn
```
```
npm i -g commitizen
```
### DOCKER:
---
```
sudo pacman -Syu
```
```
sudo pacman -S docker
```
```
sudo systemctl start docker.service
```
```
sudo systemctl enable docker.service
```
```
sudo usermod -aG docker $USER
```
```
sudo pacman -S docker-compose
```
```
reboot
```

##### images for mongodb and redis:
---
```
vim docker-compose.yml
```
```
version: '3.1'

services:

  mongodb:
    image: mongo
    restart: always
    ports:
      - 27017:27017
```
```
docker-compose up
```
```
vim docker-compose.yml
```
```
version: '3.1'

services:
  redis:
    image: redis:6
    restart: always
    ports:
      - 6379:6379
```
```
docker-compose up
```
### INSTALL:
---
* vscode
* vscode-insiders
* mongodb-altas
* 




## WORKSPACES KEYS:
* windowmanager:
    * move window to workspace
      * super+alt+hjkl
    * tile window
      * super+arrows
    * move to workspace
      * super+hjkl
    * add/delete (near) workspace
      * super(+alt)+insert/delete
    * stick window
      * alt+super+pause
* window buttons:
    * show handle
    * allow drag-drop


# GIT + ssh
```
git config --global user.name "nik"
```
```
git config --global user.email "volsknik@gmail.com"
```
```
sudo pacman -S xclip
```
```
ssh-keygen -t ed25519 -C "gitlabForS@akura"
```
```
xclip -sel clip < ~/.ssh/id_ed25519.pub
```
```
ssh -T git@gitlab.example.com
```






