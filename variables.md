---
description: >-
  Variables allow you to easily add information about the voter, bot, server and
  more into your custom vote embeds
---

# Variables



## Variable Formatting

Variables require **lowercase** letters and must be surrounded with `{}`.

Variables also do not contain spaces and are alphanumeric (a-z, 0-9), except for underscores(`_`).

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

## Variable List

The following variables are supported in all embed fields except image & field name & values. Please see below for a list of supported variables for images&#x20;

<table><thead><tr><th>Name</th><th>Description</th><th data-type="checkbox">Bots</th><th data-type="checkbox">Servers</th></tr></thead><tbody><tr><td>tag</td><td>Voters username &#x26; tag</td><td>true</td><td>true</td></tr><tr><td>id</td><td>Voters user ID</td><td>true</td><td>true</td></tr><tr><td>mention</td><td>Mentions the voter</td><td>true</td><td>true</td></tr><tr><td>total_votes</td><td>Voters total votes for the bot/server</td><td>true</td><td>true</td></tr><tr><td>monthly_votes</td><td>Voters votes for the bot/server this month</td><td>true</td><td>true</td></tr><tr><td>platform</td><td>Platform the bot/server was voted on</td><td>true</td><td>true</td></tr><tr><td>link</td><td>Link to vote for the bot/servre</td><td>true</td><td>true</td></tr><tr><td>date</td><td>Current date</td><td>true</td><td>true</td></tr><tr><td>role</td><td>Role given to voters</td><td>true</td><td>true</td></tr><tr><td>duration</td><td>Duration vote role is kept for</td><td>true</td><td>true</td></tr><tr><td>guild_name</td><td>Name of the voted or current server</td><td>true</td><td>true</td></tr><tr><td>guild_id</td><td>ID of the voted or current server</td><td>true</td><td>true</td></tr><tr><td>bot_name</td><td>Name of the voted bot</td><td>true</td><td>false</td></tr><tr><td>bot_mention</td><td>Mentions the voted bot</td><td>true</td><td>false</td></tr></tbody></table>

## Image Variable List

The following variables are only supported for the author, footer & main image fields of the vote embed

<table><thead><tr><th>Name</th><th>Description</th><th data-type="checkbox">Bots</th><th data-type="checkbox">Servers</th></tr></thead><tbody><tr><td>user_avtar</td><td>Voters icon</td><td>true</td><td>true</td></tr><tr><td>app_icon</td><td>Icon of the voted bot/server</td><td>true</td><td>true</td></tr></tbody></table>
