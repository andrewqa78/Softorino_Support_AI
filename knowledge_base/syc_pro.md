# SYC PRO / Softorino YouTube Converter

## SYC PRO — Quick Reference

### System Requirements
- **macOS:** 11.0 (Big Sur) or later, Intel Core i5+, 2GB RAM, 100MB disk
- **Windows:** Windows 10+, 1GHz processor, 2GB RAM, 100MB disk, .NET Framework
- **Windows only:** Apple Mobile Device Support drivers (auto-installed on install)

### Trial Limitations
- **macOS:** 3 video files during trial
- **Windows:** 24-hour unlimited trial

### Feature Limitations & Restrictions
- Requires internet connection and valid media URLs
- iPhone & Mac only (no iPad, iPod, or Android)
- Supports YouTube Shorts, videos, playlists, and tracks only
- Video output: MP4 only
- Audio output: MP3 or AAC only (no FLAC or WAV)
- No manual subtitle editor

---

## SYC PRO — Crash on Intel Mac when clicking "Download to this Computer"

### Summary

**Product:** SYC PRO for Mac
**Issue:** App crashes immediately when user clicks "Download to this Computer". Affects Intel (AMD64) Macs. Known bug -- was fixed in a subsequent update.

### Symptoms

- SYC PRO crashes the moment user clicks "Download to this Computer".
- EXC_BAD_ACCESS error when initializing local download paths.
- Issue may be intermittent at first (occasional crashes), then becomes consistent.
- Affects macOS Monterey on Intel Macs specifically.
- Crash may also occur with other destinations (Apple Music, Favorites).

### Common Customer Phrases

- "SYC PRO crashes when I click Download to this Computer."
- "It crashes no matter which destination I choose."
- "It worked before but now crashes every time."

### Questions to Ask

- Intel or Apple Silicon Mac?
- macOS version?
- SYC PRO version?
- Which download destination triggers the crash?

### Root Cause

Known bug affecting Intel Macs -- crash occurred at the moment SYC PRO tried to initialize local download paths (EXC_BAD_ACCESS). Fixed in a subsequent SYC PRO release.

### Resolution

1. First -- check for updates: open SYC PRO → Settings → Updates → Check for Updates. Install the latest version.
2. If update resolves the crash -- done.
3. If app is already on the latest version and still crashes: do a full clean reinstall using CleanAppsNow.
4. For Intel Macs, use the dedicated AMD64 download link: https://softorino.com/softorino-youtube-converter/download/amd64
5. After reinstall, activate via Universal License Dashboard.

### Escalate If

- Latest version installed and crash persists on Intel Mac.
- Crash happens on Apple Silicon Mac -- different root cause.

### Internal Notes

- This was a known Intel-specific bug -- confirmed fixed in a later build. Always check for updates first before doing a full reinstall.
- For Intel Macs, always use the AMD64-specific download link rather than the generic one.
- Do not suggest CleanAppsNow before first checking if an update is available -- the update alone may fix it.

---

## SYC PRO / Universal License — SYC² tile causes activation loop

### Summary

**Product:** SYC PRO / Universal License Dashboard
**Issue:** User activates from the wrong "SYC²" tile in the dashboard and gets stuck in an activation loop.

### Symptoms

- User is sent back to their email and then back to the dashboard repeatedly.
- The SYC logo shown during activation looks different from the SYC PRO logo.
- Activation never completes despite following all steps.
- User may have been using an old link or old dashboard bookmark.

### Root Cause

The Universal License Dashboard contains a legacy **SYC²** tile from an older app generation. This tile is no longer used for activating the current SYC PRO. Clicking Activate on it triggers a loop because the legacy app is no longer active.

### Resolution

1. Ask the user to open the Universal License Dashboard: https://softorino.com/submanager/
2. Scroll through the list of apps.
3. Find **Softorino YouTube Converter PRO** -- this is the correct tile.
4. Click **Activate** next to that tile specifically.
5. Tell the user to ignore the SYC² tile entirely.

### Internal Notes

- The SYC² tile and the SYC PRO tile have different logos -- users sometimes notice the difference and report it as suspicious. Explain that SYC² is the legacy version and only SYC PRO should be used.
- If the user has been activating from SYC², their activation attempts may not have registered against the correct app -- confirm in Shining.

---

## SYC PRO — Crash on Mac / vague crash description from user

### Summary

**Product:** SYC PRO for Mac
**Issue:** App crashes but user description is unclear or uses incorrect feature names.

### Symptoms

- User reports crash but describes it using terms that don't match SYC PRO features (e.g. "crashes when stats download" -- SYC PRO has no statistics feature).
- Crash may happen on launch, after pasting a link, during download, or after multiple downloads.
- User may attach a crash file in an unsupported format (.pages, .numbers, .key).

### Common Customer Phrases

