---
title: "How to create your first account"
weight: 2
type: docs
---

Once GSP is installed, you need to create an account to access it, to create one just go to the installation folder with

```bash
cd game-server-panel
```

install the modules needed to create the account with

```bash
npm install
```

give the command

```bash
npm run createuser
```

and finally enter your data

{{<alert title = "Note">}}
All the data entered will be saved ONLY in the database on which the GSP backend is hosted.
Before being inserted into the database, all data is encrypted with the sha256 algorithm in order to have greater security
{{</ alert>}}