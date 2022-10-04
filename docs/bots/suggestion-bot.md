---
sidebar_position: 3
---

# Suggestion Bot

This bot is a public hosted as well as open-source Discord bot which can be found [here](https://github.com/dev-suro/suggestion-bot).

It allows users to make suggestions as well as accept and deny, and reverse the previous.

People can either use the command `/suggestions add` or `type in the channel` that the suggestion bot is setup at.

:::info Do you want to invite the bot?
https://discord.com/oauth2/authorize?client_id=320196959015141377&permissions=277562608656&scope=bot%20applications.commands
:::

Everyone who has access will be able to up-/downvote and Staff can either accept, deny or reset the suggestion.

```
Resetting means removing the accept or deny button and allowing voting again.
```

## Installation
Use `node i`

## Token
Put token in `src/botconfig/config.json`

## To start
Use `node index.js`

# Editing the `botconfig/config.json`

The:
- `"token": "TOKEN"` = self explanatory
- `"bot_name": "Suggestions"` = will change the name of the bot.
- `"loadSlashsGlobal": true` = Set it to true, when your Slash Commands are ready, false loads instant true loads slow but stable! (GLOBAL/GUILD COMMANDS, DISCORD DOCS!)
- `"slashCommandsDirs":` = Folders it scans for slashCommands

# Editing the `botconfig/embed.json`

Also sort of self explanatory.

```json
{
  "color": "#3498db",
  "wrongcolor": "#e01e01",
  "footertext": "",
  "footericon": ""
}
```

# Editing the languages!
If you want to add languages, you need to add it on 2 places.

Let's say you want to add the French translation.
- First is copying the .json file in the `src/botconfig/languages/` from lang_en.json to lang_fr.json (You can name it anything, but keep it nice!).
- After editing the file and translating it, go to `src/slashCommands/manage/` and find `line 13`, where it should say this:
```json
    {"StringChoices": { name: "language", description: "Select your preferred language", required: true, choices: [["English", "lang_en"], ["German", "lang_de"], ["Dutch", "lang_nl"], ["Russian", "lang_ru"], ["Spanish", "lang_es"]] }}
```

Now add behind `["Spanish", "lang_es"]` the `["French", "lang_fr"]`
:::caution
Make sure to add the COMMA (,) behind `["Spanish", "lang_es"]`
:::