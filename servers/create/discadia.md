---
description: >-
  Find a more detailed description about setting up a server on Disurl with Vote
  Manager
hidden: true
---

# Discadia

{% hint style="info" %}
This continues from the tutorial on the previous page ([here](./))
{% endhint %}

To continue your setup, please go to the link shown as step one. It should look like this: `https://disurl.me/dashboard/server/[your-servers-id]/webhooks`

**E.G.** `https://disurl.me/dashboard/server/959775329843544074/webhooks`

<figure><img src="../../.gitbook/assets/disurl-1.png" alt=""><figcaption><p>Your servers Discord Servers webhooks page </p></figcaption></figure>

You should be taken to a page that looks like the above image.&#x20;

Paste the Webhook URL provided in step two into the field labelled **Webhook URL**. The URL should follow the format `https://webhooks.votemanager.xyz/request/disurl/[your-servers-id]/`

**E.G.** `https://webhooks.votemanager.xyz/request/disurl/959775329843544074/`

Next, enter the provided passphrase into the field labelled **Authorization Key**

<figure><img src="../../.gitbook/assets/disurl-2.png" alt=""><figcaption><p>Webhook Name &#x26; Payload URL have been filled out</p></figcaption></figure>

After filling out the fields as described above, click on the **Save** button. You should see an item added in the Active Webhooks section

<figure><img src="../../.gitbook/assets/disurl-3.png" alt=""><figcaption><p>Webhook details have been saved</p></figcaption></figure>

Your vote tracker is now fully setup! A message will be sent with your configured embed to the channel you configured whenever a user gives gems to/bumps your server

If you forget or lose your passphrase you can run the `/trackers passphrase` command. Select **Server** for the type then choose the tracker from the options and run the command

<figure><img src="../../.gitbook/assets/tracker_passphrase.png" alt=""><figcaption><p>Trackers Passphrase Command</p></figcaption></figure>
