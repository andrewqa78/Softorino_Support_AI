# AltTunes

## AltTunes — Quick Reference

### System Requirements
- **Windows:** Windows 10/11 (32-bit & 64-bit), 1GHz processor, 2GB RAM, 100MB disk
- Requires Apple Mobile Device Support drivers (auto-installed on install)
- Supports iPhone only (NOT iPad) -- requires iOS 18

### Trial Limitations
- 24-hour full access trial

### Feature Limitations & Restrictions
- Windows only (no Mac version)
- iPhone only (no iPad support)
- USB cable required (no wireless)
- iOS only (no Android)
- No music conversion -- transfers existing files only
- HEIC to JPG conversion is automatic (no format selection)
- Backups stored locally (no cloud sync)

---

## AltTunes for Windows — iPhone detected by Windows but not by AltTunes / iOS version conflict

### Summary

**Product:** AltTunes for Windows
**Issue:** iPhone detected by Windows but not by AltTunes after iOS update

### Symptoms

- iPhone is visible in Windows (File Explorer / This PC).
- AltTunes does not detect the connected device.
- Issue often appears after an iOS update on the same device.
- App worked previously with the same iPhone.

### Common Customer Phrases

- "My computer sees the iPhone but AltTunes does not."
- "AltTunes stopped detecting my iPhone."
- "It worked before but now the app does not see my phone."

### Questions to Ask

- Was iOS recently updated on this iPhone?
- Does Windows File Explorer show the device under This PC?
- Does iTunes detect the iPhone?

### Root Cause Candidates

- AltTunes caches device fingerprint and iOS version on first connection.
- After an iOS update the cached data no longer matches the connected device, causing a detection conflict.
- Deleting the cached files resets the device state and resolves the mismatch.

### Resolution

1. Close AltTunes.
2. Open File Explorer and navigate to C:\ProgramData\Softorino\AltTunes\.
   Note: ProgramData is a hidden folder. To make it visible, click View in the menu bar and enable Hidden items.
3. Delete the files named Settings and Device from that folder.
4. Reconnect the iPhone and open AltTunes.

### Escalate If

- Files deleted but iPhone is still not detected by AltTunes.
- iTunes also does not detect the device — treat as Apple driver issue, follow standard standalone iTunes repair path.

### Internal Notes

- This is a known minor bug. Do not frame it as a major issue when communicating with users.
- Do not confuse with activation/license problems.
- If iTunes also fails, the issue is at the Apple driver level, not AltTunes settings.

---

## AltTunes / WALTR PRO for Windows — Device visible in Windows but not in iTunes (advanced driver repair)

### Summary

**Product:** AltTunes / WALTR PRO for Windows
**Issue:** iPhone or iPad is detected by Windows (File Explorer, Device Manager) but does not appear in iTunes at all. Standard iTunes reinstall did not help.

### Symptoms

- Device shows up under Portable Devices in Device Manager or in File Explorer.
- iTunes does not detect the device -- not even briefly.
- AltTunes or WALTR PRO cannot detect the device either.
- Standard steps (uninstall MS Store iTunes → install standalone iTunes) already tried without success.
- Device may partially appear in some app but clicking does nothing ("only half of the device appears").

### Two-Scenario Diagnostic -- Always Clarify This First

Before troubleshooting, confirm which scenario applies:

**Scenario 1:** iPhone appears in iTunes but NOT in AltTunes/WALTR PRO → issue is app-specific, use app-level workaround (delete settings/device cache files).

**Scenario 2:** iPhone does NOT appear in iTunes at all → issue is at the Apple driver level on Windows. AltTunes and WALTR PRO cannot detect the device until iTunes does. Follow the advanced repair steps below.

### Common Customer Phrases

- "My iPhone is connected but your app doesn't see it."
- "Windows sees the iPhone but iTunes doesn't."
- "I tried reinstalling iTunes four times and nothing works."
- "Only half of the iPhone appears and clicking does nothing."

