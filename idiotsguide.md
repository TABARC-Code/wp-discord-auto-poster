# Idiots Guide to Webhooks and This Plugin

I am keeping this simple on purpose. Webhooks tend to get wrapped in technical language that scares people off. The truth is less dramatic. A webhook is basically a URL that accepts data. Nothing supernatural. Just a special link you send information to, and the receiving service does something with it.

Once you understand that, everything else makes more sense.

-------

## What a webhook really is

A webhook is a listening point. Imagine a mailbox that only accepts parcels. You cannot put letters in it, only parcels, and every time the mailbox gets a parcel it reacts in a specific way. Discord reacts by posting the message into a channel.

So the plugin grabs some info from WordPress, puts it in a digital parcel, and sends it to the webhook URL. Discord sees it, nods, and drops the message into the channel.

That is the entire mechanism.

-------

## Why Discord uses webhooks

Normally if you want a proper Discord bot, you need a token, a developer account, a server running 24 hours a day, libraries, gateways and a small prayer. Webhooks cut that nonsense out.

A Discord webhook URL contains everything needed for posting. It is a single key that says "send stuff here and I'll deal with it".

No passwords.
No coding.
No massive setup rituals.

---

## What the webhook URL looks like

It is long. Slightly ugly. Something like this:

```
https://discord.com/api/webhooks/123456789012345678/SomeVeryLongToken
```

Think of it as a VIP backstage pass. Whoever has the URL can post to that channel. Treat it like a password. Do not paste it in public places unless you want random strangers posting memes in your server.

---

## How the plugin uses the webhook

The plugin reads your post title, excerpt, link and possibly the featured image. It builds a little packet of data called JSON. This packet tells Discord what to show.

Then the plugin sends it to the webhook URL. Discord checks the packet and posts it. Discord always replies with a code. The success code is 204. If anyone is wondering why it is not 200, join the club. It just is. Computers enjoy being quirky.

-------

## Why the plugin needs the webhook URL

Discord does not come to WordPress asking for news. WordPress must go to Discord. To go somewhere, WordPress needs an address. The webhook URL is the destination.

WordPress pushes the message
Discord receives it
The channel updates
Life continues

-------

## How to get a webhook URL in Discord

Here is the simple version without scary steps.

1. Open Discord and go into the server you want to use.
2. Pick the channel you want messages to appear in.
3. Open the settings for that channel.
4. Look for Integrations.
5. Inside Integrations, look for Webhooks.
6. Create a new webhook or edit an existing one.
7. Copy the Webhook URL.

Paste that into the plugin settings. Done.

No tokens. No extra apps. No windows full of code.

-------

## Why this method is easier than using a full Discord bot

A full bot needs a permanent home. It needs safe handling for its secret token. It needs code to connect to the Discord gateway and wait for events. It needs someone who cares enough to maintain it.

A webhook needs a URL and one request. That is why this plugin uses it. It behaves without demanding a whole coding ecosystem.

---------

## Webhook definition in one sentence

A webhook is a URL that waits for data and triggers an action when it receives it.

-------

## Notes for the confused or sleep deprived

I have seen people freeze at the word webhook. The key is not to overthink it. If you can paste a link into a browser, you can handle a webhook URL. The plugin does the heavy lifting. The only real mistake you can make is pasting the wrong URL or forgetting the URL entirely.

You can test the URL from the settings page. If Discord replies, everything is fine. If not, Discord sends back an error which usually means the URL was wrong or the webhook was deleted.

-------

## Basic setup guide

These are the steps without commentary or complexity. Just the actions.

1. Install the plugin into your WordPress plugins folder.
2. Activate the plugin in the WordPress admin.
3. Go into your Discord server.
4. Go into the channel settings for the channel you want messages in.
5. Open Integrations.
6. Open Webhooks.
7. Create a webhook or select an existing one.
8. Copy the webhook URL.
9. Paste the URL into the plugin settings page.
10. Choose which post types you want to auto post.
11. Choose whether to include the featured image.
12. Save settings.
13. Publish a post.
14. Watch Discord update.

If it does not update, test your webhook in the plugin settings. If the test works, the plugin is able to send messages. If the test fails, the webhook URL is the first suspect.

-------
