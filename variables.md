---
description: >-
  Variables allow you to easily add information about the voter, bot, server and
  more into your custom vote embeds
---

# Variables

## Variable Formatting

Variables require **lowercase** letters and must be surrounded with `{}`.

#### Incorrect Variable Formatting

{% code title="Missing {}" %}
```
tag
```
{% endcode %}

{% code title="Contains uppercase letters" %}
```
{Tag}
```
{% endcode %}

{% code title="Contains a space" %}
```
{total votes}
```
{% endcode %}

#### Correct Variable Formatting

```
{tag}
{total_votes}
```

## TagScript  V1

{% hint style="danger" %}
TagScript V1 is now deprecated and will not work inside of Vote Messages anymore. If you notice tags not getting replaced, make sure to check its a TagScript V2 variable
{% endhint %}

### Text Variables

The following variables are supported in all embed fields except image & field name & values. Please see below for a list of supported variables for images&#x20;

<table><thead><tr><th width="141">Name</th><th>Description</th><th width="81" data-type="checkbox">Bots</th><th width="92" data-type="checkbox">Servers</th></tr></thead><tbody><tr><td>tag</td><td>Voters username &#x26; tag</td><td>true</td><td>true</td></tr><tr><td>id</td><td>Voters user ID</td><td>true</td><td>true</td></tr><tr><td>mention</td><td>Mentions the voter</td><td>true</td><td>true</td></tr><tr><td>total_votes</td><td>Voters total votes for the bot/server</td><td>true</td><td>true</td></tr><tr><td>monthly_votes</td><td>Voters votes for the bot/server this month</td><td>true</td><td>true</td></tr><tr><td>platform</td><td>Platform the bot/server was voted on</td><td>true</td><td>true</td></tr><tr><td>link</td><td>Link to vote for the bot/servre</td><td>true</td><td>true</td></tr><tr><td>date</td><td>Current date</td><td>true</td><td>true</td></tr><tr><td>role</td><td>Role given to voters</td><td>true</td><td>true</td></tr><tr><td>duration</td><td>Duration vote role is kept for</td><td>true</td><td>true</td></tr><tr><td>guild_name</td><td>Name of the voted or current server</td><td>true</td><td>true</td></tr><tr><td>guild_id</td><td>ID of the voted or current server</td><td>true</td><td>true</td></tr><tr><td>bot_name</td><td>Name of the voted bot</td><td>true</td><td>false</td></tr><tr><td>bot_mention</td><td>Mentions the voted bot</td><td>true</td><td>false</td></tr></tbody></table>

### Image Variable List

The following variables are only supported for the author, footer & main image fields of the vote embed

<table><thead><tr><th width="135">Name</th><th>Description</th><th width="74" data-type="checkbox">Bots</th><th width="100" data-type="checkbox">Servers</th></tr></thead><tbody><tr><td>user_avtar</td><td>Voters icon</td><td>true</td><td>true</td></tr><tr><td>app_icon</td><td>Icon of the voted bot/server</td><td>true</td><td>true</td></tr></tbody></table>



## TagScript V2

TagScript V2 is our current system for variables & dynamic content in messages. TagScript V1 only supported text variables and a few image variables, with inconsistent naming and formats. TagScript V2 fixes those issues

All V2 tags has a Top Level Tag, followed by a period (`.`) and then a property. This makes it much easier to see what a tag is for and gives access to many more tags