- "The app crashes when it starts download."
- "It crashes when stats download." (no such feature -- needs clarification)
- "It keeps closing itself."
- "Crashes after some downloads."

### Questions to Ask -- Clarify When Exactly the Crash Happens

Always ask these before escalating:

1. Does the app crash immediately on launch?
2. Does it crash after you paste a YouTube link?
3. Does it crash while downloading, or only after the download completes?
4. Does it happen with every video or only certain ones?
5. Which version of SYC PRO? (SYC PRO → About SYC PRO in the menu bar)
6. Mac model and macOS version?

### Crash Report -- Accepted Formats

When requesting a crash report, specify the format explicitly. **Do not accept .pages, .numbers, or .key files** -- these are Apple iWork formats that support cannot open directly.

Ask for one of:
- PDF export of the report
- Screenshots of the crash report text
- The macOS crash log from Console.app (preferred -- most useful for developers)

**How to get the macOS crash log:**
1. Press Command + Space → search for **Console**
2. Open Console app
3. In the left panel, select **Crash Reports**
4. Find the most recent SYC PRO crash report
5. Export or copy the contents and send to support

### Root Cause Candidates

- TranscoderCore crash after multiple downloads (see existing SYC PRO crash entry)
- macOS / Apple Silicon compatibility issue
- Specific video URL or format triggering a crash
- Build-specific issue

### Escalate If

- Crash is reproducible with the same URL every time
- Multiple users with the same Mac model/chip report the same crash
- Crash log provided and crash occurs on launch with no user interaction

### Internal Notes

- SYC PRO does NOT have a "statistics" feature. If the user mentions this, ask them to clarify exactly what they were doing when the crash occurred.
- Always ask clarifying questions before escalating -- vague descriptions cannot be investigated by the dev team.
- Crash log from Console.app is far more useful than a screenshot of the app freezing.

---

## SYC PRO — Downloaded audio files do not appear in Music app (custom library path bug)

### Summary

**Product:** SYC PRO for Mac
**Issue:** Files download successfully but do not appear in the Music app. Transfer destination is "Music" but files land in the wrong directory.

### Symptoms

- SYC PRO reports a successful download/transfer.
- Files are not visible in Music app under "Date Added" or anywhere else.
- Files exist on the Mac (can be found in Finder) but not in the library the Music app is using.
- Moving files manually into Music library folders does not make them appear -- Music uses internal indexing, not direct file detection.
- Workaround the user may discover: download to Computer, then drag and drop into Music app manually.

### Common Customer Phrases

- "Downloads go nowhere."
- "Files don't show up in my Music library."
- "It's not at the latest date added."
- "I can drag and drop manually but that's too many steps."
- "The transfer completes but nothing appears in Music."

### Questions to Ask

- Does the Music app use a custom or non-default library location?
- Has the user ever held Option while opening Music to select a different library?
- Does the issue happen with every download or only specific ones?
- What Mac chip and macOS version?

### Root Cause

Known bug. SYC PRO saves downloaded files to a default Music library path. If the Music app is configured to use a different (custom or alternative) library location, the files land in the wrong directory and Music never indexes them.

Even manually moving files into the Music media folder does not help -- Music app requires files to be properly imported through its internal indexing, not placed by hand.

### Resolution

1. Acknowledge this is a known issue -- do not ask the user to repeat the transfer or reinstall the app.
2. Confirm whether Music app uses a custom library: ask if they have ever chosen a different library on launch (hold Option when opening Music).
3. Workaround until fixed:
   - In SYC PRO, set the destination to **Computer** instead of Music.
   - Once downloaded, open Music app and drag the file from Finder directly into the Music library window.
   - This is extra steps but is the only reliable method currently.
4. Escalate to dev team if not already logged -- include macOS version, Music library setup, and whether the default library path is in use.

### Escalate If

- User confirms Music app uses the default library but files still do not appear.
- Issue reproduces with default Music library location (this would indicate a different root cause).

### Internal Notes

- This is a **known bug**: [macOS][SYC PRO][Music Integration] -- filed internally.
- Confirmed on both Intel and Apple Silicon Macs -- not hardware-specific.
- Do not suggest reinstalling SYC PRO or iTunes -- not relevant.
- Do not tell user to manually place files in Music folders -- Music does not detect files placed directly in the filesystem.
- The only working workaround: download to Computer → drag into Music app manually.
- **2026-06-01, remote session (user: Martin):** Confirmed that users with multiple Music libraries on Mac may have SYC PRO writing to a non-primary (non-active) library -- the one not currently loaded in Music app.
- Moving files manually between Music library folders does not restore visibility -- Music uses internal indexing and will not pick up files placed directly on the filesystem.
- Root cause is a product-side limitation with how SYC PRO handles non-standard or multiple Music library setups, not user error.
- Dev team notified; fix planned for a future update.

