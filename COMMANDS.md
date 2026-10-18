# SCC folders and tools

[Back to the docs](README.md)

SCC 3.7.0 has **13 callable headers**. Individual actions appear inside the GUIs. I kept the existing tools and moved their entry points into folders.

## Headers

| Header | Opens |
| --- | --- |
| `/start` | Introduction and examples |
| `/menu` | Main menu |
| `/ship` | Ship information and tools |
| `/commodity` | Material information and buy/sell views |
| `/cargo` | Same tools and options as `/commodity` |
| `/trade` | Trade routes and calculations |
| `/mining` | Mining, refining, refinery jobs and salvage |
| `/craft` | Items, recipes and inventory |
| `/ops` | Activities and community tools |
| `/reference` | Locations, missions and public profiles |
| `/settings` | Personal preferences and identity |
| `/server` | Server manager controls |
| `/help` | Guides, status, privacy and feedback |

`/menu` is the main hub. `/start` explains how SCC works and gives a few examples. You can open a topic header directly.

All header inputs are optional. Leave them empty to browse the GUI, or use a shortcut:

| Example | Opens |
| --- | --- |
| `/ship name:Reclaimer` | Ship details |
| `/craft blueprint:Karna Rifle` | Blueprint and ingredients |
| `/craft item:Iron` | Item or material, shops and sources |
| `/commodity name:Iron view:sell` | Buyers for your Iron |
| `/cargo name:Gold view:buy` | Gold sellers you can buy from |
| `/mining resource:Iron` | Resource reports and commodity views |
| `/mining laser:Lancet` | Mining laser details |
| `/mining modifier:Surge` | Modifier details |
| `/mining laser:Lancet modifier:Surge` | Loadout check |
| `/reference location:Area18` | Location or terminal |
| `/reference mission:NAME` | Mission requirements and unlocks |
| `/reference citizen:HANDLE` | Public RSI profile |
| `/reference organization:SID` | Public RSI organization |
| `/reference system:Stanton` | Starmap system |
| `/ops activity:123` | Saved activity in this server |
| `/help topic:crafting` | Crafting guide |

Names offer autocomplete where available. Activity input also suggests titles, and stores the selected activity ID. Choose one Crafting or Reference lookup per invocation; Mining accepts a laser and modifier together for a loadout check.

`/commodity` and `/cargo` share `name` and `view` options. Views are `overview`, `buy`, `sell`, `mining`, `refinery` and `trade`. Selecting only a view opens a name prompt that keeps that choice. Commodity results include an **Open UEX** link button.

`/trade` retains optional `commodity`, `budget`, `ship` and `capacity_scu` inputs. For example, `/trade commodity:Gold budget:100000 capacity_scu:46` plans a run. A ship or capacity needs a budget; advanced filters remain in the GUI.


## Using a tool

Choose a section and an action. Forms are private. Choose a detail to enter text, search suggestions, select a choice, or pick a member/channel. Optional fields use their defaults until changed. Simple single-field lookups open immediately after you choose a match. Review forms use a button named for the action, such as **Plan an activity** or **Add materials**. A submitted form cannot run twice. For crew tools, **Operation** in the tables refers to a saved activity; the GUI labels that field **Activity**.

Game lookups follow your reply preferences and default to public. Settings, identity, reports and sensitive controls remain private. Shared crew and rescue boards are posted to their channel. Source links appear in results.

Buttons last four hours. Expiry or a normal restart retains the card; **Done** removes controls and **Close** deletes it.

## GUI actions

The tables below name the sections and actions inside each header. These are GUI paths, rather than additional slash commands. Server managers and activity owners retain their permissions; maintenance tools are restricted to me.

## /ops

### Activities

