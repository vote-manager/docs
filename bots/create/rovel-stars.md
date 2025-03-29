---
description: >-
  Find a more detailed description about setting up a bot on Void Bots with Vote
  Manager
hidden: true
---

# Rovel Stars

{% hint style="info" %}
This continues from the tutorial on the previous page ([here](./))
{% endhint %}

To continue your setup, please go to the link shown as step one. It should look like this: `https://voidbots.net/bot/[your-bots-id]/webhooks`

**E.G.** `https://voidbots.net/bot/959699003010871307/webhooks`

<figure><img src="../../.gitbook/assets/voidbots-1.png" alt=""><figcaption><p>Your bots Void Bots webhook settings page</p></figcaption></figure>

&#x20;Please paste the URL provided in step two into the **Webhook URL** box. The URL should follow the format `https://webhooks.votemanager.xyz/request/voidbots/[your-bots-id]/`

**E.G.** `https://webhooks.votemanager.xyz/request/voidbots/959699003010871307/`

Next, enter the provided passphrase into the **Authorization** field

Once you have filled out the required fields, click the **Edit** button to save your changes

<figure><img src="../../.gitbook/assets/voidbots-2.png" alt=""><figcaption><p>Webhook URL &#x26; Authorization have been filled out</p></figcaption></figure>

If you forget or lose your passphrase you can run the `/trackers passphrase` command. Select **Bot** for the type then choose the tracker from the options and run the command

<figure><img src="../../.gitbook/assets/tracker_passphrase.png" alt=""><figcaption><p>Trackers Passphrase Command</p></figcaption></figure>

Your vote tracker is now fully setup! A message will be sent with your configured embed to the channel you configured whenever a user upvotes your bot
