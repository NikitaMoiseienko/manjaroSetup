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