---

## SYC PRO — Activation successful but user thinks activation failed

### Summary

**Product:** SYC PRO
**Issue:** Activation successful but user thinks activation failed

### Symptoms

- Screenshot shows green success message.
- Text says "SYC PRO Activated — Your license has been successfully verified."
- User still asks for activation help.

### Common Customer Phrases

- "It keeps saying I need to activate."
- "I followed the steps."

### Questions to Ask

- What appears after clicking Close?
- Does the app open after success message?

### Root Cause Candidates

- User misunderstands success screen.
- Next step is to close activation window and use app.

### Resolution

1. Tell user activation succeeded.
2. Ask them to click Close.
3. Open YouTube in browser, copy URL, let SYC PRO detect it.
4. Ask for screenshots only if problem happens after success screen.

### Escalate If

- App still asks for activation after success message and restart.

### Internal Notes

- Do not escalate if screenshots clearly show activation success.

---

## SYC PRO for Windows — iOS compatibility driver installation loop

### Summary

**Product:** SYC PRO for Windows
**Issue:** iOS compatibility driver installation loop

### Symptoms

- App repeatedly installs iOS compatibility driver.
- User restarts and gets same prompt.
- App never opens normally.

### Common Customer Phrases

- "Stuck installing iOS compatibility driver."
- "It keeps asking me to restart."

### Questions to Ask

- Is iTunes installed? Microsoft Store or Apple standalone?
- Does iTunes launch and detect device?

### Root Cause Candidates

- Missing/corrupted Apple drivers.
- Microsoft Store iTunes lacks required components for app.

### Resolution

1. Uninstall Microsoft Store iTunes if present.
2. Install standalone iTunes from Apple using official direct installer.
3. Open iTunes once.
4. Restart PC.
5. Open SYC PRO again.

### Escalate If

- Standalone iTunes works and detects device but SYC still loops.

### Internal Notes

- Same iTunes standalone link as WALTR Windows driver cases.

---

## SYC PRO — Oops, something went wrong for YouTube URL

### Summary

**Product:** SYC PRO
**Issue:** Oops, something went wrong for YouTube URL

### Symptoms

- App fails parsing YouTube video.
- Shows "Oops, something went wrong."
- May work with VPN or different region.

### Common Customer Phrases

- "Cannot download this URL."
- "Oops Something Went Wrong."
- "It worked before but now fails."

### Questions to Ask

- Does it fail for every YouTube link or only specific links?
- Does VPN change the result?
- What country/city?
- YouTube or YouTube Music?

### Root Cause Candidates

- YouTube regional restriction.
- IP flagged/rate-limited by YouTube.
- Specific URL parsing issue.
- Unsupported YouTube Music.

### Resolution

1. Ask for failing link and region.
2. Ask user to restart router to get new IP if dynamic IP.
3. Ask to test with VPN.
4. Clarify YouTube Music is not supported.
5. Record URL for future updates.

### Escalate If

- All YouTube videos fail for many users.
- Same URL fails across regions.
- Known parser outage.

### Internal Notes

- Do not promise immediate fix. Say link/region will be considered in future updates.

---

## SYC PRO — Crash after multiple downloads / transcoder crash

### Summary

**Product:** SYC PRO
**Issue:** Crash after multiple downloads / transcoder crash

### Symptoms

- App crashes after several downloads, sometimes after 10--15 MP3 files.
- Crash logs show transcoder-related libraries.
- May affect Intel or Apple Silicon separately.

### Common Customer Phrases

- "It crashes after some downloads."
- "Works for a while, then closes."

### Questions to Ask

- Mac model Intel or Apple Silicon?
- Does it happen with all videos or specific links?
- Audio/video format and quality?
- Destination: Computer, Music, or device?
- Can user provide URLs?

### Root Cause Candidates

- TranscoderCore crash.
- Specific media format problem.
- Memory/resource buildup after repeated downloads.

### Resolution

1. Ask for exact URLs, selected quality, destination, Mac type.
2. Suggest temporary pauses between batches.
3. Suggest restarting app between large batches as workaround, framed carefully.
4. Forward crash logs to dev team.

### Escalate If

- Crash reproducible with same URL.
- Multiple users with same processor/build.

### Internal Notes

- Avoid saying "just restart after every 15 files"; frame as temporary stability workaround.

---

## SYC PRO — Wi-Fi device search stuck on "Searching for devices via Wi-Fi" (macOS Tahoe)

### Summary

**Product:** SYC PRO for Mac
**Issue:** SYC PRO stays stuck on "Searching for devices via Wi-Fi" and cannot detect devices, even though Mac's internet/Wi-Fi is working. Seen frequently on macOS Tahoe 26.3.1.

### Symptoms

