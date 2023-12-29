---
description: >-
  Find a more detailed description about setting up a bot on Botlist.me with
  Vote Manager
---

# Botlist.me

{% hint style="info" %}
This continues from the tutorial on the previous page ([here](./))
{% endhint %}

To continue your setup, please go to the link shown as step one. It should look like this: `https://botlist.me/bot/[your-bots-id]/edit`

**E.G.** `https://botlist.me/bot/959699003010871307/edit`

<figure><img src="../../.gitbook/assets/botlist-1.png" alt=""><figcaption><p>Your bots Botlist.me settings page</p></figcaption></figure>

You should be taken to a page that looks like the above image. Scroll down find the fields labelled **Webhook URL** and **Webhook Authorization** near the bottom.

<figure><img src="../../.gitbook/assets/botlist-2.png" alt=""><figcaption><p>Scroll down to the webhook options</p></figcaption></figure>

&#x20;Please paste the URL provided in step two into the **Webhook URL** box. The URL should follow the format `https://webhooks.votemanager.xyz/request/botlist/[your-bots-id]/`

**E.G.** `https://webhooks.votemanager.xyz/request/botlist/959699003010871307/`

Next, enter the provided passphrase into the **Webhook Authorization** field

Once you have filled out the required fields, click the **Edit** button to save your changes

<figure><img src="../../.gitbook/assets/botlist-3.png" alt=""><figcaption><p>Webhook URL &#x26; Authorization have been filled out</p></figcaption></figure>

If you forget or lose your passphrase, you can run the `/setup passphrase bot` command

<figure><img src="../../.gitbook/assets/botlist-4.png" alt=""><figcaption><p>Setup Passphrase Command</p></figcaption></figure>

Your vote tracker is now fully setup! A message will be sent with your configured embed to the channel you configured whenever a user upvotes your bot
