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
sudo pacman -S vim
```
```
sudo pacman -S yay
```
### NVM:
---
```
sudo pacman -S nvm
```
```
echo 'source /usr/share/nvm/init-nvm.sh' >> ~/.bashrc`
```
```
exec $SHELL
```
```
nvm install --lts
```
```
nvm alias default + version number
```
```
npm i -g npm
```
```
npm i -g yarn
```
```
npm i -g commitizen
```
```
npm i -g localtunnel
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
      
  redis:
    image: redis:6
    restart: always
    ports:
      - 6379:6379
      
  postgres:
    container_name: postgres_container
    image: postgres
    environment:
      POSTGRES_USER: ${POSTGRES_USER:-postgres}
      POSTGRES_PASSWORD: ${POSTGRES_PASSWORD:-changeme}
      PGDATA: /data/postgres
    volumes:
       - postgres:/data/postgres
    ports:
      - "5432:5432"
    networks:
      - postgres
    restart: unless-stopped
  
  pgadmin:
    container_name: pgadmin_container
    image: dpage/pgadmin4
    environment:
      PGADMIN_DEFAULT_EMAIL: ${PGADMIN_DEFAULT_EMAIL:-pgadmin4@pgadmin.org}
      PGADMIN_DEFAULT_PASSWORD: ${PGADMIN_DEFAULT_PASSWORD:-admin}
      PGADMIN_CONFIG_SERVER_MODE: 'False'
    volumes:
       - pgadmin:/root/.pgadmin

    ports:
      - "${PGADMIN_PORT:-5050}:80"
    networks:
      - postgres
    restart: unless-stopped

networks:
  postgres:
    driver: bridge

volumes:
    postgres:
    pgadmin:
```
```
docker-compose up
```
### INSTALL:
---
* vscode
* vscode-insiders
* mongodb-altas
* slack
* telegram
* chrome



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
---

## GUAKE
* install
* ctrl+3 => guake
* keybindings:
    * toggle visibility ctrl+3
    * toggle fullscreen ctrl+3
    * split vertical/horizontal ctrl+shift++/-
    * focus ctrl+hjkl
    * resize splited terminal panel ctrl+shift+hjkl
    * left/riht tabs ctrl+alt+shift+h/l
    * move tab to left/right ctrl+alt+shift+j/k

## TILDA
Like Guake when possible and 4 instead of 3
* make guake half-up, tilda - half-bottom