| Action | What it does | Details |
| --- | --- | --- |
| **Plan an activity** | Create an activity and post a crew signup board | Title (required); Activity (optional); Starts (optional); Meeting point (optional); Capacity (optional); Region (optional); Ships (optional); Notes (optional) |
| **Find a crew** | Find activities and open crew slots in this server | Include closed (optional) |
| **Repeat weekly** | Repeat an activity each week with a fresh crew board in this channel | Operation (required); First (required); Timezone (required) |
| **Weekly schedules** | Review weekly activities and board delivery problems in this server | No details needed |
| **Manage a weekly schedule** | Pause, resume, or remove a weekly schedule you own or manage | Schedule (required); Action (required) |
| **Set my reminder** | Request or stop a personal DM reminder for an activity you joined | Operation (required); Enabled (optional); Minutes (optional) |
| **Open an activity** | Open an activity, its crew, jobs, and material reservations | Operation (required) |
| **My reminders** | Review your activity reminders and any failed DM deliveries | No details needed |
| **Post a crew board** | Post or replace the signup board in this channel | Operation (required) |
| **Join a crew** | Join an activity or change your crew role | Operation (required); Role (optional) |
| **Leave a crew** | Leave the crew and release your unfinished jobs | Operation (required) |
| **Change activity status** | Start, complete, or cancel an activity you lead | Operation (required); Status (required) |
| **Activity from a craft plan** | Turn a crafting plan and its material shortages into a crew activity | Blueprint (required); Quantity (optional); Starts (optional); Meeting point (optional) |
| **Add a crew job** | Add a gathering, hauling, or other job to your activity | Operation (required); Title (required) |
| **Manage a crew job** | Claim, release, or complete a crew job | Operation (required); Action (required); Job (optional) |
| **Reserve materials** | Set aside shared materials so another activity cannot use them | Operation (required); Item (required); Quantity (required) |
| **Material reservations** | Release reserved materials or record that they were consumed | Reservation (required); Action (required) |

### Earnings

| Action | What it does | Details |
| --- | --- | --- |
| **View earnings** | Preview crew earnings or view a saved settlement | Operation (required) |
| **Record income or cost** | Record actual income or an expense for your crew | Operation (required); Kind (required); Amount (required); Description (required) |
| **Void an entry** | Correct the ledger by voiding an entry while preserving its history | Entry (required) |
| **Set a crew share** | Adjust a crew member’s share; all members start with equal shares | Operation (required); Member (required); Weight (required) |
| **Settle crew shares** | Save the final split and lock the ledger against accidental changes | Operation (required) |
| **Mark a share paid** | Record a payment you have already made in game | Operation (required); Member (required) |
| **Reopen a settlement** | Reopen an unpaid settlement to correct income, costs, or shares | Operation (required) |

### Rescue & escort

| Action | What it does | Details |
| --- | --- | --- |
| **Request rescue or escort** | Post a rescue or escort request with responder buttons | Kind (required); Location (required); Details (required); Expires (optional) |
| **Find open requests** | Find open rescue and escort requests in this server | No details needed |
| **Open a request** | Open a rescue or escort request and its controls | Request (required) |
| **Post a request board** | Post or replace your request board in this channel | Request (required) |
| **Update a request** | Claim, release, arrive at, resolve, or cancel a support request | Request (required); Action (required) |

### Notes

| Action | What it does | Details |
| --- | --- | --- |
| **Add a note** | Save a tip, route, workaround, procedure, or guide for this server | Title (required); Body (required); Category (optional); Tags (optional); Game version (optional); Source url (optional) |
| **Read a note** | Open one suggested community note by its ID | Note id (required) |
| **Search notes** | Search this server's note titles, text, tags, and categories | Query (required); Category (optional) |
| **Browse notes** | Browse recent community notes, optionally within one category | Category (optional); Limit (optional) |
| **Edit a note** | Edit a suggested note you wrote or manage as a server administrator | Note id (required); Title (optional); Body (optional); Category (optional); Tags (optional); Game version (optional); Source url (optional) |
| **Delete a note** | Delete a suggested note you wrote or manage as a server administrator | Note id (required) |
| **Verify a note** | Confirm that a suggested community note still works in the current patch | Note id (required) |
| **Note categories** | List the community note categories currently used in this server | No details needed |

### Debriefs

| Action | What it does | Details |
| --- | --- | --- |
| **Record a debrief** | Record a crew success or a lesson learned | Kind (required); Description (required) |
| **Read debriefs** | Read recent successes or lessons learned in this server | Kind (optional) |
| **Debrief totals** | Count this server’s recorded successes or lessons | Kind (optional) |

## /mining

### Mining

