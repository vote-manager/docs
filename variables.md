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

<table><thead><tr><th width="144">Tag</th><th>Description</th><th>Value</th></tr></thead><tbody><tr><td><code>voter</code></td><td>Contains information about the user who voted</td><td><code>&#x3C;@760170825629958184></code></td></tr><tr><td><code>guild</code></td><td>Contains information about the guild the tracker is setup in</td><td></td></tr><tr><td><code>app</code></td><td>Contains information about the bot that was voted for</td><td><code>&#x3C;@959699003010871307></code></td></tr><tr><td><code>platform</code></td><td>Contains information about the platform that the vote was on</td><td></td></tr><tr><td><code>rewards</code></td><td>Contains information about the rewards given</td><td></td></tr></tbody></table>

{% hint style="info" %}
There are other top level tags for integration provided tags, for example `miki` contains information about the Miki EXP data that was given. You can find a list of tags for each Integration on their Discovery page&#x20;
{% endhint %}

{% hint style="warning" %}
If a server was voted for, then any `app` tags will be replaced with nothing, or may not the replaced at all. The `guild` tag will always be replaced with the data of the server the vote message is to be sent in, even if the target was a bot
{% endhint %}

### `voter` Properties

<table data-full-width="true"><thead><tr><th width="191">Tag</th><th>Description</th><th>Valid For<select multiple><option value="9706cb0e435d4d1cadb32d26e9804bea" label="Image" color="blue"></option><option value="05360f9338284067940a45938172fa61" label="Text" color="blue"></option><option value="c6823b4adf8a4b0d8cb3a6a75b93057d" label="Colour" color="blue"></option><option value="21a57cdae11b43089d1fef31f0a19852" label="Date" color="blue"></option><option value="0f9f981453cf4eb386820cba3377dc49" label="Link" color="blue"></option></select></th></tr></thead><tbody><tr><td><code>id</code></td><td>ID of the voter</td><td><span data-option="05360f9338284067940a45938172fa61">Text</span></td></tr><tr><td><code>username</code></td><td>Username of the voter</td><td><span data-option="05360f9338284067940a45938172fa61">Text</span></td></tr><tr><td><code>global_name</code></td><td>Voter's global display name, falls back to <code>username</code> if not set</td><td><span data-option="05360f9338284067940a45938172fa61">Text</span></td></tr><tr><td><code>display_name</code></td><td>Voter's nickname, or <code>global_name</code> if not set</td><td><span data-option="05360f9338284067940a45938172fa61">Text</span></td></tr><tr><td><code>votes</code></td><td>Voter's total votes</td><td><span data-option="05360f9338284067940a45938172fa61">Text</span></td></tr><tr><td><code>buckets:&#x3C;id></code></td><td>Number of votes in the bucket with the ID <code>&#x3C;id></code>, for example <code>voter.buckets:monthly</code> would be the number of votes in the defaut Monthly bucket</td><td><span data-option="05360f9338284067940a45938172fa61">Text</span></td></tr><tr><td><code>created_at</code></td><td>Date voter's account was created on</td><td><span data-option="05360f9338284067940a45938172fa61">Text, </span><span data-option="21a57cdae11b43089d1fef31f0a19852">Date</span></td></tr><tr><td><code>joined_at</code></td><td>Date the voter joined the server</td><td><span data-option="05360f9338284067940a45938172fa61">Text, </span><span data-option="21a57cdae11b43089d1fef31f0a19852">Date</span></td></tr><tr><td><code>avatar_url</code></td><td>Voter's avatar</td><td><span data-option="9706cb0e435d4d1cadb32d26e9804bea">Image, </span><span data-option="0f9f981453cf4eb386820cba3377dc49">Link</span></td></tr><tr><td><code>banner_url</code></td><td>Voter's banner</td><td><span data-option="9706cb0e435d4d1cadb32d26e9804bea">Image, </span><span data-option="0f9f981453cf4eb386820cba3377dc49">Link</span></td></tr><tr><td><code>accent_color</code></td><td>Voter's profile accent colour. Will fallback to default embed if not set</td><td><span data-option="c6823b4adf8a4b0d8cb3a6a75b93057d">Colour</span></td></tr><tr><td><code>banner_color</code></td><td>Voter's profile banner colour. Will fallback to default embed if not set</td><td><span data-option="c6823b4adf8a4b0d8cb3a6a75b93057d">Colour</span></td></tr></tbody></table>

### `guild` Properties

