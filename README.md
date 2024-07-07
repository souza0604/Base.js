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

## Installation

**Node.JS 16.6.0 or newer is required.**  

```sh-session
npm install aoi.js
```

## Setting up

```javascript
const aoijs = require("aoi.js")

const bot = new aoijs.AoiClient({
  token: "DISCORD BOT TOKEN",
  prefix: "DISCORD BOT PREFIX",
  intents: ["GUILDS", "GUILD_MESSAGES"]
})
//Events
bot.onMessage()

//Command Example (ping)
bot.command({
  name: "ping",
  code: `
  Pong! $pingms 🏓
  `
});

//Ready Event
bot.readyCommand({
  channel: "",
  code: `
  $log[Ready on $userTag[$clientID]]
  `
});

//Slash Command Example (ping)
//$createApplicationCommand[$guildID;ping;Pong!;true;slash]
bot.interactionCommand({
  name: "ping",
  prototype: 'slash',
  code: `
  $interactionReply[Pong! $pingms 🏓]
  `
});
```
### Would you want to contribute? 

We would like to build our documentary along with you to make it betters to everyone!

Before contributing please read our [Contribution Guidelines](https://github.com/aoijs/documentation/blob/v5/.github/docs/contributing.md).

## Links
- [Website](https://aoi.js.org)
- [NPM](https://www.npmjs.com/package/aoi.js)
- [Github](https://github.com/AkaruiDevelopment/aoi.js)
- [Discord Server](https://discord.gg/HMUfMXDQsV)
- [Documentation](https://aoi.js.org/docs/)