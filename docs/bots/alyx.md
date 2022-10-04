---
sidebar_position: 2
---

# Alyx

:::tip
If you want access to this bot, please ask fayevr#0001 on Discord.
:::

This bot is a global `reporting` and `banning` bot. It's source is private, because of multiple reasons.
However, I would be willing to show how the bot is setup and help you with your project!

Alyx is a public bot, in where people can report a user violating a rule, for example Discord ToS.

Moderators will be able to either accept the report, and the bot will ban the user from their server, or deny the report, and nothing will happen.

:::caution
Every report needs a valid proof with a link, for example [Imgur](https://imgur.com). Otherwise the report will fail and not be sent.
:::

In the future, this bot will also have Dashboard with a list of banned users, and the ability to ban users via the Dashboard.
Keep in mind, that the dashboard is not publicly accessable and will only be allowed for users that we allow.

# Editing the config.json

Bot developers have access to global settings, like unbanning as well as blacklisting users/servers. Here is also the activity as well as the bot client id.
```json
"bot": {
    "developers": [
        "196742608846979072",
        "196846656480739328"
    ],
    "activity": {
        "type": "WATCHING",
        "status": "reports."
    },
    "id": ""
},
```

The database section is for MongoDB
```json
"database": {
    "host": "",
    "username": "",
    "password": ""
},
```

:::note
Each command is setup as a `plugin`, meaning you can easily remove or add slash commands.
:::

The help command is setup at the very end of the `plugin` section. As well as the description it says.
```json
"messageContent": {
    "content": ":wave:",
    "embeds": [
        {
            "description": "Hello!\n\nI am Alyx, a global reporting and Banning system.\n\nI use SLASH commands '/', so to report people, please use /report.\n\nThis bot only gets added to specific servers that the developers trust enough to report users.\n\nIf you would like to report a certain user for abusing the power of the /report command, please contact one of the developers in the [Support Discord Server](https://discord.gg/eYYwNP6nwn).\n\nHave any more questions? Feel free to ask your fellow Admins or contact us directly!",
            "color": 65535
        }
    ]
}
```