# Bin Zayed Bot — Privacy Policy

**Effective date:** July 27, 2026
**Last updated:** July 27, 2026

Bin Zayed Bot ("the Bot", "we", "us", "our") is a Discord moderation, economy, and gaming bot built for private server use.

This Privacy Policy explains what Discord-related data the Bot processes, why, where it is stored, and how it can be removed.

---

## 1. Scope

This Privacy Policy applies only to Bin Zayed Bot and the server(s) it is installed on. It applies to:

- The Discord bot application itself
- Local data files it stores on its hosting provider (Render / Railway)
- Images and GIFs it generates on request (roulette wheels, mafia role cards)

By using Bin Zayed Bot in a server, you acknowledge that limited data described below may be processed as part of normal operation.

---

## 2. Data We Collect and Process

The Bot only stores what specific features require. It does **not** archive general server messages, does **not** use any external database service, and does **not** use Discord's Message Content for anything other than reading prefix commands and game answers typed directly to it.

### Account and server data
- Discord User IDs (to track balances, warns, permissions, game stats)
- Guild role IDs (only for the `-صلاحيات` permission system, to check who can use which command)
- Usernames (displayed in embeds; not stored longer than needed to show a message)

### Economy and games data
- Currency balance, level, and XP per user
- Shop purchase history (item IDs bought)
- Warn records (moderator ID, reason, timestamp)
- Session point totals (from the `-ps` / `-نقاط` / `-reset` commands)
- Mafia game statistics (wins/losses/games played per user)
- Command-role permission mappings (which roles can use which commands)

### Message content
The Bot reads message content only when a feature needs it directly, specifically:
- Reading prefix commands (e.g. `-حظر`, `-رصيد`)
- Reading answers typed during games (e.g. `-اسرع`, `-فكك`, `-ريبلكا`)
- Reading a player's defense message during a Mafia trial (other messages sent during that 15-second window may be deleted by the Bot as part of the game's rules, if it has permission to do so)

The Bot does **not** log, archive, or forward general conversation to any external service. It does not read or process Direct Messages.

### Generated images
Some features generate an image or GIF on the fly (e.g. `-روليت`'s spinning wheel, Mafia's role-distribution card). These are created locally at the moment of the command and sent directly as a Discord attachment. They are not stored afterward and contain no personal data beyond what is already visible in the game (usernames/mentions already shown in the channel).

---

## 3. How We Use Data

Data is processed only to:
- Run moderation commands (ban, kick, mute, warn, clear)
- Operate the economy system (balance, daily rewards, shop, leaderboard)
- Run games and track scores/results
- Enforce the server's custom command-permission settings
- Fix bugs and keep the Bot running reliably

We do not sell data. We do not use it for advertising. We do not share it with any third party except the hosting provider running the Bot's server (Render or Railway), which simply runs the Node.js process and stores its data files.

---

## 4. Where Data Is Stored

Unlike bots that use external databases (MongoDB, Redis, etc.), Bin Zayed Bot stores all of its data in simple local JSON files on its hosting provider's disk:

- `economy.json` — balances, XP, levels, inventory
- `warns.json` — moderation warnings
- `permissions.json` — command/role access rules
- `points.json` — temporary session points
- `mafia_stats.json` — mafia win/loss records
- `shop.json` — shop item catalogue

These files live only on the server the Bot is hosted on (Render or Railway) and are not synced to any third-party analytics, logging, or data-broker service.

---

## 5. Privileged Gateway Intents

### Guild Members Intent
Used to check role membership for the permission system and to fetch member info needed for moderation and game commands.

### Message Content Intent
Used only for prefix commands and in-game answers, as described in Section 2. Not used for general message monitoring.

---

## 6. Data Retention

- Economy balances, warns, permissions, and mafia stats are kept until manually reset by a server admin or removed by deleting the relevant JSON file on the host.
- Session points (`-ps`/`-نقاط`) are meant to be temporary and can be wiped anytime with `-reset`.
- Generated images/GIFs are not retained after being sent — they exist only in memory during the command and are discarded immediately after.

---

## 7. Your Rights

Since all data is stored locally under the server owner's own hosting account (not a shared third-party database), a server admin can view, edit, or delete any of the JSON data files at any time through their hosting dashboard. If you are a member of a server using this Bot and want your data removed, contact that server's admin — they have direct control over the data since it lives on their own hosting instance.

---

## 8. Changes to This Policy

This document may be updated as the Bot's features change. Check the file's "Last updated" date above.

---

## 9. Contact

For questions about this policy, contact the server owner or bot operator directly.