### Questions to Ask

- Does the iPhone appear in iTunes? (Scenario 1 vs Scenario 2 -- critical)
- Is the issue with one Apple device only, or all devices tried?
- What iPhone/iPad model and iOS version?
- What Windows version?
- Is any antivirus or endpoint security software installed?

### Root Cause Candidates

- Apple driver components (AppleMobileDeviceSupport, AppleApplicationSupport) not installed correctly.
- Security software or firewall blocking Apple driver installation or communication.
- Corrupted driver state left by Microsoft Store iTunes even after uninstall.
- Device pairing trust not completed properly.

### Resolution

Standard steps first (if not already done):
1. Uninstall Microsoft Store iTunes if present.
2. Restart PC.
3. Install standalone iTunes from Apple: https://secure-appldnld.apple.com/itunes12/047-76416-20260302-fefe4356-211d-4da1-8bc4-058eb36ea803/iTunes64Setup.exe
4. Open iTunes, connect device, tap Trust This Computer on iPhone/iPad.

If standard reinstall still does not work -- advanced repair:

5. Check Apple Mobile Device Service: Win + R → services.msc → find "Apple Mobile Device Service" → confirm Running and set to Automatic → right-click → Restart.
6. Try a different USB port (direct port on the PC, not a hub or front panel) and a different Apple-certified cable.
7. Temporarily disable antivirus or security software and test again -- some tools block Apple drivers on Windows 11.
8. Manual MSI driver install:
   - Download the iTunes standalone installer from Apple but do not run it directly.
   - Right-click the installer file → Extract (or use 7-Zip).
   - Run the extracted installers manually in this exact order:
     1. AppleApplicationSupport.msi
     2. AppleMobileDeviceSupport.msi
     3. AppleSoftwareUpdate.msi
   - Restart PC, reconnect device, test iTunes.
9. Check Device Manager with device connected -- look for any Apple entry with a warning icon under Universal Serial Bus devices or Portable Devices.

If device still does not appear in iTunes after all steps:
10. Ask for a screen recording showing the connection attempt -- "half device appearing" or other partial behavior needs to be seen to diagnose correctly.
11. If all steps exhausted and iTunes still fails: the issue is outside what any third-party app can resolve. The Apple Windows drivers are not functioning correctly on that system. User may need to contact Apple Support or try the device on another PC.

### Escalate If

- All steps above completed and iTunes still does not detect the device.
- Security software is confirmed as the blocker but user cannot disable it (corporate machine).
- Screen recording shows unexpected behavior not covered above.

### Internal Notes

- Always use the two-scenario framework to set correct expectations early. If iTunes cannot detect the device, be clear with the customer that this is not an AltTunes or WALTR PRO limitation.
- Manual MSI extraction is the strongest available fix short of a full Windows reinstall.
- "Half of iPhone appears / clicking does nothing" = incomplete driver install or broken pairing -- request screen recording to confirm before next step.
- Do not keep sending the same iTunes reinstall instructions if the customer has already tried it multiple times. Move to advanced steps.

---

## AltTunes for Windows — Photos stuck on Retrieving Data

### Summary

**Product:** AltTunes for Windows
**Issue:** Photos stuck on Retrieving Data

### Symptoms

- AltTunes stuck on rainbow phone/spinner.
- Photos do not load for hours.
- Backup may work but Photos section does not.

### Common Customer Phrases

- "Retrieving data forever."
- "I cannot transfer photos."
- "The wheel keeps spinning."

### Questions to Ask

- Windows version?
- iPhone model/iOS?
- How many photos/videos?
- Is iTunes installed from Apple standalone?
- Does Windows Explorer show photos?

### Root Cause Candidates

- Internal app state stuck.
- Huge photo library.
- Apple device interface slow/unresponsive.
- Apple drivers/iTunes issue.

### Resolution

