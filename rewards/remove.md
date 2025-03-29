---
description: >-
  Set the wrong number of votes for a role reward? Added to many role rewards?
  Don't worry, you can remove a role reward by following the steps shown here
---

# Removing

## Removing a single reward

To remove a single role reward, run the `/rewards remove` command

<figure><img src="../.gitbook/assets/rewards_remove_1.png" alt=""><figcaption><p>Rewards Remove Command</p></figcaption></figure>

{% tabs %}
{% tab title="Required Options" %}
* `type` - The type of tracker (**Bot**/**Server**)
* `tracker` - The tracker you wish to remove a reward from
* `role` - The reward that should be deleted
{% endtab %}
{% endtabs %}

<figure><img src="../.gitbook/assets/rewards_remove_2.png" alt=""><figcaption><p>Options have been filled out</p></figcaption></figure>

Once you have filled out all the options, you can run the command. The role reward will now not be given any more.

{% hint style="warning" %}
This does not remove the role from members, nor does it delete the role
{% endhint %}

## Removing All Rewards

Should you wish to remove all extra role rewards, you can use the `/rewards reset` command

<figure><img src="../.gitbook/assets/rewards_reset_1.png" alt=""><figcaption><p>Rewards Reset Command</p></figcaption></figure>

{% tabs %}
{% tab title="Required Options" %}
* `type` - The type of tracker (**Bot**/**Server**)
* `tracker` - The tracker you wish to remove a reward from
{% endtab %}
{% endtabs %}

<figure><img src="../.gitbook/assets/rewards_reset_2.png" alt=""><figcaption><p>Options have been filled out</p></figcaption></figure>

Once you have filled out all the options you can run the command and all extra vote rewards will be removed

{% hint style="warning" %}
This does not remove any of the roles from members, nor does it delete any of the roles
{% endhint %}
