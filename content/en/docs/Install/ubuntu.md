---
title: "How to install GSP on Ubuntu"
weight: 1
type: docs
---

The first step to install GSP is to install MongoDB, the NoSQL database used to log into the web panel

## Install MongoDB

### Import GPG key
```bash
wget -qO - https://www.mongodb.org/static/pgp/server-5.0.asc | sudo apt-key add -
```

### Add MongoDB repos and install it
```bash
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/5.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-5.0.list
```

and then 

```bash
sudo apt update && sudo apt install -y mongodb-org
```

now you have to start mongod.service with the following command

```bash
sudo systemctl start mongod
```


## Install Docker
This step is simpler than the previous one since Docker is already in the Ubuntu repositories.

```bash
sudo apt install docker && sudo apt install docker.io
```

once installed start docker service

```bash
sudo systemctl enable --now docker
```

## Install NodeJS and NPM
```bash
sudo apt install nodejs npm
```

## Clone git repository
```bash
git clone https://github.com/game-server-panel/game-server-panel.git
```

## Install dependencies
```bash
npm run dependencies
```

# Congratulations, you've just installed GSP! :D