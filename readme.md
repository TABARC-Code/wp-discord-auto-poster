# WP-Discord Auto-Poster

Automatically post new WordPress content to a Discord channel via webhook, with some control instead of chaos.

## What it does

This plugin sends a Discord embed whenever I publish new content in WordPress.

I can:

- Choose which post types get auto-posted (posts, pages, custom post types).
- Toggle auto-posting on or off globally.
- Include or skip the featured image in the embed.
- Set the bot display name.
- Pick the embed accent colour.
- Manually post or repost individual items from a meta box.

If auto-posting is off, the manual controls still work.

---

## Requirements

- WordPress 5.0+ (block editor compatible, but also fine with Classic).
- A Discord server where I can create a webhook.
- PHP 7.4+ recommended.

---

## Installation

1. Clone or download this repository:

   ```bash
   git clone https://github.com/TABARC-Code/wp-discord-auto-poster.git
