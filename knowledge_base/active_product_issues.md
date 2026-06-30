# ACTIVE PRODUCT ISSUES (TEMPORARY)

## ⚠️ IMPORTANT — READ BEFORE HANDLING ANY TICKET

This file contains **temporary product issues only**.

- Check this file **first**, before reading any product KB file.
- If the customer's issue matches an entry here — follow the AI Response Instructions in that entry. Do **not** run standard troubleshooting.
- These entries **must be removed immediately** after a fix is released.
- Do **not** convert these entries into permanent Knowledge Base articles.
- If an entry is marked **RESOLVED** — delete it entirely. Do not leave it in the file.

---

## SYC PRO — "Oops! Something went wrong :(" for music-related YouTube content

**Status: ACTIVE — Temporary issue. No ETA available.**

### Issue

Some YouTube content triggers the error:

> "Oops! Something went wrong :("

### Affected Content

Mostly affects:
- Songs
- Music videos
- Playlists
- Children's songs
- Worship songs
- Similar music-related content

Regular YouTube videos (non-music) usually continue to work normally.

### Root Cause

Recent changes on YouTube's side currently prevent certain videos from being properly analyzed by SYC PRO.

This is **NOT** caused by:
- Universal License
- Customer account
- VPN, Firewall, or Antivirus software
- Proxy settings
- Local computer configuration

### AI Response Instructions

✅ **DO:**
- Inform the customer this is a known temporary issue.
- Tell them it is already documented internally and under investigation.
- Tell them there is no ETA for a fix at this time.

❌ **DO NOT:**
- Ask the customer to reset their license.
- Ask them to reinstall SYC PRO or iTunes.
- Ask them to disable antivirus, VPN, or firewall.
- Promise a release date.
- Run any standard "Oops" troubleshooting from the SYC PRO KB.

### Customer Response Template

> We are aware of this issue. Some YouTube content -- primarily music-related videos and playlists -- may currently trigger the "Oops! Something went wrong :(" message in SYC PRO.
>
> This is a temporary issue related to recent changes on YouTube's side and is already being investigated by our team.
>
> Unfortunately, we do not have an ETA for a fix at this time, but we will notify users once an update is available.

---

⚠️ **MAINTENANCE NOTE: REMOVE THIS ENTIRE ENTRY IMMEDIATELY AFTER A FIX IS RELEASED.**

---

## BEAMER — UI controls unresponsive on macOS Tahoe (4.2.0)

**Status: ACTIVE — Temporary issue. No ETA available.**

### Issue

On macOS Tahoe (26.x), Beamer 4.2.0 main UI controls (play/pause, stop, subtitles, and other primary controls) are not clickable/responsive during AirPlay streaming.

### Affected Content

- Confirmed with AirPlay to Apple TV 4K (tvOS 26.x) from a Mac running macOS Tahoe.
- Audio may play while video does not appear, inconsistently across attempts.
- Once one piece of media has played, subsequent media in the same session may fail to play at all.
- Play/pause/stop via the Apple TV remote still works -- only the in-app Beamer controls are affected.

### Root Cause

Compatibility issue between Beamer 4.2.0 and macOS Tahoe. Confirmed still present in the latest shipped build as of this writing (Beamer 4.2.0, also reproduced on macOS 26.5.2). Not specific to one Mac model or chip.

This is **NOT** caused by:
- License or activation
- The customer's Apple TV/Chromecast configuration
- A specific media file

### AI Response Instructions

✅ **DO:**
- Confirm this is a known, currently unresolved compatibility issue with macOS Tahoe specifically (not other macOS versions).
- Tell the customer the team is aware and actively working on it.
- Tell them there is no ETA for a fix at this time.
- If asked why Beamer is still being promoted/sold while broken on Tahoe: explain that Beamer continues to work normally for users on other supported macOS versions, and the issue is specific to certain newer macOS releases.

❌ **DO NOT:**
- Offer a discount, refund, or any compensation specifically tied to this issue -- not currently authorized.
- Promise a release date.
- Run standard AirPlay/Chromecast/streaming troubleshooting from `other_products.md` -- this is a confirmed app/OS compatibility issue, not a setup problem.
- Suggest downgrading macOS as a fix.

### Customer Response Template

> Thank you for confirming. You're right that this issue is not yet resolved -- we're aware of a compatibility problem between Beamer and macOS Tahoe that affects the main playback controls (play/pause, stop, subtitles) during AirPlay streaming.
>
> Beamer continues to work normally for users on other supported macOS versions, which is why it remains available -- the issue is specific to certain newer macOS releases, including Tahoe.
>
> Our team is aware of this and actively working on a fix, but we don't have an ETA to share at this time. We'll let you know as soon as there's an update.

---

⚠️ **MAINTENANCE NOTE: REMOVE THIS ENTIRE ENTRY IMMEDIATELY AFTER A FIX IS RELEASED. If a permanent Beamer-specific troubleshooting case is ever needed after this is resolved, file it under `other_products.md` -- Beamer has no dedicated product MD file.**
