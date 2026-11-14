# Remote for LG TV

Support page for **Remote for LG TV**, a Stream Deck plugin that controls LG OLED and other LG webOS smart TVs: remote buttons, power, volume, apps, inputs, picture and sound settings, Stream Deck + dials, and a Plex® Now Playing key. Get it on the [Elgato Marketplace](https://marketplace.elgato.com/).

## Get help

- **Found a bug?** [Open a bug report](../../issues/new?template=bug_report.yml).
- **Have an idea?** [Suggest a feature](../../issues/new?template=feature_request.yml).

Please search [existing issues](../../issues) first.

## Requirements

- Windows 10 or later, or macOS 12 or later.
- Stream Deck 7.1 or later.
- An LG webOS smart TV (2014 or later, including LG OLED) on the same network as the computer.
- For the Plex Now Playing key: a Plex account, a Plex Media Server the computer can reach, and the Plex app on the TV.

## Setup

1. Turn the TV on.
2. Drag any **Remote for LG TV** action onto a key, for example **Remote Button**.
3. In its settings, click **Search**, choose your TV, and click **Pair**. If nothing is found, type the TV's IP address and click **Search** again. The IP address is in the TV's settings under **General → Network → Wi-Fi Connection** (or **Wired Connection**) → **Advanced Settings**; the exact menu names vary by model.
4. **Accept** the request that appears on the TV, using the TV's remote.
5. Choose what the key does. Add more keys for other actions; they all share the pairing.

**To turn the TV on from Stream Deck**, turn on **Turn on via Wi-Fi** (on some models **Mobile TV On** or **LG Connect Apps**) in the TV's settings, under **General → Devices → TV Management** or **Connection**, depending on the model.

**More than one TV?** Click **Add TV** in any key's settings and pair it the same way. Each key or dial then has a **Control** menu for choosing its TV; the first TV paired is the default.

**Plex Now Playing:** drag the key onto Stream Deck, pair the TV as above, then click **Sign in** under **Plex** in its settings. A short code appears and plex.tv/link opens in your browser: sign in there and enter the code. The plugin never sees your Plex password. Your Plex Media Server is found on its own; if it isn't, enter its IP address under **Address**.

## The actions

| Action | What it does |
|---|---|
| **Remote Button** | Any button of the TV's remote: arrows, OK, Back, Home, Exit, Settings, Quick Settings, Info, playback, channels, numbers, color buttons, subtitles and more. Can also type text into a search field, open a web page, show a message on the TV, or go to a channel by number. Optional **Hold** and **Double press** commands. |
| **Power** | Power on / off, power on, power off, or screen off / on (the sound keeps playing). A green dot shows when the TV is on. |
| **Volume** | Volume up or down (hold to repeat), mute, or a set level. The key shows the TV's volume. |
| **Open App** | Opens an app from the TV's list, optionally straight to a YouTube video. The key shows the app's icon, with a bar while it's on screen. |
| **Input** | Switches to an HDMI input, the next input, or opens the TV's input list. The key shows a bar while that input is on screen. |
| **Picture & Sound** | Picture mode, next picture mode, energy saving, brightness (OLED light or backlight), or sound output (TV speakers, soundbar over HDMI ARC, optical, Bluetooth). |
| **Plex Now Playing** | Shows the poster, title and progress of what Plex plays on this TV, read from your Plex Media Server, with a pause sign while paused. Press to pause or play (the TV's own Play and Pause buttons are sent). |
| **TV Dial** (Stream Deck +) | Volume, channels, navigation, playback, apps, inputs, brightness or scrolling, with the volume, channel or app shown on the touch strip. |

## Troubleshooting

- **Search finds nothing:** make sure the TV is on and on the same network as the computer, then enter its IP address and search again. Some routers and mesh Wi-Fi systems block automatic discovery.
- **No request appears on the TV, or pairing fails:** turn the TV on fully (not in standby) and try **Pair** again. If you declined the request by mistake, pair again and accept it.
- **Keys say "TV is off" while the TV is on:** the TV's IP address may have changed. The plugin looks for the TV again on its own; if that doesn't work, reserve a fixed IP address for the TV in your router, then click **Forget** and pair again.
- **Power on doesn't work:** turn on **Turn on via Wi-Fi** / **Mobile TV On** in the TV's settings (see Setup). Some TVs can only be woken over a wired connection, or for a while after they were turned off. Waking from the plugin also needs the computer and the TV on the same network.
- **A picture setting doesn't change:** some settings only apply to the kind of picture on screen (an HDR mode only while HDR content plays), and not every model has every mode.
- **Volume keys show "External speaker":** the sound goes to a device whose volume the TV can't control (for example an optical connection). Use that device's own volume control.
- **Plex Now Playing says "Not playing" while Plex plays on the TV:** the key looks for the Plex player with the TV's IP address. Open the key's settings and choose the TV's Plex app in **Show** (it's listed while something plays). If it says **Server off**, check that the computer can reach your Plex Media Server, or enter its IP address under **Address**.
- **Plex Now Playing shows the right film, but pressing it does nothing:** make sure the Plex app is on the TV's screen (the key sends the TV's Play and Pause buttons to the app in front).
- **Windows asks whether to allow network access:** choose **Allow** so the plugin can find and control your TV on your local network.

When reporting a bug, attach the latest log from:

- **macOS:** `~/Library/Application Support/com.elgato.StreamDeck/Plugins/com.johnlee.lgtvremote.sdPlugin/logs/`
- **Windows:** `%APPDATA%\Elgato\StreamDeck\Plugins\com.johnlee.lgtvremote.sdPlugin\logs\`

## Privacy

The plugin collects no personal data. It connects to your TV on your local network and, only if you use the Plex Now Playing key, to plex.tv and your Plex Media Server. See the [Privacy Policy](PRIVACY.md).

## Open-source software

The plugin includes open-source software; see `THIRD_PARTY_NOTICES.txt` inside the plugin.

---

LG, webOS and OLED evo are trademarks of LG Electronics Inc. This plugin is not affiliated with, sponsored by, or endorsed by LG Electronics Inc. Plex is a trademark of Plex, Inc. This plugin is not affiliated with, sponsored by, or endorsed by Plex, Inc.