| Action | What it does | Details |
| --- | --- | --- |
| **Resource buy & sell prices** | Open commodity data including buy, sell and mining views | Resource (required) |
| **Mining lasers** | Inspect a mining laser's range, power, module slots, and modifiers | Laser (required) |
| **Mining modifiers** | Inspect a mining module or gadget and its published effects | Modifier (required) |
| **Check a loadout** | Compare a laser and up to three mining modifiers against a rock profile | Laser (required); Modifier 1 (optional); Modifier 2 (optional); Modifier 3 (optional); Rock mass (optional); Resistance (optional); Instability (optional) |
| **Find resource buyers** | Find the best cached locations to sell a raw mining resource | Resource (required) |
| **Plan a mining trip** | Build a simple mining trip plan around a resource, ship, and target amount | Resource (required); Ship (optional); Amount scu (optional); Priority (optional) |

### Refining

| Action | What it does | Details |
| --- | --- | --- |
| **Refinery methods** | Browse refinery methods and their published yield, time, and cost values | Method (optional) |
| **Compare refinery yields** | Compare refinery options for a resource by yield, speed, or cost | Resource (required); Priority (optional) |

### Refinery jobs

| Action | What it does | Details |
| --- | --- | --- |
| **Track a job** | Save a refinery job and optionally remind you when it is ready | Station (required); Material (required); Quantity (required); Ready (required); Method (optional); Remind (optional) |
| **My refinery jobs** | See refinery completion times and your pickup queue | All members (optional) |
| **Collect a job** | Mark a refinery job as picked up | Job (required) |
| **Cancel a job** | Cancel a tracked refinery job and its reminder | Job (required) |

### Salvage

| Action | What it does | Details |
| --- | --- | --- |
| **Salvage ships** | Browse ships and special variants identified for salvage gameplay | Ship (optional) |
| **Sell salvage materials** | Find cached sale routes for RMC or Construction Materials | Material (required) |
| **Plan salvage trips** | Estimate salvage cargo trips and show current material sale options | Ship (required); Material (required); Target scu (required) |

## /craft

### Items & recipes

| Action | What it does | Details |
| --- | --- | --- |
| **Search items** | Explore an item, its ingredients, shops and sources, or open the menu | Query (optional) |
| **Look up a blueprint** | Look up a crafting blueprint, ingredients, time, and unlock status | Query (required) |
| **Source ingredients** | Turn blueprint ingredients into mining, gathering, and sale-location guidance | Query (required); Quantity (optional) |
| **Plan materials** | Compare a blueprint's requirements with this server's shared inventory | Query (required); Quantity (optional) |
| **Record blueprint ownership** | Record a crafting blueprint that you own for this server's planners | Query (required) |
| **Blueprint owners** | See which members have recorded ownership of crafting blueprints | Member (optional) |

### Inventory

| Action | What it does | Details |
| --- | --- | --- |
| **Add materials** | Add crafting material to this server's shared inventory | Name (required); Quantity (required); Unit (optional); Quality (optional); Location (optional) |
| **View inventory** | List crafting materials recorded in this server's shared inventory | No details needed |
| **Remove materials** | Remove one suggested entry from this server's shared inventory | Entry id (required) |
| **Verify an entry** | Confirm that an inventory entry still matches the stock in game | Item (required) |
| **Inventory history** | See additions, consumption, removals, and verification of shared stock | Item (required) |

## /reference

### Locations

| Action | What it does | Details |
| --- | --- | --- |
| **Find a location** | Find terminals, cities, moons, planets, and their parent locations | Query (required) |

### Missions

| Action | What it does | Details |
| --- | --- | --- |
| **Find a mission** | Search current mission records by name and gameplay category | Category (required); Query (optional) |
| **Reputation paths** | Show the prerequisites, reputation, systems, and rewards for one mission | Mission (required) |
| **Mining missions** | Browse mission records related to mining, ore, and refinery gameplay | No details needed |

### Public profiles

| Action | What it does | Details |
| --- | --- | --- |
| **Public citizen profile** | Look up a public RSI citizen profile through the independent API cache | Handle (required) |
| **Public organization profile** | Look up a public RSI organization profile by Spectrum ID | Sid (required) |
| **Starmap systems** | Look up an independent cached RSI starmap system record | System (required) |

## /settings

### Preferences

| Action | What it does | Details |
| --- | --- | --- |
| **Personal preferences** | Choose your language, ship budget, pledge currency, and reply privacy | No details needed |

### Identity

