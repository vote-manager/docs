---
description: >-
  Find a more detailed description about setting up a bot on Discords with Vote
  Manager
---

# Discords

{% hint style="info" %}
This continues from the tutorial on the previous page ([here](./))
{% endhint %}

To continue your setup, please go to the link shown as step one. It should look like this: `https://discords.com/bots/bot/[your-bots-id]/edit`

**E.G.** `https://discords.com/bots/bot/959699003010871307/edit`



You should be taken to a page that looks like the above image. Please enter the URL provided in step two into the field labelled **Webhook URL**, under **Developer Values**. The URL should follow the format `https://webhooks.votemanager.xyz/request/discords/[your-bots-id]/`

**E.G.** `https://webhooks.votemanager.xyz/request/discords/959699003010871307/`

Next, paste the passphrase provided into the field labelled **Webhook Secret**. Finally, scroll down to the bottom of the page and click **Apply Changes**



If you forget or lose your passphrase you can run the `/trackers passphrase` command. Select **Bot** for the type then choose the tracker from the options and run the command

<figure><img src="../../.gitbook/assets/tracker_passphrase.png" alt=""><figcaption><p>Trackers Passphrase Command</p></figcaption></figure>

Your vote tracker is now fully setup! A message will be sent with your configured embed to the channel you configured whenever a user upvotes your bot