<table data-full-width="true"><thead><tr><th width="194">Tag</th><th>Description</th><th>Valid For<select multiple><option value="4ef4de51d31d40d09caecd3c561f3d66" label="Image" color="blue"></option><option value="9fa6726afaf74dd880f80f22a55509d6" label="Text" color="blue"></option><option value="f66acade483644fb8e9a02c1b28ac887" label="Colour" color="blue"></option><option value="b27cb0ebbdd149fc915a196434647928" label="Date" color="blue"></option><option value="f3534bd4343b46e4938060ae24c111da" label="Link" color="blue"></option></select></th></tr></thead><tbody><tr><td><code>id</code></td><td>ID of the server</td><td><span data-option="9fa6726afaf74dd880f80f22a55509d6">Text</span></td></tr><tr><td><code>name</code></td><td>Name of the server</td><td><span data-option="9fa6726afaf74dd880f80f22a55509d6">Text</span></td></tr><tr><td><code>created_at</code></td><td>Date server was created</td><td><span data-option="9fa6726afaf74dd880f80f22a55509d6">Text, </span><span data-option="b27cb0ebbdd149fc915a196434647928">Date</span></td></tr><tr><td><code>icon_url</code></td><td>Server icon</td><td><span data-option="4ef4de51d31d40d09caecd3c561f3d66">Image, </span><span data-option="f3534bd4343b46e4938060ae24c111da">Link</span></td></tr><tr><td><code>banner_url</code></td><td>Server banner</td><td><span data-option="4ef4de51d31d40d09caecd3c561f3d66">Image, </span><span data-option="f3534bd4343b46e4938060ae24c111da">Link</span></td></tr></tbody></table>

### `app` Properties

<table data-full-width="true"><thead><tr><th width="197">Tag</th><th>Description</th><th>Valid For<select multiple><option value="2c2701d0cf3d4478b9a1c595e48fa413" label="Image" color="blue"></option><option value="6b105a42588442b596778fdffed76faa" label="Text" color="blue"></option><option value="f83e1f4c705c48949a4d2f20e4edba18" label="Colour" color="blue"></option><option value="b7fec09629954663a46eeac45682627e" label="Date" color="blue"></option><option value="d7013afe789a446884d8f8a450a47370" label="Link" color="blue"></option></select></th></tr></thead><tbody><tr><td><code>id</code></td><td>ID of the voted bot</td><td><span data-option="6b105a42588442b596778fdffed76faa">Text</span></td></tr><tr><td><code>username</code></td><td>Name of the voted bot</td><td><span data-option="6b105a42588442b596778fdffed76faa">Text</span></td></tr><tr><td><code>created_at</code></td><td>Date the voted bot was made</td><td><span data-option="6b105a42588442b596778fdffed76faa">Text, </span><span data-option="b7fec09629954663a46eeac45682627e">Date</span></td></tr><tr><td><code>joined_at</code></td><td>Date the voted bot joined the server</td><td><span data-option="6b105a42588442b596778fdffed76faa">Text, </span><span data-option="b7fec09629954663a46eeac45682627e">Date</span></td></tr><tr><td><code>avatar_url</code></td><td>Avatar of the voted bot</td><td><span data-option="2c2701d0cf3d4478b9a1c595e48fa413">Image, </span><span data-option="d7013afe789a446884d8f8a450a47370">Link</span></td></tr></tbody></table>

### `platform` Properties

<table data-full-width="true"><thead><tr><th width="202">Tag</th><th>Description</th><th>Valid For<select multiple><option value="23f8a3fbeefa4b0c98dcbfe90dab9341" label="Image" color="blue"></option><option value="9f3ee708c4954e3db63b5860055c3f0f" label="Text" color="blue"></option><option value="775955a3caf64bb4995aad2d830e795b" label="Colour" color="blue"></option><option value="01c08ead21f44c7a805ffdb85d907775" label="Date" color="blue"></option><option value="db019b5ebd864b24ab03e16a60c1e975" label="Link" color="blue"></option></select></th></tr></thead><tbody><tr><td><code>name</code></td><td>Name of the platform voted on</td><td><span data-option="9f3ee708c4954e3db63b5860055c3f0f">Text</span></td></tr><tr><td><code>next_vote.hours</code></td><td>Relative time until the user can vote (e.g. <strong>in 6 hours</strong>)</td><td><span data-option="9f3ee708c4954e3db63b5860055c3f0f">Text</span></td></tr><tr><td><code>next_vote</code></td><td>Time when the user is next able to vote</td><td><span data-option="9f3ee708c4954e3db63b5860055c3f0f">Text, </span><span data-option="01c08ead21f44c7a805ffdb85d907775">Date</span></td></tr><tr><td><code>url</code></td><td>Link to the platform</td><td><span data-option="9f3ee708c4954e3db63b5860055c3f0f">Text, </span><span data-option="db019b5ebd864b24ab03e16a60c1e975">Link</span></td></tr><tr><td><code>view_url</code></td><td>Link to the bot/servers page on the platform</td><td><span data-option="9f3ee708c4954e3db63b5860055c3f0f">Text, </span><span data-option="db019b5ebd864b24ab03e16a60c1e975">Link</span></td></tr><tr><td><code>vote_url</code></td><td>Link to vote on the platform</td><td><span data-option="9f3ee708c4954e3db63b5860055c3f0f">Text, </span><span data-option="db019b5ebd864b24ab03e16a60c1e975">Link</span></td></tr><tr><td><code>icon_url</code></td><td>Platform's icon/logo</td><td><span data-option="23f8a3fbeefa4b0c98dcbfe90dab9341">Image, </span><span data-option="db019b5ebd864b24ab03e16a60c1e975">Link</span></td></tr></tbody></table>

