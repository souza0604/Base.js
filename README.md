# Introdução

## aoi.js

**Olá, este repositório foi criado para te ajudar a ter uma base usando aoi.js!**

<img src = "https://aoi.js.org/assets/images/aoijs-new.png">


[![Servidor Suporte](https://img.shields.io/discord/773352845738115102?color=5865F2\&logo=discord\&logoColor=white)](https://aoi.js.org/invite) [![NPM Versão](https://img.shields.io/npm/v/aoi.js.svg?maxAge=3600)](https://www.npmjs.com/package/aoi.js) [![NPM Download s](https://img.shields.io/npm/dt/aoi.js.svg?maxAge=3600)](https://www.npmjs.com/package/aoi.js)


## Sobre

_Aoi.JS é um pacote com funções simplificadas e prontas para uso para desenvolvedores de Discord Bot desenvolverem seus próprios Discord Bots._
 _Pretendendo ser o pacote mais fácil de aprender_ 
_É rápido e flexível usar funções._ 
_Código aberto para a comunidade ❤️_

## Instalação

**Node.JS 16.6.0 ou o novo.**  

```sh-session
npm install aoi.js
```

## Configurações

```javascript
const {
	AoiClient
} = require("aoi.js");
const config = require("./config.js")
const fs = require('fs');

const client = new AoiClient(config.Bot);

require("./src/types/events/variavel.js")(client);
require("./src/types/events/status.js")(client);
require("./src/types/functions/antiCrash.js")(client);

// Handler
client.loadCommands("./src/comandos/", true);
for (const file of fs.readdirSync('./src/types/functions').filter(file => file.endsWith('.js'))) {
	require(`./src/types/functions/${file}`)(client);
}
```