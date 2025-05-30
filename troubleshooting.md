---
description: Here are a few problems people run into frequently and some solutions
---

# Troubleshooting

<details>

<summary>The vote message is not being sent</summary>

Please ensure that the channel you have configured exists and that vote manager has the following permissions in it:

* View Channel
* Send Messages
* Embed Links

</details>

<details>

<summary>The reward role is not being given</summary>

There are 2 common causes for this issue:

1. **Vote Manager does not have permission to give roles**\
   In order to solve this, please ensure that vote manager has a least one role with either the **Manage Roles** or **Administrator** permission
2. **The role Vote Manager is trying to give is above its highest role**\
   Bots are only able to give roles that are below their highest role. To solve this, move at least one role (likely the `@Vote Manager` role above the role you are trying to give, as below

<img src=".gitbook/assets/troubleshooting_role_order.png" alt="" data-size="original">

</details>

<details>

<summary>The bot cannot respond to commands or send messages</summary>

Vote Manage requires at least one role (usually the `@Vote Manager` role with the following permissions

* View Channels
* Send Messages
* Send Messages in Threads
* Use External Emojis
* Embed Links
* Attach Files
* Add Reactions
* Manage Roles
* Manage Webhooks
* Read Message History

Alternatively, you can grant the **Administrator** permission to any role that Vote Manager has to provide it with all required permissions

</details>
