---
title: "Come installare GSP su Ubuntu"
weight: 1
type: docs
---

Il primo passo per installare GSP consiste nell'installare MongoDB, database NoSQL usato per eseguire il login all'interno del pannello

## Installa MongoDB

### Come importare la chiave GPG
```bash
wget -qO - https://www.mongodb.org/static/pgp/server-5.0.asc | sudo apt-key add -
```

### Aggiungi i repository di MongoDB e installalo
```bash
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/5.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-5.0.list
```

e installalo

```bash
sudo apt update && sudo apt install -y mongodb-org
```

adesso avvia il servizio che gestisce MongoDB con il seguente comando

```bash
sudo systemctl start mongod
```

## Installa Docker
Questo passo è più semplice, rispetto al precedente essendo che Docker si trova già nei repository di Ubuntu.

```bash
sudo apt install docker && sudo apt install docker.io
```

una volta installato bisogna avviare il servizio con il seguente comando

```bash
sudo systemctl enable --now docker
```

## Installa NodeJS e NPM
```bash
sudo apt install nodejs npm
```

## Clona il repository da Github
```bash
git clone https://github.com/game-server-panel/game-server-panel.git
```

## Installa le dipendenze
```bash
npm run dependencies
```

# Congratulazioni, hai appena installato GSP! :D