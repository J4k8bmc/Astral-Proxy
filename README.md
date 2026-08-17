Astral Proxy

A local Minecraft 1.8.9 proxy for Hypixel Bedwars - denicking, custom tab stats, floating nametags, rush/target analysis, and behavior-based AntiCheat. Runs entirely on your own machine; nothing you do is sent anywhere except the API calls each feature needs (Hypixel, Bordic/Aurora, Urchin, Seraph - only if you set a key for it).

> **Beta.** Most features are stable, but the AntiCheat checks in particular are heuristic-based and will occasionally false-flag or miss things. Treat a flag as a hint to watch someone more closely, not proof.

Setup

1. Download the latest `.exe` from [Releases](../../releases)
2. Press windows + r and copy this PATH: (`C:\Windows\System32\drivers\etc\hosts`) and press enter.
3. (Enable desktop icons if you have them hidden) then drag the "hosts" file to desktop.
4. Right click on it and press "Edit in notepad". Scroll down and paste this line in the bottom: `127.0.0.1 mc.hypixel.net`.
5. Click save (Ctrl + s) and drag the file back into `C:\Windows\System32\drivers\etc\hosts` folder.
6. Launch terminal and type `ipconfig /flushdns` or reboot computer.
7. Launch `Astral Proxy.exe`, click on the `PAUSED` Proxy Status and allow public and private network access.
8. In the minecraft server list add these IP's: `proxy.hypixel.net`or`play.hypixel.net`(Your hypixel IP from now on) and add the proxy IP: `hypixel.net`. Make sure you have set Server Resource Pack to Enabled to ensure tabstats alignment.
9. Set your API keys once it's running - when you join on the proxy ip - `hypixel.net` you will now have access to several commands. Do: `/setkey <|urchin|seraph|aurora> <key>`for every key.
10. Lastly regenerate/create hypixel API key by clicking the "REGENERATE" button inside the app. Once you log in and copy the key simply press on "REPLACE" button and you're ready to play.

To remove the hosts entry later (e.g. to play without the proxy), just delete that line from the hosts file.

Commands

Config
| Command | Description |
|---|---|
| `/ap config` | Main settings menu (snipe messages, safelist, nick override, API keys) |
| `/tabconfig` | Tab column formatting menu |

Toggles
| Command | Description |
|---|---|
| `/pchat` | Shows your messages in party chat |
| `/tabstats` | Custom tab-list stats rendering |
| `/nametags` | Floating in-world nametag badges |
| `/resourcepack` | Exact-pixel tab alignment via a small resource pack |
| `/rbw` | Ranked Bedwars mode - locks non-essential features, enables nametags |
| `/skindenicker` | Resolve nicked players by their embedded skin profile name |
| `/numdenicker` | Resolve nicked players by kill-feed counts |
| `/denickstats` | Show stats automatically after a denick |
| `/pregamestats` | Show player stats when they talk in queue |
| `/alerts` | Show tag descriptions when the game starts |
| `/rushmsg` | Auto rush-direction analysis |
| `/targetmsg [wlr]` | Auto priority-target analysis (`wlr` toggles showing WLR in it) |
| `/partycounter` | Announce party join/leave counts |
| `/autobusy` | `/status busy` on queue, `/status online` after 60s back in the lobby |
| `/blockstats` | Auto stats+tags+unblock for resolved blocklist entries |
| `/prefix` | Show the `[AP]` tag on every message |
| `/debug` | Verbose `[DEBUG]` chat messages |
| `/shortenranks` | Shows `[M++]` instead of `[MVP++]` in tab/nametags |
| `/brackets` | Wrap star/prestige level in `[brackets]` everywhere it's shown |

Info lookups
| Command | Description |
|---|---|
| `/info <name>` | Rank, stars, FKDR/WLR + tags |
| `/stats <name>` | Rank, stars, full BW stats + winstreak |
| `/tags <name>` | Urchin/Seraph cheater tags |
| `/ws <name>` | Winstreak (current + historical highs per mode) |
| `/ping <name>` | Ping history |
| `/finals <count>` | Find players near a given finals count |
| `/beds <count>` | Find players near a given beds count |

Other
| Command | Description |
|---|---|
| `/1s` `/2s` `/3s` `/4s` `/44s` | Quick-join Bedwars Solos/Doubles/Threes/Fours/4v4 |
| `/sm [1-10]` | Send a random (or specific) snipe message |
| `/testapis` | Check API key status |
| `/setkey <type> <key>` | Set an API key |
| `/myign <name\|on\|off>` | Auto-lookup whoever pings your name |
| `/nick <name>` | Tell the proxy your current nick, so self-detection still works while nicked |
| `/safelist add\|remove\|preview\|clear\|autoadd <ign>` | Manage the safelist (never denicked, tagged, or flagged) |
| `/blocknicks` | Blocks every nicked player in your current game; unblocks resolved ones once it ends |
| `/antycheat [check]` | Toggle AntiCheat overall, or one specific check |

AntiCheat checks (`/antycheat <check>`)
| Check | Detects |
|---|---|
| `noslow` | Sprinting and blocking at once without the slowdown that should cause |
| `autoblockorangeb` | Attacking while still holding block up |
| `autoblockorangec` | Blocking perfectly timed right after taking a hit |
| `sprint` | Sprinting in a direction vanilla physics shouldn't allow |
| `scaff` | Placing blocks with a suspiciously brief crouch tap |
| `legitscaff` | Bridging faster than legitimately possible while aiming down |
| `scaffnoaim` | Bridging faster than legitimately possible without aiming down at all |
| `velocity` | Suppressed knockback after taking a hit |
| `fastmine` | Breaking blocks faster than any legitimate tool/enchant combo allows |
| `aimassist` | Suspiciously precise aim lock onto a target across several swings |

License

All rights reserved. No redistribution, modification, or reverse engineering permitted without written permission from the author.
