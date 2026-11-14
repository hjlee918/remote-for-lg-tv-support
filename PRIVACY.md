# Privacy Policy

**Remote for LG TV** (Stream Deck plugin), published by Artifex.
Effective date: November 14, 2026.

## Summary

The plugin does not collect, sell, or share personal data, and it sends nothing to us. TV control stays on your local network, between your computer and your TV. Only if you use the optional **Plex® Now Playing** key does the plugin also talk to Plex: to plex.tv to sign you in and list your servers, and to your own Plex Media Server.

## What the plugin stores, and where

The plugin saves the following in Stream Deck's settings on your computer:

- Each TV you paired: its name, model, IP address, network (MAC) addresses, and its UPnP identifier.
- The key each TV gave the plugin when you accepted the pairing request on the TV. It lets your computer control the TV without asking again.
- What you chose for each key or dial, for example "Volume up" or an app to open, and for app keys the app's name and icon, so the key looks right while the TV is off.

If you sign in to Plex for the Plex Now Playing key, also:

- The **Plex token** that plex.tv gives the plugin when you sign in with a code at plex.tv/link. It lets the plugin read your Plex Media Server. The plugin never sees or stores your Plex password. The token is sent only to plex.tv and to your Plex Media Servers, in a request header.
- Your Plex username and whether you have Plex Pass (to show in the settings).
- Each Plex server on your account: its name, identifier, version, and its addresses.
- An identifier the plugin makes for itself, so Plex lists it as a device on your account ("Remote for LG TV (Stream Deck)").

This information never leaves your computer except as described below. To delete it, click **Forget** next to a TV, or **Sign out** under Plex, in any key's settings, or uninstall the plugin. To also remove the plugin's access on the TV, remove it from the TV's list of connected devices or mobile apps in the TV's settings; to remove its access to Plex, go to plex.tv: Account → Authorized Devices.

## Network use

For the TV, the plugin communicates only with TVs on your local network:

- **Search** sends a standard discovery message (SSDP) on your local network to find LG TVs, or checks the IP address you enter.
- **Pair**, every key press and every dial turn send commands directly to your TV. While a key or dial is on your Stream Deck, the plugin keeps a connection to the TV open so the key can show the TV's state (for example its volume, or which app is on screen).
- **Power on** sends a Wake-on-LAN packet on your local network.
- App icons are downloaded from your TV.

For the optional Plex Now Playing key only:

- **Signing in:** the plugin asks plex.tv for a code, opens plex.tv/link in your browser, and asks plex.tv every few seconds whether you entered it.
- **Finding servers:** the plugin asks plex.tv for the servers on your account, and sends a standard Plex discovery message (GDM) on your local network.
- **While a Plex Now Playing key is on your Stream Deck,** the plugin reads your Plex Media Server: what's playing (titles, positions, which player and which user), and artwork, which it downloads from your server. It keeps a connection open to your server to hear about playback as it happens. It compares the player's IP address with your TV's to find what plays on the TV.

Without a Plex sign-in, the plugin makes no connections to the internet. It contains no analytics, tracking, or advertising, and uses no server of ours.

## Logs

Stream Deck keeps a plugin log on your computer to help diagnose problems:

- macOS: `~/Library/Application Support/com.elgato.StreamDeck/Plugins/com.johnlee.lgtvremote.sdPlugin/logs/`
- Windows: `%APPDATA%\Elgato\StreamDeck\Plugins\com.johnlee.lgtvremote.sdPlugin\logs\`

The log can include your TV's name and IP address, your Plex username and your Plex server's name and address, and messages about commands that failed. It never includes the TV's pairing key, the Plex token, or what you watch. The log stays on your computer unless you choose to share it.

## Support requests

If you open an issue in this repository, the issue and anything you attach to it (such as a log) are **public on GitHub** and subject to [GitHub's Privacy Statement](https://docs.github.com/site-policy/privacy-policies/github-general-privacy-statement). Remove anything you don't want to share before posting.

## Plex and purchases

Signing in and your Plex account are handled by Plex, under [Plex's Privacy Policy](https://www.plex.tv/about/privacy-legal/). Purchases on the Elgato Marketplace are handled by Elgato (Corsair) and its payment processor, Stripe. We do not receive your payment details. Elgato's privacy policy and [Stripe's Privacy Policy](https://stripe.com/privacy) describe how they handle your data.

## Changes

If this policy changes, the updated version will be posted here with a new effective date.

## Contact

Questions about this policy: [open an issue](https://github.com/hjlee918/remote-for-lg-tv-support/issues).