{% hint style="warning" %}
The `platform.next_vote` and `platform.next_vote.hours` tags are only supported in message content, embed field values, embed descriptions and embed timestamps due to a limitation of Discord's formatting. Using these tags in other fields will cuase unexpected formatting
{% endhint %}

### `rewards` Properties





<table data-full-width="true"><thead><tr><th width="207">Tag</th><th>Description</th><th>Valid For<select multiple><option value="10c03e80e2fd40dd8f0994356bf57694" label="Image" color="blue"></option><option value="a8d8f25826254ca08a6596be3afe0126" label="Text" color="blue"></option><option value="b981992639664c94a1c7651aae056a4b" label="Colour" color="blue"></option><option value="13305ff63e54422383c87be08fbd2265" label="Date" color="blue"></option><option value="54739159e2ec454886953de9a39bbb9a" label="Link" color="blue"></option></select></th></tr></thead><tbody><tr><td><code>role</code></td><td>Mention the primary reward role</td><td><span data-option="a8d8f25826254ca08a6596be3afe0126">Text</span></td></tr><tr><td><code>role.id</code></td><td>ID of the primary reward role</td><td><span data-option="a8d8f25826254ca08a6596be3afe0126">Text</span></td></tr><tr><td><code>role.name</code></td><td>Name of the primary reward role</td><td><span data-option="a8d8f25826254ca08a6596be3afe0126">Text</span></td></tr><tr><td><code>role.duration</code></td><td>Duration primary reward role is kept for</td><td><span data-option="a8d8f25826254ca08a6596be3afe0126">Text</span></td></tr><tr><td><code>role.color</code></td><td>Color of the primary reward role</td><td><span data-option="b981992639664c94a1c7651aae056a4b">Colour</span></td></tr></tbody></table>

### `miki` Properties

<table data-full-width="true"><thead><tr><th width="208">Tag</th><th>Description</th><th>Valid For<select multiple><option value="6ddaf5ed31b94d10b6735085f059b91a" label="Image" color="blue"></option><option value="72b7998e1f624133925b78d4c067cd6a" label="Text" color="blue"></option><option value="8f2feeea57a948ed8f4c25000d68a83d" label="Colour" color="blue"></option><option value="5e9dcedf24234961be99c49fa12ea147" label="Date" color="blue"></option><option value="91f1d732fc704ce9a043fde60326fbd9" label="Link" color="blue"></option></select></th></tr></thead><tbody><tr><td><code>bucket</code></td><td>Bucket that given EXP is in</td><td><span data-option="72b7998e1f624133925b78d4c067cd6a">Text</span></td></tr><tr><td><code>exp</code></td><td>Amount of EXP given to voter</td><td><span data-option="72b7998e1f624133925b78d4c067cd6a">Text</span></td></tr><tr><td><code>levelled_up</code></td><td>If the user has levelled up</td><td><span data-option="72b7998e1f624133925b78d4c067cd6a">Text</span></td></tr></tbody></table>

### Additional Tags

These tags have no Top Levels Tags and are used as just `{tag}`

<table data-full-width="true"><thead><tr><th width="207">Tag</th><th>Description</th><th>Valid For<select multiple><option value="9e1929b7c03944d7b352dc566d5a238d" label="Image" color="blue"></option><option value="6b96304e2f634b3698a983187ab28eee" label="Text" color="blue"></option><option value="f0c39f1be55e46fb9af86c597e5dfdcb" label="Colour" color="blue"></option><option value="805b9a31e0414bba9cf131690a8f5172" label="Date" color="blue"></option><option value="2b40c9716d084afd8bc2352e05c371a9" label="Link" color="blue"></option></select></th></tr></thead><tbody><tr><td><code>date</code></td><td>Current date</td><td><span data-option="6b96304e2f634b3698a983187ab28eee">Text, </span><span data-option="805b9a31e0414bba9cf131690a8f5172">Date</span></td></tr><tr><td><code>monthly_vote</code></td><td>Voter's votes in the monthly bucket. </td><td><span data-option="6b96304e2f634b3698a983187ab28eee">Text</span></td></tr></tbody></table>

{% hint style="danger" %}
`{monthly_votes}` has been deprecated and may be removed in a future update. You should use the tag `{voter.buckets:monthly}` instead
{% endhint %}