- SYC PRO shows "Searching for devices via Wi-Fi" indefinitely.
- Mac's internet connection is fully functional.
- SYC PRO is NOT listed under System Settings → Privacy & Security → Local Network.
- Connection may have worked once, then stopped working the next day (intermittent access revocation).
- Firewall and/or VPN may be active.

### Common Customer Phrases

- "SYC cannot connect to Wi-Fi on my Mac."
- "It's searching for Wi-Fi but cannot find anything."
- "My Wi-Fi is working -- I'm browsing the internet just fine."
- "SYC Pro is not listed in Local Network settings."
- "It connected once but stopped working the next day."

### Questions to Ask

1. Which exact version of SYC PRO are you using? (SYC PRO → About in menu bar)
2. Does the app stay on "Searching for devices via Wi-Fi" indefinitely, or does it time out with an error?
3. Is SYC PRO listed under System Settings → Privacy & Security → Local Network?
4. Are you running a VPN? If so, which one?
5. Have you tried a full uninstall and reinstall of SYC PRO?

### Root Cause Candidates

- **macOS Tahoe Local Network permission not granted**: SYC PRO relies on macOS network discovery (Bonjour/mDNS) to find iOS devices on the local network. macOS must grant Local Network permission for this to work. On Tahoe, the permission prompt may not have appeared, or may have been revoked after first use.
- **Important**: Apps cannot be manually added to the Local Network list. macOS adds them automatically when an app first requests access. If SYC PRO is not listed, macOS hasn't yet registered the permission -- a restart of the app and Mac is needed to re-trigger the prompt.
- **VPN or Firewall blocking mDNS**: VPN splits or kills local network discovery. macOS Firewall may block incoming connections required by SYC PRO.
- **Tahoe-specific regression**: macOS Tahoe 26.3.1 appears to be stricter about local network permissions and may revoke them between sessions.

### Resolution

1. Confirm both the Mac and the iOS device are on the same Wi-Fi network (same router, same band).
2. Fully quit any VPN app running on the Mac.
3. Disable Firewall: System Settings → Network → Firewall → Turn Off.
4. Check Local Network: System Settings → Privacy & Security → Local Network.
   - If SYC PRO is listed: make sure the toggle is ON.
   - If SYC PRO is NOT listed: this is expected on first run or after permission reset. Restart SYC PRO and then restart the Mac -- macOS should trigger the permission prompt automatically on relaunch.
5. Reopen SYC PRO after restart and check if it now finds devices.
6. If still failing after steps 1--5: ask for the SYC PRO version, a screenshot of the Wi-Fi settings page, and whether a full reinstall has been attempted.

### Escalate If

- All steps above attempted and SYC PRO still does not appear in Local Network after multiple restarts on Tahoe.
- User has no VPN, firewall is off, both devices on same network -- still stuck indefinitely.
- Issue reproduces consistently after each Mac restart (permission keeps getting revoked by macOS).
- Screenshots provided confirm firewall is off and Local Network list does not include SYC PRO even after reinstall.

### Internal Notes

- SYC PRO does not directly control Wi-Fi -- it relies on macOS network discovery. If macOS can't discover the target device, SYC PRO won't see it either.
- Do NOT tell customers they can manually add SYC PRO to the Local Network list -- they cannot. macOS populates that list automatically when an app first triggers the permission request.
- The "Wi-Fi searching" feature is for detecting iOS devices on the local network to transfer content to them. If the customer has no iOS device and is only downloading to their Mac, the Wi-Fi section is irrelevant -- clarify this to avoid confusion.
- Customers on macOS Tahoe may confuse "can't connect to Wi-Fi" (internet) with "SYC PRO can't find devices via Wi-Fi" (local network discovery). Clarify the distinction early.
- Ticket reference: pjunice@aol.com, May--June 2026, macOS Tahoe 26.3.1 -- escalated to tech team, unresolved at time of writing.

---

## SYC PRO — Classic iPod / non-iOS device transfer limitation

### Summary

**Product:** SYC PRO
**Issue:** Classic iPod / non-iOS device transfer limitation

### Symptoms

- Customer wants transfer to iPod Classic or older iPod.
- Downloaded songs do not appear on device.
- Device support unclear.

### Common Customer Phrases

- "SYC PRO does not recognize my iPod."
- "Files download but not on iPod."

### Questions to Ask

- Which iPod generation/model?
- Does iTunes/Finder see the iPod?
- Does transfer to Computer work?

### Root Cause Candidates

- Some older non-iOS iPods may not be fully supported in current SYC PRO transfer flow.
- Feature may be planned but not currently available.

### Resolution

1. Clarify current limitation gently.
2. Suggest downloading to Computer first.
3. If supported by iTunes, user may manually sync through iTunes.
4. Mention team may expand support in future, no ETA.

### Escalate If

- App claims support for model but fails consistently.

### Internal Notes

- Do not overpromise older iPod compatibility.
