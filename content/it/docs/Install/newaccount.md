---
title: "Come creare il primo account"
weight: 2
type: docs
---

Una volta installato GSP è necessaria la creazione di un account per potervi accedervi, per crearne uno basta recarsi nella cartella di installazione con

```bash
cd game-server-panel
```

installare i moduli necessari alla creazione dell'account con 

```bash
npm install
```

dare il comando 

```bash
npm run createuser
```

e infine inserire i propri dati

{{< alert title="Nota" >}}
Tutti i dati inseriti verranno salvati SOLAMENTE nel database sui cui viene ospitato il backend di GSP.
Tutti i dati prima di essere inseriti nel database vengono criptati con l'algoritmo sha256 al fine di avere maggior sicurezza
{{< /alert >}}
