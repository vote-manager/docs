---
description: >-
  Find a more detailed description about setting up a bot on Top.gg with Vote
  Manager
---

# Infinity Bots

{% hint style="info" %}
This continues from the tutorial on the previous page ([here](./))
{% endhint %}

To continue your setup, please go to the link shown as step one. It should look like this: `https://infinitybots.gg/bot/[your-bots-id]/settings`

**E.G.** `https://infinitybots.gg/bot/959699003010871307/settings`

<figure><img src="../../.gitbook/assets/ibl-1.png" alt=""><figcaption><p>Your bots Infinity Bots settings page</p></figcaption></figure>

You should be taken to a page that looks like the above image. Click on the sidebar option labelled **Webhooks** to view your bots webhooks

Next, click on the **+New Webhook** button show in the image below

<figure><img src="../../.gitbook/assets/ibl-2.png" alt=""><figcaption><p>Go to the Webhooks section</p></figcaption></figure>

After doing so, you should see a button labelled **Untitled Webhook** appear underneath it. Clicking on it should expand to show the webhook details

<figure><img src="../../.gitbook/assets/ibl-3 (1).png" alt=""><figcaption></figcaption></figure>

Name the webhook something that shows what it is, for example, Vote Manager. Then, paste the URL provided in step two into the **Webhook URL** box. The URL should follow the format `https://webhooks.votemanager.xyz/request/ibl/[your-bots-id]/`

**E.G.** `https://webhooks.votemanager.xyz/request/ibl/959699003010871307/`

Enter the provided Passphrase into the **Webhook Secret** field. Ensure that **Simple Auth** is left unchecked and the **Event Whitelist** contains **NEW\_VOTE** or is left empty

<figure><img src="../../.gitbook/assets/Bot Top.gg #2.png" alt=""><figcaption><p>Webhook URL &#x26; Authorization have been filled out</p></figcaption></figure>

If you forget or lose your passphrase, you can run the `/setup passphrase bot` command

<figure><img src="../../.gitbook/assets/ibl-5.png" alt=""><figcaption><p>Setup Passphrase Command</p></figcaption></figure>

Your vote tracker is now fully setup! A message will be sent with your configured embed to the channel you configured whenever a user upvotes your bot