| Action | What it does | Details |
| --- | --- | --- |
| **Link Citizen iD** | Connect your linked Discord and RSI accounts through Citizen iD | No details needed |
| **My linked identity** | Show your own saved Citizen iD connection | No details needed |
| **Unlink Citizen iD** | Remove your own saved RSI identity connection from SCC | No details needed |
| **RSI display on crew boards** | Choose whether your verified RSI handle appears on this server’s crew boards | Enabled (required) |

### Language

| Action | What it does | Details |
| --- | --- | --- |
| **Current language** | Show your personal, server, Discord, and resolved SCC language | No details needed |
| **Set my language** | Override automatic detection with your personal SCC language | Language (required) |
| **Use server language** | Remove your override and automatically follow server or Discord language | No details needed |

## /server

### Setup & controls

| Action | What it does | Details |
| --- | --- | --- |
| **Set an advanced value** | Set one advanced server-specific SCC value | Key (required); Value (required) |
| **View server values** | List advanced SCC settings saved for this server | No details needed |
| **Server preferences** | Set server defaults for SCC language, ship budget, currency, and reply privacy | No details needed |
| **Post a shared SCC panel** | Post a reusable SCC button panel in this server channel | No details needed |
| **Enable or disable features** | Choose which optional community workflows this server uses | Feature (optional); Enabled (optional) |

### Trade alerts

| Action | What it does | Details |
| --- | --- | --- |
| **Add a trade alert** | Notify a channel when a commodity reaches a profit-per-SCU target | Commodity (required); Minimum profit per scu (required); Channel (optional) |
| **View trade alerts** | List commodity profit alerts configured for this server | No details needed |
| **Remove a trade alert** | Remove one suggested commodity profit alert | Alert id (required) |

### Service alerts

| Action | What it does | Details |
| --- | --- | --- |
| **Subscribe to RSI status** | Post official RSI outages and recoveries in a server channel | Channel (optional) |
| **Status subscriptions** | List channels receiving official RSI status changes in this server | No details needed |
| **Stop status notifications** | Stop official RSI status notifications in a server channel | Channel (optional) |

### Usage

| Action | What it does | Details |
| --- | --- | --- |
| **Server usage** | Show private anonymous command totals for this server | Days (optional) |
| **Usage recording preference** | Enable or disable optional anonymous analytics for this server | Enabled (required) |

### Language

| Action | What it does | Details |
| --- | --- | --- |
| **Set server language** | Set the default SCC response language for this Discord server | Language (required) |
| **Reset server language** | Remove the server override and use each member's Discord language | No details needed |

### Maintenance

| Action | What it does | Details |
| --- | --- | --- |
| **Global usage** | I use this to review global anonymous command totals; restricted to me | Days (optional) |
| **SCC profile & status** | I use this to change SCC’s global Discord status and activity text; restricted to me | No details needed |
| **Refresh source data** | I use this to refresh the shared UEX, Wiki, and reference caches; restricted to me | Force (optional) |
| **Review submitted reports** | I use this to review private bug reports and suggestions; restricted to me | Report id (optional) |
| **Sync Discord headers** | I use this to resync SCC’s headers and translations with Discord; restricted to me | No details needed |

## /help

### Guides

| Action | What it does | Details |
| --- | --- | --- |
| **Read a guide** | Browse SCC features, examples, and command categories | Category (optional) |

### Status

| Action | What it does | Details |
| --- | --- | --- |
| **Connection check** | Check SCC's connection and Discord response time | No details needed |
| **SCC health** | Show Discord, provider, cache, RSI, and dashboard health | No details needed |
| **RSI service status** | Check official Star Citizen platform and game service status | No details needed |

### Feedback

| Action | What it does | Details |
| --- | --- | --- |
| **Report a bug** | Send me a private report about an SCC problem | Description (required) |
| **Suggest an idea** | Privately suggest a new SCC feature or improvement | Suggestion (required) |
| **Report incorrect game data** | Privately flag an incorrect Star Citizen value, source, or location | Subject (required); Correction (required) |

### Privacy

| Action | What it does | Details |
| --- | --- | --- |
| **Privacy information** | See exactly what SCC stores, excludes, and keeps server-isolated | No details needed |

Ship comparisons, dealerships, cargo and fuel remain in `/ship`. Route calculators and filters remain in `/trade`. The **Item shops** button is in `/craft`. Recipe ingredients and commodity results still link to their related views and UEX marketplace browsing.
