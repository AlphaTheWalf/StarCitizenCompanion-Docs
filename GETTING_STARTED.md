# Getting started

[Back to the docs](README.md)

## Open SCC

Run `/start` for an introduction and examples, or `/menu` to open SCC’s folders. You can also use **Open my SCC panel** on a shared hub.

`/menu` is the main hub. Your preferences are optional: choose **My preferences** on the introduction, or open `/settings` → **Preferences → Personal preferences**. Preferences stay private. Game lookups default to public, while saved visibility choices still apply.

## Pick a folder

| Header | What you can do |
| --- | --- |
| `/ship` | Ship details, editions, comparisons, dealerships, cargo and fuel |
| `/commodity` | Buy/sell locations, materials, mining and refining views |
| `/trade` | Routes, budgets, calculations and report filters |
| `/mining` | Mining equipment, trip plans, refining, refinery jobs and salvage |
| `/craft` | Items, recipes, ingredients, blueprint ownership and inventory |
| `/ops` | Activities, crew, jobs, weekly schedules, earnings, rescue, notes and debriefs |
| `/reference` | Locations, missions, public citizen/org profiles and starmap |
| `/settings` | Your preferences, language and Citizen iD connection |
| `/server` | Manager settings, shared panels, notifications and usage |
| `/help` | Guides, status, privacy, feedback and data reports |

Choose a section, then an action. Detail forms stay private. Set required fields, adjust any optional fields you need, then choose **Run**. Searchable fields offer matching suggestions; member and channel fields have their own pickers. Server features and permissions still apply.

## Items, recipes, and source links

Open `/craft` → **Items & recipes → Search items** and enter `Karna Rifle`, or choose **Look up a blueprint** in **Items & recipes**. The **Item shops** button looks up NPC shop offers.
When viewing a recipe:

- Select an ingredient under **Explore an ingredient or related result** to look it up in SCC. Use **Back** to return. A commodity ingredient opens its buy/sell and mining views, with **Back to recipe** to return.
- Open **Wiki page** or **Wiki search** to read more in your browser.
- Choose **Plan materials** to compare the recipe with your server's shared inventory, or **Source materials** for gathering guidance.
- Use **Next details** and **More related** when a recipe has more information than fits on one page.

You'll also find source links in ship, trade, mining, refinery, mission, salvage, location, and public RSI results. **Wiki data record** opens the original data behind a result. Wiki search links are used when SCC doesn't have a direct article link.

If SCC can't find a recipe or price, that doesn't mean the item is unavailable in game. Wikelo barter rewards are shown separately from crafting recipes. Blueprint browsing works in DMs; shared inventory planning needs a server.

## Commodities and materials

Try `/commodity name:Gold`. The first card shows both buy and sell locations. Choose **Buy locations**, **Sell locations**, **Mining**, **Refining** or **Trade routes** below it. Raw ore and refined cargo keep separate quotes; the related-material dropdown lets you switch between them. Commodity and ore prices use aUEC per SCU.

Ship lists put shared source references at the bottom, with a Wiki link beside each ship. A dealership’s location appears once above its offers.

## Find a player seller or buyer

Weapon and material results can suggest UEX player sellers. Open **UEX marketplace** to browse **Find sellers** or **Find buyers**. You can filter by price, quality, and location.

Select the currency and unit before comparing prices. SCU, cSCU, boxes, and individual items are listed separately; SCC doesn't convert between them. Quality uses UEX's 0–1000 scale. Listings with unknown quality are excluded when you set a minimum.

Player listings are separate from NPC shop prices. They refresh on demand and may be cached for up to five minutes. If UEX is unavailable, a recent cached listing may appear with a warning. Prices, stock, and availability come from traders and may have changed.

Open the UEX listing to contact a seller or buyer. SCC doesn't place orders, publish listings, or send messages to traders. You don't need a UEX account key to browse.

## Keep the channel tidy

Searches and topic changes usually update the same menu. **Close** removes it. **Done** leaves the card without buttons and keeps its existing privacy setting.

Controls stay active for four hours. When they expire or SCC restarts, the result stays in chat and its temporary controls are removed where possible. Open its folder again to browse further. Discord controls how long private replies remain visible; public results are the better choice when you want to revisit them later.

Read **Home → What’s new** or the [changelog](CHANGELOG.md) for recent changes.

## Private or public replies

**Private** replies are visible only to you. **Public** replies can be read by anyone with access to the channel. Even when public, your personal menu can only be used by you; others can open their own.

Account linking, settings, reports, reminders, subscriptions, and sensitive controls stay private. Crew and rescue boards are shared in their channel so other members can join. Reply preferences change SCC's responses, not how Discord displays the command you entered.

Your personal settings apply across servers. Choose **Use default** to follow a server's settings. Language falls back to your Discord language when no preference is set. Some advanced forms and explanations still use English.

## Prices and ship budgets

- In-game purchase and rental prices use **aUEC**.
- Real-money pledge prices are separate. Choose USD, EUR, GBP, or hide them. If a source doesn't have your currency, SCC labels the original currency; it doesn't calculate an exchange rate.
- Ship budget filters use available purchase quotes. Set it to zero for any budget. Searching for a ship by name ignores the budget so you can still view it.

Check the date and game version shown before buying or trading. Update times vary by source, and a listed price doesn't guarantee current stock. SCC doesn't transfer currency.

## Join a crew

Open `/ops` → **Activities → Find a crew**, or reach it through **Ops & community** in `/menu`, choose an activity, and pick a role. Check the board for jobs and use **Remind me** if you'd like a private reminder. Leaving the crew cancels it. See [Community activities](COMMUNITY_ACTIVITIES.md) for planning your own session.

## Link your RSI identity, if you want

SCC works without account linking. Citizen iD verifies your RSI identity and matches it to the Discord account you've linked there.

Open `/settings` → **Identity → Link Citizen iD**, then finish signing in on the account page. **My linked identity** shows your saved result privately. It reflects your last sign-in, so it isn’t a continuous identity check.

**RSI display on crew boards** lets you choose **Yes** or **No** for this server. Display is off by default and set separately for each server. **Unlink Citizen iD** removes the connection. Read the [privacy policy](PRIVACY_POLICY.md) for details.

Everyday features work inside Discord. Account linking opens a sign-in page. I use a separate private dashboard to maintain SCC; you don't need it to use the bot.
