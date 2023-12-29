---
description: >-
  Find a more detailed description about setting up a bot on Top.gg with Vote
  Manager
---

# Top.gg

{% hint style="info" %}
This continues from the tutorial on the previous page ([here](./))
{% endhint %}

To continue your setup, please go to the link shown as step one. It should look like this: `https://top.gg/bot/[your-bots-id]/webhooks`

**E.G.** `https://top.gg/bot/959699003010871307/webhooks`

<figure><img src="../../.gitbook/assets/Bot Top.gg #1.png" alt=""><figcaption><p>Your bots Top.gg webhooks page</p></figcaption></figure>

{% hint style="success" %}
You need to be logged in & own or be in a team that owns the bot on Top.gg to access this page
{% endhint %}

You should be taken to a page that looks like the above image. Please paste the URL provided in step two into the **Webhook URL** box. The URL should follow the format `https://webhooks.votemanager.xyz/request/[platform]/[your-bots-id]/`

**E.G.** `https://webhooks.votemanager.xyz/request/topgg/959699003010871307/`

You should then paste the passphrase shown in step six into the **Authorization** box. It should be a 20 character long string

<figure><img src="../../.gitbook/assets/Bot Top.gg #2.png" alt=""><figcaption><p>Webhook URL &#x26; Authorization have been filled out</p></figcaption></figure>

If you forget or lose your passphrase you can run the `/setup passphrase bot` command

<figure><img src="../../.gitbook/assets/Bot Top.gg #3.png" alt=""><figcaption><p>Setup Passphrase Command</p></figcaption></figure>

Your vote tracker is now fully setup! A message will be sent with your configured embed to the channel you configured whenever a user bumps or server on Discord Servers
