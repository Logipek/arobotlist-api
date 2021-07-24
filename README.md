# arobotlist-api
<a href="https://arobotlist.xyz/dc" target="_blank"><img src="https://img.devsforum.net/tr/img/h1Z2X3.png" alt="Join our discord" width="256"></a><br>
**Support:** [https://arobotlist.xyz/dc](https://arobotlist.xyz/dc) <br>
**NPM:** [npmjs.com/package/arobotlist-api](https://www.npmjs.com/package/arobotlist-api)<br>

## Installation
*If you have trouble with the installation, please feel free to visit our [discord](https://arobotlist.xyz/dc) address.*
- `npm i arobotlist-api`

```js
const arobotlist = require("arobotlist-api");
const dbl = new arobotlist("TOKEN-HERE", client);

client.on("ready", async () => {
  dbl.serverCount();
  // console.log("Server count posted")
  
  let hasVote = await dbl.hasVoted("866761155657990204");
  if(hasVote === true) {
    console.log("Voted")
  } else {
    console.log("Vote please.")
  }
  
  
  let search = await dbl.search("867516723115720716")
  console.log(search)
  /*
  {
    avatar: 'https://cdn.discordapp.com/avatars/867516723115720716/fa929b253dc99dd5770b2c22d11dd26f.webp',
    botID: '867516723115720716',
    username: 'AroServerList',
    discrim: '5807',
    shortDesc: 'Server Listing',
    prefix: 'aro!',
    votes: 31,
    ownerID: '733396325411979335',
    owner: 'Enil',
    coowners: [ '' ],
    tags: [ 'Moderation', 'Botlist', 'Music' ],
    longDesc: longDesc,
    certificate: 'Certified'
  }
  */
});
```

