---
description: >-
  Vote Manager supports vote tracking for servers on Top.gg & Discord Servers.
  Below, you can find information about how to set up Vote Manager for your
  Discord Bot
---

# Creating

To get started with setup, run the `/setup create server` command and fill in the options

<figure><img src="../.gitbook/assets/Server Create #1.png" alt=""><figcaption><p>Setup Create Command</p></figcaption></figure>

{% tabs %}
{% tab title="Required Options" %}
* `platform` - The platform you want to setup the vote tracker on
* `channel` - The channel to send your vote message in
{% endtab %}

{% tab title="Optional Options" %}
* `role` - Role to be given to users after they vote
* `duration` - How long user should keep the role specified above
* `ping` - Should the voter be pinged in the vote message
{% endtab %}
{% endtabs %}

<figure><img src="../.gitbook/assets/Server Create #2.png" alt=""><figcaption><p>Options have been filled out</p></figcaption></figure>

Once you have filled out the options, run the command. Upon doing so, a  pop-up will appear allowing you to customise the embed on your vote message. Please see below for details about required & optional fields as well as default values

<figure><img src="../.gitbook/assets/Server Create #3.png" alt=""><figcaption><p>Vote Embed Builder</p></figcaption></figure>

{% hint style="success" %}
You can use variables to have vote infomation in your vote message. see [here](../variables.md) for more details
{% endhint %}

{% tabs %}
{% tab title="Required Fields" %}
* **Title** - title of the embed
  * <mark style="color:green;">**✓**</mark> <mark style="color:green;"></mark><mark style="color:green;">- Variables are supported</mark>
  * <mark style="color:green;">**✓**</mark> <mark style="color:green;"></mark><mark style="color:green;">- Markdown is supported</mark>
* **Color** - color of the left border on the embed
  * <mark style="color:red;">**✗**</mark> <mark style="color:red;"></mark><mark style="color:red;">- Variables are not supported</mark>
  * <mark style="color:red;">**✗**</mark> <mark style="color:red;"></mark><mark style="color:red;">- Markdown is not supported</mark>
  * <mark style="color:green;">**✓**</mark> <mark style="color:green;"></mark><mark style="color:green;">- Allowed formats</mark>
    * Hex code (Ex `#0bbbb7`)
    * Integer (Ex `0x0bbbb7`)
    * RGB color values (Ex `11, 187, 183`)
    * Preset (Ex `Red`)
    * Random (use `Random`)
    * Any other valid format found [here](https://discord.js.org/#/docs/main/main/typedef/ColorResolvable)
* **Description** - main content of the embed
  * <mark style="color:green;">**✓**</mark> <mark style="color:green;"></mark><mark style="color:green;">- Variables are supported</mark>
  * <mark style="color:green;">**✓**</mark> <mark style="color:green;"></mark><mark style="color:green;">- Markdown is supported</mark>
* **Footer** - small text at the bottom of the embed
  * <mark style="color:green;">**✓**</mark> <mark style="color:green;"></mark><mark style="color:green;">- Variables are supported</mark>
  * <mark style="color:red;">**✗**</mark> <mark style="color:red;"></mark><mark style="color:red;">- Markdown is not supported</mark>
{% endtab %}

{% tab title="Optional Fields" %}
**Image** - Big image in the embed. Appears below the description

* <mark style="color:red;">**✗**</mark> <mark style="color:red;"></mark><mark style="color:red;">- Variables are not supported</mark>
* <mark style="color:red;">**✗**</mark> <mark style="color:red;"></mark><mark style="color:red;">- Markdown is not supported</mark>
* <mark style="color:green;">**✓**</mark> <mark style="color:green;"></mark><mark style="color:green;">- Allowed formats</mark>
  * Any `https`or `http` link to an image file
{% endtab %}
{% endtabs %}

Once you have made your custom embed, press the submit button. This will close the pop-up, and you will be sent a message similar to the following

<figure><img src="../.gitbook/assets/Server Create #4.png" alt=""><figcaption><p>Last step in Discord</p></figcaption></figure>

* **1**: These are the next steps for your setup. You can find more detail about them by going to the page in our docs for the bot list you are using:
  * [Top.gg](broken-reference)
  * [Discord Servers](discordservers.md)
* **2**: Details about your vote tracker including the channel, role & duration
* **3**: This is the authentication password for your tracker. **Do not share this with anyone else!** We also recommend keeping this somewhere safe as you may need it later
* **4:** The second embed is a preview of your vote message

To continue your setup, please go to the URL provided in the above embed (#1). Here you should find a place to input the webhook URL provided in the above embed (#2) and the password (#6). If you can't find it please go to our docs page from the bot list you are using.