In addition to those improvements, TagScript V2 adds more types of tag: **Colour**, **Link** & **Date** tags. Some can be used with the existing setup commands & embed customisation in Discord, and some, such as link tags, will only be useful when customising the extra fields available in the [Dashboard](https://dashboard.votemanager.xyz)

### Top Level Tags

Some Top Level Tags have replaced values, usually mentions, if no additional property is specified

<table><thead><tr><th width="144">Tag</th><th>Description</th><th>Value</th></tr></thead><tbody><tr><td><code>voter</code></td><td>Contains information about the user who voted</td><td><code>&#x3C;@760170825629958184></code></td></tr><tr><td><code>guild</code></td><td>Contains information about the guild the tracker is setup in</td><td></td></tr><tr><td><code>app</code></td><td>Contains information about the bot that was voted for</td><td><code>&#x3C;@959699003010871307></code></td></tr><tr><td><code>platform</code></td><td>Contains information about the platform that the vote was on</td><td></td></tr><tr><td><code>rewards</code></td><td>Contains information about the rewards given</td><td></td></tr><tr><td><code>miki</code></td><td>Contains information about the rewards given by Miki, if setup</td><td></td></tr></tbody></table>

{% hint style="warning" %}
If a server was voted for, then any `app` tags will be replaced with nothing, or may not the replaced at all. The `guild` tag will always be replaced with the data of the server the vote message is to be sent in, even if the target was a bot
{% endhint %}

### `voter` Properties

<table data-full-width="true"><thead><tr><th width="191">Tag</th><th>Description</th><th data-type="select" data-multiple>Valid For</th></tr></thead><tbody><tr><td><code>id</code></td><td>ID of the voter</td><td></td></tr><tr><td><code>username</code></td><td>Username of the voter</td><td></td></tr><tr><td><code>global_name</code></td><td>Voter's global display name, falls back to <code>username</code> if not set</td><td></td></tr><tr><td><code>display_name</code></td><td>Voter's nickname, or <code>global_name</code> if not set</td><td></td></tr><tr><td><code>votes</code></td><td>Voter's total votes</td><td></td></tr><tr><td><code>created_at</code></td><td>Date voter's account was created on</td><td></td></tr><tr><td><code>joined_at</code></td><td>Date the voter joined the server</td><td></td></tr><tr><td><code>avatar_url</code></td><td>Voter's avatar</td><td></td></tr><tr><td><code>banner_url</code></td><td>Voter's banner</td><td></td></tr><tr><td><code>accent_color</code></td><td>Voter's profile accent colour. Will fallback to default embed if not set</td><td></td></tr><tr><td><code>banner_color</code></td><td>Voter's profile banner colour. Will fallback to default embed if not set</td><td></td></tr></tbody></table>

### `guild` Properties

<table data-full-width="true"><thead><tr><th width="194">Tag</th><th>Description</th><th data-type="select" data-multiple>Valid For</th></tr></thead><tbody><tr><td><code>id</code></td><td>ID of the server</td><td></td></tr><tr><td><code>name</code></td><td>Name of the server</td><td></td></tr><tr><td><code>created_at</code></td><td>Date server was created</td><td></td></tr><tr><td><code>icon_url</code></td><td>Server icon</td><td></td></tr><tr><td><code>banner_url</code></td><td>Server banner</td><td></td></tr></tbody></table>

### `app` Properties

<table data-full-width="true"><thead><tr><th width="197">Tag</th><th>Description</th><th data-type="select" data-multiple>Valid For</th></tr></thead><tbody><tr><td><code>id</code></td><td>ID of the voted bot</td><td></td></tr><tr><td><code>username</code></td><td>Name of the voted bot</td><td></td></tr><tr><td><code>created_at</code></td><td>Date the voted bot was made</td><td></td></tr><tr><td><code>joined_at</code></td><td>Date the voted bot joined the server</td><td></td></tr><tr><td><code>avatar_url</code></td><td>Avatar of the voted bot</td><td></td></tr></tbody></table>

### `platform` Properties

<table data-full-width="true"><thead><tr><th width="202">Tag</th><th>Description</th><th data-type="select" data-multiple>Valid For</th></tr></thead><tbody><tr><td><code>name</code></td><td>Name of the platform voted on</td><td></td></tr><tr><td><code>next_vote.hours</code></td><td>Relative time until the user can vote (e.g. <strong>in 6 hours</strong>)</td><td></td></tr><tr><td><code>next_vote</code></td><td>Time when the user is next able to vote</td><td></td></tr><tr><td><code>url</code></td><td>Link to the platform</td><td></td></tr><tr><td><code>view_url</code></td><td>Link to the bot/servers page on the platform</td><td></td></tr><tr><td><code>vote_url</code></td><td>Link to vote on the platform</td><td></td></tr><tr><td><code>icon_url</code></td><td>Platform's icon/logo</td><td></td></tr></tbody></table>

### `rewards` Properties

<table data-full-width="true"><thead><tr><th width="207">Tag</th><th>Description</th><th data-type="select" data-multiple>Valid For</th></tr></thead><tbody><tr><td><code>role</code></td><td>Mention the primary reward role</td><td></td></tr><tr><td><code>role.id</code></td><td>ID of the primary reward role</td><td></td></tr><tr><td><code>role.duration</code></td><td>Duration primary reward role is kept for</td><td></td></tr></tbody></table>

### `miki` Properties

<table data-full-width="true"><thead><tr><th width="208">Tag</th><th>Description</th><th data-type="select" data-multiple>Valid For</th></tr></thead><tbody><tr><td><code>bucket</code></td><td>Bucket that given EXP is in</td><td></td></tr><tr><td><code>exp</code></td><td>Amount of EXP given to voter</td><td></td></tr><tr><td><code>levelled_up</code></td><td>If the user has levelled up</td><td></td></tr></tbody></table>

### Additional Tags

These tags have no Top Levels Tags and are used as just `{tag}`

<table data-full-width="true"><thead><tr><th width="207">Tag</th><th>Description</th><th data-type="select" data-multiple>Valid For</th></tr></thead><tbody><tr><td><code>date</code></td><td>Current date</td><td></td></tr><tr><td><code>monthlyVotes</code></td><td>Voter's votes in the monthly bucket. </td><td></td></tr></tbody></table>
