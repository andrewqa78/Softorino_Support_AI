# WALTR PRO

## WALTR PRO — Quick Reference

### System Requirements
- **macOS:** 10.15 (Catalina) or later, Intel Core i5+, 2GB RAM, 200MB disk
- **Windows:** Windows 10+, 1GHz processor, 2GB RAM, 200MB disk
- **Windows only:** Apple Mobile Device Support drivers (auto-installed on install)

### Trial Limitations
- Books/PDFs: 10 files
- Movies: 1 file
- TV Shows: 3 files
- Music: 10 files
- Ringtones: 2 files
- Files via Alternative Apps: Unlimited

### Feature Limitations & Restrictions
- Apple devices only (iPhone, iPad, iPod) -- no Android
- Files must be dropped into supported destination tiles
- AI metadata works best with known media -- may not tag niche or obscure files
- Hi-Res audio up to 192kHz (DSD limits not confirmed)
- Manual metadata editing: hold Cmd (⌘) while dropping a file
- ACR & AI features require internet access

---

## WALTR PRO for Windows — Crash on startup / app cannot be opened at all (new install)

### Summary

**Product:** WALTR PRO for Windows
**Issue:** App crashes immediately on startup and shows error report dialog. User cannot open the app at all.

### Symptoms

- App shows crash/error report dialog immediately on launch.
- User cannot reach the main interface or activation screen.
- Reinstalling via standard uninstall does not fix the crash.
- Issue appears on a fresh install for a new Universal License user.

### Common Customer Phrases

- "I keep getting an error message when I try to open it."
- "The error report box keeps appearing."
- "I reinstalled it and it still crashes."

### Questions to Ask

- Windows version?
- Is iTunes installed? If yes, from Microsoft Store or Apple's website?
- Does the crash happen before any device is connected?

### What NOT to Ask

- **Do not ask for the app version** -- if the app crashes on startup, the user cannot access the About window. This is an impossible request and wastes a reply.

### Root Cause Candidates

- Missing Apple components (CoreFoundation.dll, Apple Mobile Device Support) -- same as WALTR PRO startup crash pattern.
- Corrupted installer or incompatible build with the user's Windows configuration.
- Newer build compatibility issue on specific Windows setups.

### Resolution

1. Do not ask for app version -- the user cannot open the app.
2. Ask if iTunes is installed and whether it's from Microsoft Store or Apple's website.
3. If no iTunes or Microsoft Store iTunes: install standalone iTunes first, restart PC, then test WALTR PRO again.
4. If reinstall is needed: send the **official current download link** -- https://ushining.softorino.com/download.php?abbr=wpm -- NOT the earlier-versions link. New Universal License users should always get the latest build.
5. If older build resolves the crash (app opens): the issue is a compatibility problem with the latest build on that specific Windows setup. Escalate to dev team with Windows version details.
6. Once app opens, guide user to activate via the License Dashboard: https://softorino.com/submanager/

### Escalate If

- Standalone iTunes is installed and app still crashes.
- Older build opens but latest build crashes consistently.

### Internal Notes

- **Never send earlier-versions links to new Universal License users.** Earlier-versions are for legacy license holders only. New users should always install from the official download link or the License Dashboard.
- If the user mentions CoreFoundation.dll error specifically, follow the WALTR PRO Windows CoreFoundation.dll entry.

---

## WALTR PRO for Windows — Crash on startup / corrupted Apple components or iTunes library

### Summary

**Product:** WALTR PRO for Windows
**Issue:** WALTR PRO crashes on launch. Apple components appear installed but don't function correctly. May also be caused by an outdated Windows version.

### Symptoms

- WALTR PRO crashes on startup with error reporter.
- iTunes may also fail to launch.
- .NET Framework 4.8 appears installed but is not detected by WALTR PRO.
- System is running a very old Windows 10 build (e.g. 1903/build 18362 from 2019).
- Apple drivers appear present in Device Manager but do not work correctly.
- Issue persists after standard reinstall.

### Common Customer Phrases

- "I get an error message every time I try to open it."
- "I reinstalled and still get the error."
- "It says .NET is installed but the app won't open."
- "I'm using a Windows tablet."

### Root Cause Candidates

- Corrupted Apple components (iTunes, Apple Mobile Device Support, Bonjour, Apple Application Support).
- Damaged iTunes library file (`iTunes Library.itl`) preventing iTunes from launching, which cascades into WALTR PRO failure.
- Very old Windows 10 build -- components like .NET 4.8 may appear installed but are not properly registered. Updating to a current Windows build (22H2 or later) can resolve this.
- Windows tablet running ARM or S Mode -- WALTR PRO may not be compatible.

