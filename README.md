<h1 align="center">
VAFT + Keep Tab Active
</h1>

Merged userscript based on [TwitchAdSolutions (vaft)](https://github.com/pixeltris/TwitchAdSolutions) with integrated [Keep Tab Active](https://github.com/Vikindor/twitch-keep-tab-active) behavior.

This version is meant to replace the need to run a separate Twitch anti-ad script and a separate tab-activity script side by side. It keeps the core **vaft** ad-handling logic, while also adding the most useful parts of **Keep Tab Active** so Twitch is less likely to pause, mute, throttle, or de-prioritize playback in background tabs.

Particularly useful for those who want a single userscript for **ad handling + stable background playback**, including **Drops farming** and long passive viewing sessions.

## ✨ Features

- Keeps the core **vaft** anti-ad logic and player recovery behavior.
- Spoofs **visibility and focus** so Twitch treats the tab as active.
- Helps keep the player **“in view”** for observer-based checks.
- Sends light **activity pings** to reduce idle/background issues.
- Automatically clicks **Start Watching** and similar recovery gates when they appear.
- Keeps the script as a **single merged userscript** instead of relying on two overlapping scripts.

## 🚀 Installation

1. Install [Tampermonkey](https://www.tampermonkey.net/) or another userscript manager.
2. Install the merged script:
   - [VAFT_plus_Keep_Tab_Active.js](./VAFT_plus_Keep_Tab_Active.js)

## ⚙ How it works (high-level)

- `vaft` handles Twitch ad-related worker / stream / player logic.
- The merged keep-active layer makes the page report itself as visible and focused.
- The player is treated as visible by observer-based checks.
- Small UI interruptions such as “Start Watching” overlays are auto-cleared.
- Background playback is made more stable without overriding all programmatic pauses.

## ⚠️ Notes & Limitations

- Other Twitch extensions or userscripts that patch the same browser/player APIs may still conflict.