1. Install latest AltTunes.
2. Delete C:\ProgramData\Softorino\AltTunes\settings.dat.
3. Reconnect unlocked iPhone and trust computer.
4. Close iTunes/iCloud/phone management apps.
5. Use direct USB port/cable.
6. If still stuck, escalate to @AndrewQA.

### Escalate If

- Photos section stuck after settings reset and Apple driver check.
- User has very large library and app never enumerates items.

### Internal Notes

- For 50GB/10k photos, items should start appearing within minutes, not hours.
- If the customer's iPhone is running a beta iOS version, check the dedicated entry below ("AltTunes for Windows — iOS beta compatibility issues") before assuming a generic stuck-state cause.

---

## AltTunes for Windows — iOS beta compatibility issues (stuck "Retrieving data...", encrypted backup toggle freezes)

### Summary

**Product:** AltTunes for Windows
**Issue:** Customer's iPhone running an iOS beta version (confirmed: iOS 27 beta) causes AltTunes to get stuck on "Retrieving data..." indefinitely, fails to load photos, and freezes when toggling the encrypted backup setting. A second device on a stable iOS version, on the same PC and AltTunes install, worked normally within seconds.

### Symptoms

- AltTunes shows "Retrieving data..." indefinitely (multiple hours) for a device running an iOS beta.
- Same PC, same AltTunes install -- a different device on a stable iOS version loads normally and quickly.
- Toggling "encrypted backups" off while the beta-iOS device is connected can freeze the app.
- Standard driver/iTunes/settings-file troubleshooting does not resolve it.
- Library size alone doesn't explain the delay -- in the confirmed case, the device with MORE photos (stable iOS, ~13,000) loaded within seconds, while the device with FEWER photos (beta iOS, ~8,000) never loaded.

### Common Customer Phrases

- "Stuck on Retrieving data for hours."
- "My wife's phone loaded in seconds, mine never did."
- "Turning off encrypted backups froze the app."
- "I'm on the iOS beta."

### Questions to Ask

- Is the affected iPhone running a beta iOS version? Which one?
- Does a different device on a stable iOS version work normally on the same PC/AltTunes install?
- Has standard driver/settings-file troubleshooting already been completed? (see "AltTunes for Windows — Photos stuck on Retrieving Data" above)

### Root Cause Candidates

- Known compatibility issue between AltTunes and iOS beta builds (confirmed with iOS 27 beta). Apple changes device communication behavior throughout the beta cycle, which can break AltTunes' data retrieval and backup-toggle functions.
- Not related to license, installation, Windows setup, or library size -- a stable-iOS device on the same setup works normally.

### Resolution

1. Complete standard troubleshooting first (see "AltTunes for Windows — Photos stuck on Retrieving Data") to rule out the generic stuck-state cause.
2. If the device is confirmed on a beta iOS version, and a stable-iOS device works fine on the same PC: explain this is a known iOS-beta compatibility limitation, not a license, installation, or Windows issue.
3. Do not promise an ETA -- compatibility work is planned closer to the official iOS release, but Apple keeps changing beta behavior, so nothing can be guaranteed mid-beta.
4. If the customer needs to back up the affected device now: suggest waiting for the public iOS release, or temporarily using a different computer/device if available.
5. For re-running an export to recover files missed in an earlier interrupted export: AltTunes does not skip duplicates automatically -- exporting to the same folder can create duplicate files. Recommend exporting to a new, empty folder and comparing/merging results manually afterward.

### Escalate If

- Customer is on a stable (non-beta) iOS release and still reproduces this exact pattern.
- Multiple customers report the same issue on the same beta iOS version -- log for dev team pattern tracking.

### Internal Notes

- Confirmed by @AndrewQA: known compatibility issue with iOS 27 beta specifically. No guaranteed compatibility with any iOS beta -- Apple changes beta behavior throughout the cycle.
- Reference ticket: Dillon, AltTunes for Windows, June 2026 -- confirmed via side-by-side test on the same PC (beta-iOS device stuck for hours; stable-iOS device with a larger library loaded in seconds).
- AltTunes does not deduplicate exports -- re-running an export to the same folder can create duplicates depending on Windows file-naming behavior. Always recommend a new empty folder for re-exports.
- Cross-reference: "AltTunes for Windows — Photos stuck on Retrieving Data" above for the generic (non-beta) stuck-state troubleshooting path.