### Resolution

**Step 1 -- Check Windows version first:**
1. Press Win + R → type `winver` → press Enter.
2. If the build is older than 19041 (Windows 10 2004): update Windows first via Settings → Update & Security → Windows Update → Check for updates. This alone may resolve the issue.

**Step 2 -- Full Apple component removal and reinstall:**
3. Uninstall all Apple components: iTunes, Apple Mobile Device Support, Apple Application Support, Bonjour, Apple Software Update.
4. Restart the PC.
5. Install standalone iTunes from Apple: https://secure-appldnld.apple.com/itunes12/047-76416-20260302-fefe4356-211d-4da1-8bc4-058eb36ea803/iTunes64Setup.exe
6. Open iTunes and confirm it launches.

**Step 3 -- If iTunes fails to launch (library error):**
7. Close iTunes.
8. Navigate to `Documents\iTunes\`.
9. Rename `iTunes Library.itl` to `iTunes Library.old`.
10. Launch iTunes again -- it will create a new library automatically.
11. Confirm iTunes opens correctly and detects the device.

**Step 4 -- Launch WALTR PRO:**
12. After iTunes is working, launch WALTR PRO.
13. Activate via the License Dashboard if needed.

**If all steps above fail:** escalate to @AndrewQA. This environment issue requires direct inspection by a human agent.

### Escalate If

- Windows is up to date, Apple components reinstalled, iTunes library reset -- and WALTR PRO still crashes.
- Device is a Windows tablet running ARM or S Mode -- WALTR PRO may not be supported.

### Internal Notes

- `iTunes Library.itl` corruption is a common hidden cause. The error message is usually: "The file iTunes Library.itl cannot be read because it was created by a newer version of iTunes" or similar library/database error.
- Renaming the .itl file and relaunching iTunes creates a fresh library without losing media files.
- Old Windows 10 builds (pre-2020) can cause .NET 4.8 to appear installed but not function -- updating Windows is the fix, not .NET reinstall.
- Windows tablets may run ARM processors or S Mode -- always ask the user to check Settings → System → About and confirm the device type and Windows edition.
- When multiple standard steps have failed and the issue appears environment-specific, escalate to @AndrewQA. Do not offer remote sessions -- those are conducted only by human agents.

---

## WALTR PRO for Windows — Crash on startup / blocked by antivirus or security software

### Summary

**Product:** WALTR PRO for Windows
**Issue:** App installs successfully but crashes immediately on launch. White screen appears for 1-2 seconds then error reporter shows up. Reinstalling does not help.

### Symptoms

- App opens briefly (white screen 1-2 seconds) then crashes.
- Error report dialog appears immediately after crash.
- Issue persists after multiple reinstalls.
- User may have aggressive antivirus or security software installed.
- DISM, registry cleaners, and system cleanup tools do not resolve the issue.

### Common Customer Phrases

- "White screen appears and then error report."
- "I installed it but it won't open."
- "I've reinstalled it multiple times."
- "Could leftover files in the Registry be the problem?"

### Root Cause Candidates

- **Antivirus or security software blocking WALTR PRO components on launch** -- most common cause when app briefly appears then immediately crashes.
- Two or more security suites running simultaneously increases the chance of conflict.
- VPN software may also interfere with activation or network components.
- Leftover registry entries from previous installs (less common but possible).
- Missing Apple drivers (CoreFoundation.dll) -- see separate entry.

### Resolution

**First -- check for security software conflict:**
1. Ask the user if they have any antivirus, internet security suite, or VPN software installed.
2. Ask them to **temporarily disable all security software and VPN**.
3. Try launching WALTR PRO again.
4. If the app opens: the security software was the blocker. Add WALTR PRO as an exception/whitelist entry in each security program, then re-enable them.

**If security software was not the issue:**
5. Run the SYC diagnostic: ask the user to install Softorino YouTube Converter. If it opens normally, the Apple components on the system are functional and the crash is isolated to WALTR PRO. If SYC also crashes, follow the CoreFoundation.dll entry -- the Apple components are the problem.
6. Check Apple drivers -- is iTunes installed? If not, install standalone iTunes from Apple (see Appendix link).
7. If iTunes is installed but app still crashes, follow the CoreFoundation.dll entry.

**Registry / leftover files:**
7. If the user suspects leftover registry entries: recommend a clean uninstall using the built-in WALTR PRO uninstaller from `C:\Program Files\WALTR PRO\`, reboot, then fresh install.
8. Do not ask non-technical users to manually edit the registry -- this is risky and unlikely to be necessary.

### Escalate If

- Security software disabled and app still crashes immediately.
- iTunes installed and drivers confirmed working but crash persists.
- User has tried clean install multiple times with the same result.

### Internal Notes

- When a user mentions antivirus/VPN software, address it immediately -- do not skip to activation steps if the app cannot even open.
- Fortect Security, Aura Ultimate, Norton, McAfee, Bitdefender are all known to block app components aggressively.
- Do not send the user to click "Reset" or "Activate" in the dashboard if the app crashes before it reaches the activation screen -- those steps are irrelevant until the app actually opens.
- DISM and Windows system cleanup do not fix security software blocking -- redirect the user to the antivirus exception approach.

---

## WALTR PRO for Windows — Crash on startup / CoreFoundation.dll missing

### Summary

**Product:** WALTR PRO for Windows
**Issue:** Crash on startup / CoreFoundation.dll missing

### Symptoms

- WALTR PRO does not launch.
- Crash Reporter appears immediately.
- User cannot reach activation screen.
- Application closes before device connection.

### Common Customer Phrases

- "WALTR PRO won't start."
- "I get Crash Reporter every time."
- "Unable to load DLL CoreFoundation.dll."
- "CoreFoundation.dll could not be found."

### Questions to Ask

- Does iTunes launch successfully?
- Was iTunes installed from Microsoft Store or Apple standalone installer?
- Windows version?

### Root Cause Candidates

- Missing/corrupted Apple Application Support.
- Missing CoreFoundation.dll.
- Incomplete iTunes installation.
- Apple Mobile Device Support damaged.

### Resolution

1. Uninstall Microsoft Store iTunes if present.
2. Install standalone iTunes from Apple: https://secure-appldnld.apple.com/itunes12/047-76416-20260302-fefe4356-211d-4da1-8bc4-058eb36ea803/iTunes64Setup.exe
3. Open iTunes once and confirm it launches.
4. Restart PC.
5. Launch WALTR PRO again.

### Escalate If

- iTunes launches but WALTR PRO still crashes.
- CoreFoundation error remains after standalone iTunes reinstall.
- App opened after Apple component reinstall but crashed again after a short session (CoreFoundation.dll error returns on next launch).

### Internal Notes

- This is a Windows Apple component issue, not a Softorino license issue.
- **SYC diagnostic:** If it is unclear whether the issue is system-wide or WALTR PRO-specific, ask the user to install Softorino YouTube Converter. If SYC opens normally, the Apple components are functional and the issue is isolated to WALTR PRO. This saves multiple reinstall cycles.
- **Temporary fix pattern:** In some cases, a full Apple component reinstall (uninstall iTunes + Apple Mobile Device Support + Apple Application Support + Bonjour → restart → fresh standalone iTunes) allows WALTR PRO to launch and run briefly, but it crashes again on the next session with the same CoreFoundation.dll error. This indicates the component reinstall was incomplete or Windows failed to register the DLLs properly. Escalate to @AndrewQA if this happens.

---

## WALTR PRO for Windows — Activation button does not save activation

### Summary

**Product:** WALTR PRO for Windows
**Issue:** Activation button does not save activation

### Symptoms

- License Dashboard opens.
- Customer clicks Activate near WALTR PRO.
- Button changes color and returns.
- App opens but asks to activate when transferring.

### Common Customer Phrases

- "I click Activate and nothing happens."
- "I already downloaded it."
- "WALTR asks for activation again."

### Questions to Ask

- Does backend show activation event?
- Does issue affect only WALTR PRO?
- Does user accept cookies?
- Windows version?

### Root Cause Candidates

- Backend activation not saved.
- Browser session/cookies blocking.
- Local license files corrupted.

### Resolution

1. Close WALTR PRO.
2. Go to C:\ProgramData\Softorino\WALTR PRO\.
3. Delete all files in that folder, especially license.dat/license2.dat/license3.dat/settings.dat.
4. Open License Dashboard in incognito/private browser.
5. Click Activate next to WALTR PRO.
6. Launch WALTR PRO and test transfer.

### Escalate If

- Backend still shows no activation attempt.
- Customer cannot use dashboard at all.
- All standard steps exhausted -- escalate to @AndrewQA.

### Internal Notes

- If local reset + incognito activation both fail, escalate to @AndrewQA. Do not offer remote sessions.

---

## WALTR PRO for Windows — iPad not detected after Microsoft Store iTunes install / trust prompt disappears instantly

### Summary

**Product:** WALTR PRO for Windows
**Issue:** iPad not detected after Microsoft Store iTunes was installed, even after switching to standalone iTunes. Trust prompt flashes briefly and disappears.

### Symptoms

- WALTR PRO worked on first install, stopped detecting iPad after Microsoft Store iTunes was installed.
- Standard fix (uninstall MS Store iTunes → install standalone iTunes) does not resolve the issue.
- Device Manager shows the iPad as a portable device ("Apple iPad").
- iPad prompts "Trust This Computer" but the trust dialog on Windows disappears almost instantly -- user cannot tap Trust on the iPad in time.
- iTunes also does not detect the iPad.
- Apple Devices app (Microsoft) also fails to connect.

### Common Customer Phrases

- "WALTR PRO doesn't see my iPad anymore."
- "It worked once and never again."
- "iTunes doesn't see it either."
- "The Trust window disappears before I can click anything."
- "Device Manager shows it but no app can connect."

### Questions to Ask

- Does iTunes detect the iPad? (critical -- if no, the issue is not WALTR PRO-specific)
- Does the trust prompt appear on the iPad? Does it stay long enough to tap?
- What cable is being used?
- What iPad model and iOS version?
- Did the issue start after a specific action (iTunes install, restart, iOS update)?

### Root Cause Candidates

- Microsoft Store iTunes leaves corrupted Apple service state even after uninstall.
- Apple pairing/trust session is broken at the Windows system level -- not a WALTR PRO issue.
- The trust handshake fails so fast the user cannot confirm it on the iPad.
- WALTR PRO relies on the same Apple services as iTunes; if iTunes fails, WALTR PRO also fails.

### Resolution

Standard path first:
1. Uninstall Microsoft Store iTunes.
2. Restart PC.
3. Install standalone iTunes from Apple: https://secure-appldnld.apple.com/itunes12/047-76416-20260302-fefe4356-211d-4da1-8bc4-058eb36ea803/iTunes64Setup.exe
4. Open iTunes, connect iPad, tap Trust when prompted.
5. Confirm iTunes detects the iPad before testing WALTR PRO.

If iTunes still does not detect the iPad:
6. Check Apple Mobile Device Service: Win + R → services.msc → find "Apple Mobile Device Service" → confirm Running and set to Automatic → Restart it.
7. Check Device Manager → Universal Serial Bus controllers → confirm "Apple Mobile Device USB Driver" is present with no warning icon.

If trust prompt disappears instantly / iPad still not paired:
8. On the iPad: Settings → General → Transfer or Reset iPad → Reset → Reset Location & Privacy.
9. Reconnect iPad and tap Trust This Computer when prompted.

If issue persists after all steps:
10. Ask user to test the iPad on another computer (Mac preferred).
11. If the iPad behaves the same on another computer -- the issue is at the iPad/iOS level. Recommend contacting Apple Support.

### Escalate If

- All steps completed, iTunes still does not detect the iPad, Reset Location & Privacy did not help.
- Behavior is the same on a second computer -- Apple Support is the correct next step.

### Internal Notes

- Key diagnostic: if iTunes also cannot detect the iPad, this is not a WALTR PRO bug. Do not keep troubleshooting WALTR PRO in isolation.
- Trust prompt flashing instantly = pairing broken at OS level, not a cable or app issue.
- Reset Location & Privacy on iPad resets all trusted computer records -- after this the iPad will ask to Trust again on every device, which is expected.

---

## WALTR PRO for Mac — Shows Intel application on Apple Silicon

### Summary

**Product:** WALTR PRO for Mac
**Issue:** Shows Intel application on Apple Silicon

### Symptoms

- macOS warns that app is Intel.
- User expected Universal/native Apple Silicon app.
- License/activation works normally.

### Common Customer Phrases

- "Why does WALTR PRO say Intel?"
- "Is there a Universal version?"
- "Rosetta support will end."

### Questions to Ask

- Does the app launch and work?
- Which macOS and Apple chip?
- Which WALTR PRO version?

### Root Cause Candidates

- Current WALTR PRO build runs via Rosetta on Apple Silicon.
- This is expected behavior, not activation failure.

### Resolution

1. Explain WALTR PRO currently runs through Rosetta.
2. Clarify license is not affected.
3. Mention team is working on native Apple Silicon support, no ETA unless confirmed.

### Escalate If

- User reports actual app crashes or functional failure.
- Rosetta warning appears with app unable to launch.

### Internal Notes

- Do not imply Universal License means Universal Binary architecture.

---

## WALTR PRO for Mac — Crash on launch/file drop on Intel Monterey

### Summary

**Product:** WALTR PRO for Mac
**Issue:** Crash on launch or file drop on macOS Monterey (Intel Mac). Known build compatibility issue with v4.0.122.

### Symptoms

- WALTR PRO v4.0.122 crashes instantly on startup or immediately when a file is dropped.
- Crash occurs before any device detection -- no iPhone needs to be connected.
- Error signature: EXC_BAD_ACCESS (SIGSEGV) / Segmentation fault: 11 at address 0x1c.
- Manual clean reinstall (clearing Application Support, Caches, Preferences) does not resolve the issue.
- Issue is specific to Intel Macs on macOS Monterey 12.x.

### Common Customer Phrases

- "WALTR PRO crashes instantly."
- "EXC_BAD_ACCESS at 0x1c."
- "Can you send an older stable build?"
- "I already did a clean uninstall and it still crashes."
- "The app crashes even without my phone connected."

### Questions to Ask

- macOS version (Monterey 12.x, Ventura 13.x, etc.)?
- Intel or Apple Silicon?
- WALTR PRO build version?
- Does crash happen without device connected?
- Can you share the crash log from Console.app?

### Root Cause Candidates

- Build-specific compatibility issue with WALTR PRO v4.0.122 on macOS Monterey Intel.
- Not related to device detection, licensing, or local app data.
- Crash occurs at the app component level before any user interaction.

### Resolution

If customer has NOT yet done a clean reinstall:
1. Ask them to use **CleanAppsNow** (included in Universal License) to fully remove WALTR PRO and all associated files. This is more thorough than manual deletion -- CleanAppsNow removes hidden Library files (Application Support, Caches, Cookies, HTTPStorages, Logs, Preferences, WebKit) that macOS users cannot access manually.
2. Open the Universal License Dashboard, install and activate CleanAppsNow.
3. In CleanAppsNow, select WALTR PRO -- all associated components will be listed on the right panel with checkboxes. Make sure all are checked before deleting.
4. Click Delete.
5. Restart the Mac.
6. Download and reinstall the latest WALTR PRO build from the License Dashboard.
7. Test if crash still occurs.

If customer has already done a manual clean reinstall AND crash persists:
7. Do not ask them to repeat reinstall steps -- it will not help.
8. Collect the crash log from Console.app if not already provided.
9. Confirm to the customer: the issue appears build-specific, the crash report has been forwarded to the dev team, and they will be updated when a workaround or stable older build is available.
10. Do not promise an ETA.

### Escalate If

- Multiple users report the same crash on Monterey Intel.
- CleanAppsNow reinstall also does not resolve the crash.
- Customer requests a refund due to the app being unusable.

### Internal Notes

- This is a **known build compatibility issue** with v4.0.122 on macOS Monterey Intel -- confirmed by the dev team.
- Do not suggest iTunes reinstall or driver troubleshooting -- not relevant for this crash.
- CleanAppsNow is part of the Universal License and removes all app components more reliably than manual deletion.
- If customer is frustrated after multiple follow-ups with no fix, acknowledge the delay directly and do not use generic "we're working on it" responses.
- Cross-reference: The same EXC_BAD_ACCESS (SIGSEGV) at 0x1c crash signature has been observed on Apple Silicon Macs running WALTR PRO v4.0.122 via Rosetta on macOS Sonoma 14.x, crashing during transfer rather than on launch. See "WALTR PRO for Mac — Crash during file transfer on Apple Silicon via Rosetta / macOS Sonoma (v4.0.122)".

---

## WALTR PRO for Mac — Crash during file transfer on Apple Silicon via Rosetta / macOS Sonoma (v4.0.122)

### Summary

**Product:** WALTR PRO for Mac
**Issue:** App crashes during file transfer on Apple Silicon Macs running WALTR PRO v4.0.122 via Rosetta on macOS Sonoma (14.x). Same crash signature as the Intel Monterey variant but triggered during transfer rather than on launch.

### Symptoms

- WALTR PRO v4.0.122 crashes during file transfer -- app may open normally but crash when a transfer starts.
- Crash occurs in the `com.softorino.bigsync` dispatch queue.
- Exception: EXC_BAD_ACCESS (SIGSEGV) / Segmentation fault: 11 at address 0x1c.
- Mac is Apple Silicon (e.g. M3, Mac15,12) running WALTR PRO via Rosetta (X86-64 Translated).
- macOS Sonoma 14.x.
- WALTR PRO version 4.0.122.

### Common Customer Phrases

- "WALTR PRO crashes when I try to upload anything."
- "The app crashes when I start a transfer."
- "I can open the app but it crashes when I try to use it."

### Questions to Ask

- Mac chip and macOS version?
- WALTR PRO version? (WALTR PRO → About WALTR PRO)
- Does the crash happen as soon as a transfer starts, or after some progress?
- Has a clean reinstall already been done?

### Root Cause Candidates

- Build-level bug in WALTR PRO v4.0.122 -- EXC_BAD_ACCESS at 0x1c in the bigsync transfer queue.
- Likely the same underlying bug as the v4.0.122 Intel Monterey crash, now confirmed to also affect Apple Silicon Macs via Rosetta on macOS Sonoma.
- Not related to device detection, licensing, or Apple driver issues.

### Resolution

1. Check for updates first: WALTR PRO menu bar → Check for Updates. Install the latest version if available.
2. If update resolves the crash -- done.
3. If already on the latest version and crash persists: do a full clean reinstall using CleanAppsNow (included in Universal License).
   - Install and activate CleanAppsNow from the License Dashboard.
   - In CleanAppsNow, select WALTR PRO, confirm all components are checked, click Delete.
   - Restart the Mac.
   - Download and reinstall WALTR PRO from the License Dashboard.
   - Test if crash still occurs.
4. If crash persists after clean reinstall: collect crash log from Console.app and escalate to dev team with Mac model, macOS version, and WALTR PRO version.
5. Do not promise an ETA for a fix.

### Escalate If

- Latest version installed and crash persists after clean reinstall.
- Multiple users on Apple Silicon / Sonoma report the same crash pattern.
- Customer requests a refund because the app is unusable.

### Internal Notes

- Same exception type and address (EXC_BAD_ACCESS SIGSEGV at 0x1c) as the confirmed v4.0.122 Intel Monterey crash. Likely the same build-level bug, now also seen on Apple Silicon via Rosetta on macOS Sonoma.
- Key difference from the Intel Monterey variant: crash occurs in `com.softorino.bigsync` during a transfer operation, not on launch or file drop.
- Mac15,12 = MacBook Pro M3 series. Runs WALTR PRO via Rosetta (X86-64 Translated) -- not a native Apple Silicon build.
- Do not suggest iTunes reinstall or driver troubleshooting -- not relevant.
- First confirmed case: Marie Verlinden, 2026-05-17, macOS 14.8 (23J21), Mac15,12, WALTR PRO 4.0.122.
- Cross-reference: See "WALTR PRO for Mac — Crash on launch/file drop on Intel Monterey" for the related Intel variant.

---

## WALTR PRO — Music transferred to Apple Music / cannot choose third-party app destination (e.g. Evermusic)

### Summary
**Product:** WALTR PRO (Mac and Windows)
**Issue:** User confused by "Where are my files?" pointing to Apple Music; wants to transfer to Evermusic or another unsupported third-party app.

### Symptoms
- "Where are my files?" shows an Apple Music library path on Mac.
- User believes their files require an Apple Music subscription to access.
- Music transferred to iPhone lands in Apple Music (the app), not in Files or a third-party app.
- User wants to transfer to Evermusic, Files app, or another app not in the supported list.
- Uninstalling Apple Music from iPhone does not change the transfer destination.

### Common Customer Phrases
- "I don't want Apple Music, I use Evermusic."
- "Where are my files shows Apple Music -- I don't have a subscription."
- "There's no way to specify where the files go on iPhone."
- "It defaults to Apple Music."
- "I uninstalled Apple Music and it still doesn't work."

### Questions to Ask
- Which third-party app do you want to use as the destination?
- Do you see a "Choose alternative apps" option in WALTR PRO?

### Root Cause Candidates
- "Where are my files?" shows the Mac Apple Music library path, not the destination on iPhone -- expected behavior, not an error.
- WALTR PRO transfers to Apple Music (the app) by default. Apple Music (the app) and Apple Music (the subscription) are different things -- no subscription is required.
- WALTR PRO supports a limited list of third-party destination apps via "Choose alternative apps." Apps not on the list cannot receive transfers directly.

### Resolution
1. Clarify: "Where are my files?" shows the Mac music library location, not the iPhone destination. This is not related to a subscription.
2. Explain: Apple Music (the app) and Apple Music (the subscription service) are separate. Files transferred to Apple Music are accessible without a subscription.
3. If the user wants a third-party destination: direct them to the "Choose alternative apps" feature in WALTR PRO.
4. Check if their desired app is in the supported list (see Internal Notes). If it is, guide them to select it before transferring.
5. If the app is not supported (e.g. Evermusic): tell the user WALTR PRO cannot transfer there directly at this time. Pass the feedback to the product team.
6. Do not suggest uninstalling Apple Music -- it has no effect on where WALTR PRO sends files.

### Escalate If
- User selected a supported alternative app but files do not arrive there.
- Transfer consistently fails for all supported alternative app destinations.

### Internal Notes
- Supported third-party apps via "Choose alternative apps" (as of 2026-06): Documents, VLC, Infuse, PlayerXtreme, PDF Expert, GoodReader, Kindle, VOX, FLAC Player+, AVplayer, PDFpen, PDF Pro 3, Adobe Acrobat, iMovie, Pages, Keynote, Numbers, ComicFlow, iComics, Files by WALTR.
- Evermusic is NOT currently supported.
- "Choose alternative apps" only shows apps the user already has installed on their iPhone.
- Never tell users to uninstall Apple Music as a fix -- it has no effect on WALTR PRO transfer behavior.
- Feedback about adding Evermusic or other apps should be passed to the product team.

---

## Waltr 2 Legacy — User sent wrong download link / WALTR PRO installed instead of Waltr 2

### Summary

**Product:** Waltr 2 (Legacy)
**Issue:** User installs WALTR PRO instead of Waltr 2 and activation key fails

### Symptoms

- User has a Waltr 2 license (5x5 key format: XXXXX-XXXXX-XXXXX-XXXXX-XXXXX).
- User downloaded WALTR PRO by mistake (or was sent the wrong link).
- Activation key does not work because the wrong app is installed.
- User reports "wrong serial number" or "key not accepted."

### Common Customer Phrases

- "The activation key is not working."
- "It shows wrong serial number."
- "I installed it but can't activate."

### Questions to Ask

- What app name appears in the title bar after installation?
- What does the activation key look like -- 5 groups of 5 characters (Waltr 2), or something else?

### Root Cause Candidates

- Agent or user downloaded WALTR PRO instead of Waltr 2.
- Waltr 2 and WALTR PRO are separate products with separate license keys.
- A Waltr 2 key will never activate WALTR PRO.

### Resolution

1. Confirm the user has a Waltr 2 license (5x5 key format).
2. Ask the user to uninstall the current app.
3. Send the correct Waltr 2 download link for their platform:
   - Mac: https://assets.softorino.com/static/download/earlier-versions/waltr2mac_2.6.27.dmg
   - Windows: https://assets.softorino.com/static/download/earlier-versions/waltr2windows_2.8.2.exe
4. Ask them to install and activate with their existing key.
5. Mention that Waltr 2 is a legacy app -- full functionality on newer macOS/Windows is not guaranteed.

### Escalate If

- Correct app installed but key still fails -- check license state in Shining.
- User wants the current supported version -- redirect to WALTR PRO.

### Internal Notes

- Waltr 2 is legacy. Be honest that it may not work perfectly on newer OS versions.
- Do not send the WALTR PRO link (waltrpromac_*.dmg) when the user has a Waltr 2 license.
- Always verify the app name in the user's screenshot before sending an activation key.

---

## Waltr 2 Legacy — Wi-Fi connection setting does not stay enabled

### Summary

**Product:** Waltr 2 Legacy
**Issue:** Wi-Fi connection setting does not stay enabled

### Symptoms

- Waltr 2 detects device via USB but Wi-Fi checkbox unchecks.
- Finder setting "Show this iPhone when on Wi-Fi" is enabled.
- User on modern macOS/iPhone.

### Common Customer Phrases

- "Enable Wi-Fi does not stay checked."
- "Cannot connect over Wi-Fi."

### Questions to Ask

- Does USB work?
- Does Finder show "Show this iPhone when on Wi-Fi"?
- macOS/iPhone versions?

### Root Cause Candidates

- Waltr 2 is legacy and may not fully support new macOS/iOS Wi-Fi sync behavior.

### Resolution

1. Confirm Waltr 2 is legacy.
2. Recommend WALTR PRO as newer supported app.
3. Explain Wi-Fi behavior may no longer be reliable in Waltr 2.

### Escalate If

- WALTR PRO also fails Wi-Fi connection.

### Internal Notes

- Be honest but gentle: "we cannot guarantee perfect Waltr 2 behavior on latest systems."

---

# Metadata, Album Art, and Apple Device Libraries

## WALTR PRO — Wrong album artwork appears after music transfer

### Summary

**Product:** WALTR PRO (also reproduced in Waltr 2)
**Issue:** Music transfers successfully but incorrect album artwork appears on device -- artwork belongs to a different artist already in the device library.

### Symptoms

- Music transfers without errors.
- Album artwork on device belongs to a completely different artist.
- The incorrect artwork is typically from an artist already present in the device library.
- Multiple retries of the same transfer may eventually produce the correct artwork (sometimes 10--20 attempts).
- Issue is intermittent but highly reproducible on large libraries.
- Source files have correct embedded artwork on Mac.
- Issue does not reproduce (or reproduces less) on clean devices with no existing library.

### Common Customer Phrases

- "Wrong cover art after transfer."
- "Artwork from another artist appears."
- "Covers are mixed up."
- "The artwork is correct on my Mac but wrong on iPhone."
- "I have to transfer the same album many times to get the right cover."

### Questions to Ask

- How many songs are already on the device?
- Does the wrong artwork belong to an artist already in the device library?
- Is the artwork correctly embedded in the source files (check on Mac)?
- What device model and iOS version?
- Does the issue happen on a device with a small or empty library?

### Root Cause Candidates

- iOS artwork cache conflict: when a large library exists on the device, iOS may reuse cached artwork from existing albums instead of reading the embedded artwork from the newly transferred file.
- Artwork mapping issue during WALTR PRO metadata processing.
- iOS MediaLibrary synchronization behavior with large libraries.
- Not a source file issue -- same files transfer correctly using other apps and eventually correct themselves after retries.

### Known Findings (from escalation)

- Source metadata and embedded artwork confirmed correct on Mac.
- Issue does not reproduce on clean/empty devices (confirmed via iPod Touch test).
- Strongly correlated with large existing libraries (12,000+ songs).
- Same issue reproduced in Waltr 2 -- not exclusive to WALTR PRO.
- Third-party transfer apps transfer the same files with correct artwork on first attempt.
- This is a known issue. No confirmed permanent fix available as of current status.

### Resolution

1. Verify artwork is correctly embedded in the source files on Mac before transfer.
2. Acknowledge the known issue -- do not suggest reinstalling WALTR PRO, reinstalling iTunes, or license troubleshooting. These have not been shown to resolve this.
3. Workaround: delete the album from device and re-transfer. Correct artwork may appear after multiple attempts.
4. Collect device model, iOS version, and WALTR PRO version for the report.
5. Escalate to development team if customer provides new reproducible patterns or additional data points.

### Escalate If

- Customer provides a new reproduction pattern not covered above.
- Issue reproduces on a clean device with no existing library.
- Customer reports the issue with a specific file type or metadata format consistently.

### Internal Notes

- This is a **known issue** -- be upfront with the customer that the team is aware of it.
- Do not promise an ETA or fix timeline unless confirmed by the dev team.
- Do not suggest reinstalling the app, drivers, or iTunes -- not relevant to this issue.
- Goodwill license extension may be appropriate for long-term affected paid customers -- flag to manager.

---

## WALTR PRO — Movie/TV metadata fetching unreliable

### Summary

**Product:** WALTR PRO
**Issue:** Movie/TV metadata fetching unreliable

### Symptoms

- Metadata fetching fails for many movies/TV shows.
- AI metadata feature often fails.
- Customer asks for TMDB/TVDB and multi-select.

### Common Customer Phrases

- "Please fix metadata fetching."
- "AI feature does not work."
- "Need multi-select for TV episodes."

### Questions to Ask

- Ask for examples only if dev team needs them.

### Root Cause Candidates

- Feature limitation / metadata provider reliability.

### Resolution

1. Thank customer for detailed feedback.
2. Pass request to development team.
3. Do not promise implementation.

### Escalate If

- High-value customer provides repeatable examples.

### Internal Notes

- Useful product feedback; agents should flag to Andrew/product.
