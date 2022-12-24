---
description: >-
  Set the wrong number of votes for a role reward? Added to many role rewards?
  Don't worry, you can remove a role reward by following the steps shown here
---

# Removing

## Removing a single reward

To remove a single role reward, run the `/rewards remove` command

<figure><img src="../.gitbook/assets/Rewards Remove #1.png" alt=""><figcaption><p>Rewards Remove Command</p></figcaption></figure>

{% tabs %}
{% tab title="Required Options" %}
* `platform` - The platform to add a role reward on
* `bot` - The bot you want to add a role reward for (only for `/rewards remove bot`)
* `votes` - How many votes the user needs to be given the role
* `role` - The role the user should be given
{% endtab %}
{% endtabs %}

<div>

<figure><img src="../.gitbook/assets/Rewards Remove #2.png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../.gitbook/assets/Rewards Remove #3.png" alt=""><figcaption></figcaption></figure>

</div>

Once you have filled out all the options, you can run the command. The role reward will now not be given any more.

{% hint style="warning" %}
This does not remove the role from members, nor does it delete the role
{% endhint %}

## Removing All Rewards

Should you wish to remove all extra role rewards, you can use the `/rewards reset` command

<figure><img src="../.gitbook/assets/Rewards Reset #1.png" alt=""><figcaption><p>Rewards Reset Command</p></figcaption></figure>

{% tabs %}
{% tab title="Required Options" %}
* `platform` - platform to add a role reward on
* `bot` - The bot you want to add a role reward for (only for `/rewards reset bot`)
{% endtab %}
{% endtabs %}

<div>

<figure><img src="../.gitbook/assets/Rewards Reset #2.png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../.gitbook/assets/Rewards Reset #3.png" alt=""><figcaption><p>Options have been filled out</p></figcaption></figure>

</div>

Once you have filled out all the options you can run the command and all extra vote rewards will be remove

{% hint style="danger" %}
There is currently no confirmation for reseting vote rewards
{% endhint %}

{% hint style="warning" %}
This does not remove any of the roles from members, nor does it delete any of the roles
{% endhint %}

{% hint style="success" %}
This will not remove youe main vote role&#x20;
{% endhint %}
