# Anycase commands for Telegraf

Makes [Telegraf](http://telegraf.js.org/) bot commands case insensitive. For example /Command will be recognized as the same as /command.  
  
Usage:

```javascript
const AnyCase = require('telegraf-anycase-commands')

const bot = new Telegraf(process.env.BOT_TOKEN)
// Or:
const bot = new Composer()

// Then:
AnyCase.apply(bot)

// Or simply:
const bot = AnyCase.apply(new Telegraf(process.env.BOT_TOKEN))
// Or:
const bot = AnyCase.apply(new Composer())
```
