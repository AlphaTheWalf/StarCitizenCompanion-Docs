# Server setup

[Back to the docs](README.md)

## Get your server started

1. [Invite SCC](https://discord.com/oauth2/authorize?client_id=1335286329931595776) and choose your server.
2. Give SCC **View Channel**, **Send Messages**, and **Embed Links** in the channels you'll use. **Read Message History** lets it find and update existing boards; **Attach Files** is needed for file replies. These features don't need Administrator permission.
3. Open `/server` → **Setup & controls → Server preferences** to choose the server's language, pledge currency, ship budget, and private or public replies. Members can override these in `/settings` → **Preferences → Personal preferences**.
4. Open `/server` → **Setup & controls → Post a shared SCC panel** to post a shared hub. Pin it if you'd like members to find it easily. Each person opens their own menu from it, and the hub works after restarts.
5. Use `/server` → **Setup & controls → Enable or disable features** to choose which features are available.

You'll need **Manage Server** permission to set up SCC or create a hub in your server. I also have access to these controls as SCC's maintainer. Discord's integration and channel permissions still apply.

Personal results remain after their controls expire or SCC restarts. Members can use **Close** to remove one or **Done** to remove only its controls. Shared hubs, crew boards, support boards, and saved records stay in place. SCC only deletes its own result when its owner presses Close.

## Choose your features

| Setting | Features |
| --- | --- |
| `operations` | Activities, crew, jobs, materials, and earnings |
| `refinery_jobs` | Refinery tracking and reminders |
| `support` | Rescue and escort requests |
| `community` | Community debriefs |

To turn off support requests, open `/server` → **Setup & controls → Enable or disable features**, set **Feature** to **support**, set **Enabled** to **No**, then choose **Run**. Turning a feature off doesn't delete its saved records.

Activity leaders and managers control their activities, reservations, and earnings settlements. Members manage their own participation and claimed jobs. Seeing a button doesn't give someone permission to change another person's records.

Server settings and shared records stay within that server. Personal preferences and account links follow the member, while permission to show an RSI handle is set separately for each server.

## Other server tools

- `/server` → **Trade alerts → Add a trade alert** sets up channel notifications for reported profitable routes.
- `/server` → **Service alerts → Subscribe to RSI status** subscribes a channel to official RSI service-status updates.
- `/server` → **Usage → Server usage** shows usage totals. In `/server` → **Usage → Usage recording preference**, set **Enabled** to **No** and choose **Run** to stop new usage records for your server; existing records remain until removed or pruned.
- `/server` → **Language → Set server language** and `/server` → **Setup & controls → Set an advanced value** offer more settings. Use `/server` → **Setup & controls → Server preferences** for the usual preferences.

See [Commands](COMMANDS.md) for the options. I manage SCC's API keys, so you don't need to provide any to set it up in your server.

## SCC's status and activity

I use `/server` → **Maintenance → SCC profile & status** to change SCC's profile across every server, so that command is restricted to me. It supports Online, Idle, Do not disturb, and Appear offline, plus Watching, Playing, Listening, Streaming, or no activity. Settings survive restarts. Changes need to be at least five seconds apart; appearing offline doesn't disconnect the bot.

The default activity directs people to `/start`. Activity text changes the profile and doesn't send an announcement. Streaming requires a supported Twitch or YouTube URL. Discord's [Streamer Mode](https://support.discord.com/hc/en-us/articles/218485407-Streamer-Mode-101) is a separate setting in the Discord app. SCC doesn't monitor member status.

## If something isn't working

Check channel and integration permissions, then try `/help` → **Status → Connection check** and `/help` → **Status → SCC health**. If a board stopped updating, restore SCC's access and ask its leader to repost it with `/ops` → **Activities → Post a crew board** or `/ops` → **Rescue & escort → Post a request board**. Use `/server` → **Setup & controls → Post a shared SCC panel** to replace a removed hub.

Report a problem with `/help` → **Feedback → Report a bug** or a [GitHub issue](https://github.com/AlphaTheWalf/StarCitizenCompanion-Docs/issues/new/choose). For account, data, or security concerns, [contact me privately](SECURITY.md).
