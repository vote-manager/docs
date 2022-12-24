---
description: >-
  Want to add more role rewards for voters? Say for 20, 30 or 50 votes? You can
  do that! The steps shown here will teach you how
---

# Adding

To add a new role reward, run the `/rewards add` command

<figure><img src="../.gitbook/assets/Rewards Add #1.png" alt=""><figcaption><p>Rewards Add Command</p></figcaption></figure>

{% tabs %}
{% tab title="Required Options" %}
* `platform` - The platform to add a role reward on
* `bot` - The bot you want to add a role reward for (only for `/rewards add bot`)
* `type` - The type of votes to check
* `votes` - How many votes the user needs to be given the role
* `role` - The role the user should be given
{% endtab %}

{% tab title="Optional Options" %}
* `duration` - Set the duration the user should keep the role for
{% endtab %}
{% endtabs %}

<div>

<figure><img src="../.gitbook/assets/Rewards Add #2.png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../.gitbook/assets/Rewards Add #3.png" alt=""><figcaption><p>Options have been filled out</p></figcaption></figure>

</div>

Once you have filled out all the options, you can run the command and the role reward will be saved

The role will now be given to any users to votes the provided number of times on the provided platform for the bot/server

{% hint style="info" %}
The role is only given when a user reaches the number of votes. It will not be given to users who already have enough votes until they vote again
{% endhint %}
