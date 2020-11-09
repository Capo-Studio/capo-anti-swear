# capo-anti-swear

A package for discord anti-swear support a lot of languages.

## Installation

    npm install capo-anti-swear

## YT Video

[Link](https://youtu.be/I0F2vtgzVvU)

## Usage
```
const AntiSwear = require("capo-anti-swear"),
  filterAR = new AntiSwear("ar"),
  filterEN = new AntiSwear("en");
const Discord = require("discord.js");
const client = new Discord.Client();
client.on("ready", () => {
  console.log(`Logged in as ${client.user.tag}!`);
});

client.on("message", async message => {
  if (!message.guild || !message.content) return;
  if (filterAR.check(message.content) || filterEN.check(message.content)) {
    return message.delete();
  }
});

client.login("token");
   ```

#### Supported Languages

`ar` - `cs` - `da` - `de` - `en` - `eo` - `es` - `fa` - `fi` - `fil` - `fr` - `hi` - `hu` - `it` - `ja` - `kab` - `ko` - `nl` - `no` - `pl` - `pt`

#### Filter

Filter constructor.

**Parameters**


-    `list` **[array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)** Instantiate filter with custom list
    

##### isProfaneLike

Determine if a single word is profane or looks profane.

**Parameters**

-   `word` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** String to evaluate for profanity.

##### replaceWord

Replace a word with placeHolder characters;

**Parameters**

-   `string` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** String to replace.

##### clean

Evaluate a string for profanity and return an edited version.

**Parameters**

-   `string` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Sentence to filter.

##### count

Count a string for profanity and return the count.

**Parameters**

-   `string` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Sentence to filter.

##### check

Check a string for profanity and return an Boolean value.

**Parameters**

-   `string` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** Sentence to filter.



