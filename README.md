# Anycase commands for Telegraf

Makes [Telegraf](http://telegraf.js.org/) bot commands case insensitive. For example /Command will be recognized as the same as /command.  
  
  
### [Installation](https://www.npmjs.com/package/telegraf-anycase-commands):
```
$ npm install telegraf-anycase-commands
or
$ yarn add telegraf-anycase-commands
```

### Usage:
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

Or if you only want to use the middleware for commands in incoming messages, without applying on commands in your code: 

```javascript
bot.use(AnyCase.lowercase)
```
Note that this will only convert incoming commands to lowercase, and commands have to be defined in lowercase in the code to match.
