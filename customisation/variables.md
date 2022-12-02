---
description: >-
  Variables allow you to easily add information about the voter, bot, server and
  more into your custom vote embeds
---

# Variables



### Variable Formatting

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

### Variable List

<table><thead><tr><th>Name</th><th>Definition</th><th data-type="checkbox">Bots</th><th data-type="checkbox">Servers</th></tr></thead><tbody><tr><td>tag</td><td>Voters username &#x26; tag</td><td>true</td><td>true</td></tr><tr><td>id</td><td>Voters user ID</td><td>true</td><td>true</td></tr><tr><td>mention</td><td>Mentions the voter</td><td>true</td><td>true</td></tr><tr><td>total_votes</td><td>Voters total votes for the bot/server</td><td>true</td><td>true</td></tr><tr><td>platform</td><td>Platform the bot/server was voted on</td><td>true</td><td>true</td></tr><tr><td>bot_name</td><td>Name of the voted bot</td><td>true</td><td>false</td></tr><tr><td>bot_mention</td><td>Mentions the voted bot</td><td>true</td><td>false</td></tr><tr><td>guild_name</td><td>Name of the voted server</td><td>false</td><td>true</td></tr><tr><td>guild_id</td><td>ID of the voted server</td><td>false</td><td>true</td></tr></tbody></table>