---

## AltTunes — Photo export size smaller than iPhone storage size

### Summary

**Product:** AltTunes
**Issue:** Photo export size smaller than iPhone storage size

### Symptoms

- User exports photos/videos but GB total is much smaller than Photos storage.
- iCloud Photos may or may not be enabled.
- User transfers in batches.

### Common Customer Phrases

- "Only 196GB exported out of 340GB."
- "Not all photos/videos show up."
- "I did not miss or overlap batches."

### Questions to Ask

- Is iCloud Photos enabled?
- Is Optimize iPhone Storage enabled?
- Exact item count in Photos app?
- Exact exported file count?
- Hidden/Recently Deleted counts?
- Missing dates/years/months?

### Root Cause Candidates

- Originals stored in iCloud while thumbnails local.
- Hidden album excluded for privacy.
- Recently Deleted excluded.
- Apple storage includes cache/thumbnails/system data.
- User skipped date range during manual batches.
- Apple media database not exposing full library to app.

### Resolution

1. Compare item counts, not only GB size.
2. Ask user to check Photos app total item count.
3. Ask exported file count on drive.
4. Check Hidden and Recently Deleted.
5. Look for missing date/month/year pattern.
6. Determine whether files did not appear in AltTunes or appeared but failed export.

### Escalate If

- Item count difference is huge after all checks.
- Specific date range never appears in app.

### Internal Notes

- Key distinction: not displayed in app vs displayed but failed during export.

---

## AltTunes — Retrieve Music crashes / DRM confusion

### Summary

**Product:** AltTunes
**Issue:** Retrieve Music crashes / DRM confusion

### Symptoms

- AltTunes crashes when opening Retrieve Music.
- Crash continues after user deleted all music from iPhone.
- User asks whether DRM causes crash.

### Common Customer Phrases

- "Is DRM the reason nothing is retrieved?"
- "AltTunes closes when I retrieve music."
- "FoneTrans works."

### Questions to Ask

- Does crash happen only in Music section?
- Photos/Videos open normally?
- AltTunes version?
- Crash logs/screen recording?
- Windows version/iPhone/iOS?

### Root Cause Candidates

- DRM prevents extraction of protected tracks but should not crash app.
- Music library database handling bug.
- Local settings corruption.
- Apple driver/iTunes component issue.

### Resolution

1. Clarify DRM limitation but not expected crash cause.
2. Ask user to delete C:\ProgramData\Softorino\AltTunes\settings.dat.
3. Install/update standalone iTunes to refresh Apple components.
4. Open iTunes and confirm device detection.
5. Retry Music section.

### Escalate If

- Crash persists after settings reset and standalone iTunes install.
- Other sections work but Music always crashes.

### Internal Notes

- Do not keep repeating "DRM" after user removed all music.

---

## AltTunes — No automatic delete after successful photo transfer

### Summary

**Product:** AltTunes
**Issue:** No automatic delete after successful photo transfer

### Symptoms

- Customer wants to transfer photos in batches and auto-delete transferred files.

### Common Customer Phrases

- "Can AltTunes delete only transferred photos from iPhone?"
- "Can it automatically remove successful exports?"

### Questions to Ask

- What is customer trying to accomplish: free space or verify backup?

### Root Cause Candidates

- Feature not currently available.

### Resolution

1. Explain AltTunes does not currently support automatic delete-after-transfer.
2. Suggest deleting manually in Photos app only after verifying exported files.
3. Remind to clear Recently Deleted to free space.

### Escalate If

- Customer sees a delete option that behaves unexpectedly.

### Internal Notes

- Avoid encouraging deletion before backup verification.
