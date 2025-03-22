---
description: >-
  Find a more detailed description about setting up a server on Top.gg with Vote
  Manager
---

# Top.gg

{% hint style="danger" %}
Top.gg has how deprecated server listing. You can no longer create new trackers for servers on Top.gg and we recommend you delete existing ones&#x20;
{% endhint %}

{% hint style="info" %}
This continues from the tutorial on the previous page ([here](../../bots/create/))
{% endhint %}

To continue your setup, please go to the link shown as step one. It should look like this: `https://top.gg/servers/[your-servers-id]/webhooks`

**E.G.** `https://top.gg/servers/959699003010871307/webhooks`

<figure><img src="../../.gitbook/assets/topgg-1.png" alt=""><figcaption><p>Your servers Top.gg webhooks page</p></figcaption></figure>

{% hint style="success" %}
You need to be logged in & own or be in a team that owns the server on Top.gg to access this page
{% endhint %}

You should be taken to a page that looks like the above image. Please paste the URL provided in step two into the **Webhook URL** box. The URL should follow the format `https://webhooks.votemanager.xyz/request/topgg/[your-servers-id]/`

**E.G.** `https://webhooks.votemanager.xyz/request/topgg/959775329843544074/`

You should then paste the passphrase shown in step six into the **Authorization** box. It should be a 20 character long string

<figure><img src="../../.gitbook/assets/topgg-2.png" alt=""><figcaption><p>Webhook URL &#x26; Authorization have been filled out</p></figcaption></figure>

After entering the required details, click **Save**. Your vote tracker is now fully setup! A message will be sent with your configured embed to the channel you configured whenever a user votes for your server on Top.gg

If you forgot or lose your passphrase, you can view it using the `/setup passphrase server` command

<figure><img src="../../.gitbook/assets/Server Top.gg #3.png" alt=""><figcaption><p>Setup Passphrase Command</p></figcaption></figure>
