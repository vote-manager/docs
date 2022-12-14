---
description: >-
  Made a slight typo in your vote embed? Need to change the vote message
  channel? You can edit your setup using the steps below
---

# Editing

{% hint style="info" %}
This requires you to already have an existing setup for the server you are running the command in, on the platform you want to edit
{% endhint %}

To edit a vote tracker, simply run the `/setup edit server` command and fill in the required options.

<figure><img src="../.gitbook/assets/Server Edit #1.png" alt=""><figcaption><p>Setup Edit Command</p></figcaption></figure>

Use the optional `channel`, `role` & `duration` parameters to change the respective settings for the vote tracker. Any options left blank will retain their previous value

{% tabs %}
{% tab title="Required Options" %}
* `platform` - The platform you want to edit the setup for
{% endtab %}

{% tab title="Optional Options" %}
* `channel` - Channel to send your vote message in
* `role` - Role to be given to users after they vote
* `duration` - How long user should keep the role specified above
{% endtab %}
{% endtabs %}

<figure><img src="../.gitbook/assets/Server Edit #2.png" alt=""><figcaption><p>Options have been filled out</p></figcaption></figure>

{% hint style="info" %}
Other rewards can be managed via the `/rewards` command (more details [here](broken-reference))
{% endhint %}

Once you have run the `/setup edit` command, the vote message embed will appear, allowing your vote embed to be updated. If you wish to leave your vote embed the same, simply press <mark style="color:purple;">**Submit**</mark>

<figure><img src="../.gitbook/assets/Server Create #3.png" alt=""><figcaption><p>Vote Message Embed Builder</p></figcaption></figure>
