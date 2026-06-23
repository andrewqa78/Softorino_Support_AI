# iRingg

## iRingg — Quick Reference

### System Requirements
- **Windows:** Windows 10+, 1GHz processor, 2GB RAM, 100MB disk, .NET Framework
- Requires Apple Mobile Device Support drivers (auto-installed on install)
- Supports iPhone only via USB or Wi-Fi

### Trial Limitations
- 1 free ringtone download (no trial activation required)

### Feature Limitations & Restrictions
- Windows only (no macOS)
- iPhone only (no Android)
- Ringtones only -- cannot send files to Apple Music
- Final ringtone must be under 40 seconds
- YouTube/SoundCloud downloads for personal use only
- SndMoji™ library is fixed (no custom sound effects)

---

## iRingg for Windows — iPhone not detected / sync over USB or Wi-Fi fails

### Summary

**Product:** iRingg for Windows
**Issue:** iPhone not detected / sync over USB or Wi-Fi fails

### Symptoms

- iRingg does not sync with iPhone over cable or Wi-Fi.
- User may have already reinstalled iRingg and iTunes without success.
- iTunes may or may not detect the device.
- `C:\ProgramData\Softorino\iRingg\` folder may not exist if iRingg never successfully connected.

### Common Customer Phrases

- "iRingg does not synchronize."
- "The program does not see my iPhone."
- "Wi-Fi does not work."
- "I reinstalled everything and nothing changed."

### Questions to Ask

- Does iTunes detect the iPhone by cable?
- Does WALTR PRO or SYC PRO detect the same iPhone?
- Does Windows Explorer show it under This PC?
- iOS version, iPhone model, Windows version?
- Which iTunes version is installed -- and was it from Apple's website or the Microsoft Store?

### Root Cause Candidates

- Apple drivers missing or corrupted (AppleMobileDeviceSupport, Bonjour).
- Microsoft Store iTunes installed instead of standalone Apple iTunes.
- iRingg-specific detection issue independent of iTunes.
- Compatibility gap: very new iOS or iPhone model not yet supported by iRingg.

### Resolution

Standard path:
1. Confirm iTunes source -- must be standalone from Apple, NOT Microsoft Store.
2. Reinstall standalone iTunes: https://secure-appldnld.apple.com/itunes12/047-76416-20260302-fefe4356-211d-4da1-8bc4-058eb36ea803/iTunes64Setup.exe
3. Open iTunes and confirm the iPhone is detected there first.
4. Delete iRingg local files (except license.dat) from `C:\ProgramData\Softorino\iRingg\` -- note this folder is hidden; enable View > Hidden items.
5. Relaunch iRingg and test.

If iTunes also does not detect the device after reinstall:
6. Check Apple Mobile Device Service: Win+R → services.msc → confirm Running and set to Automatic.
7. Try manual MSI driver install: extract the iTunes installer and run AppleApplicationSupport.msi → AppleMobileDeviceSupport.msi in order.
8. Try different USB port and cable.

If all steps exhausted and nothing works:
9. Escalate to dev team -- likely a compatibility issue with the specific iOS/iPhone version.

### Escalate If

- All steps completed, iTunes detects device but iRingg still does not.
- Very new iPhone model or iOS version -- iRingg may not yet support it.
- `AppleSoftwareUpdate.msi` or `Bonjour64.msi` missing from iTunes install package -- flag to dev team.

### Internal Notes

- **iTunes version awareness:** The latest iTunes for Windows is 12.13.x. Do NOT tell users that 12.13.x is "outdated" -- it is the current version. Verify the actual latest version before commenting on it.
- The standalone iTunes link in the Appendix installs a specific build. If that build is older than what the user has, do not insist they downgrade.
- Microsoft Store iTunes is always the first thing to check -- it lacks components that Bonjour and Apple drivers need.
- `C:\ProgramData\Softorino\iRingg\` may not exist if iRingg never established a successful connection -- this is not an error, just means there are no cached files to delete.
- If the user has tried: new cable, different USB ports, router restart, network reset on iPhone, Windows reinstall, and multiple iTunes reinstalls -- this is beyond standard troubleshooting. Escalate immediately and do not repeat the same steps.

---

## iRingg — For You tab is empty

### Summary

**Product:** iRingg
**Issue:** For You tab is empty

### Symptoms

- iRingg opens.
- iPhone/device may be detected.
- For You tab shows no tracks.
- User thinks library did not sync.

### Common Customer Phrases

- "For You music library is empty."
- "iRingg does not load my iTunes library."

### Questions to Ask

- Can user use Search Online?
- Does iTunes show local music library?
- Are songs local files or Apple Music subscription?
- Does iRingg show any other tabs correctly?

### Root Cause Candidates

- For You recommendations did not populate.
- Local music data not loaded/analyzed yet.
- Protected/streaming music not available.
- Empty local library.

### Resolution

1. Explain empty For You is not necessarily a blocker.
2. Guide user to Search Online tab.
3. Tell them to search artist/song name, then create ringtone from YouTube/SoundCloud result.
4. Ask whether local library should contain downloadable, DRM-free tracks.

### Escalate If

- Search Online also fails.
- Local DRM-free library exists in iTunes but iRingg never sees it.

### Internal Notes

- For You is recommendation/library area, not the only way to create ringtones.

---

## iRingg — Basic usage: create ringtone from online search

### Summary

**Product:** iRingg
**Issue:** Basic usage: create ringtone from online search

### Symptoms

- User does not understand how to select tracks.
- For You tab empty.

### Common Customer Phrases

- "How do I create a ringtone?"
- "Where are the songs?"

### Questions to Ask

- What song/artist does the user want?
- Does Search Online show results?

### Root Cause Candidates

- Usage confusion.

### Resolution

1. Open Search Online.
2. Search artist/song such as Eminem, Drake, Kanye West.
3. Select result from YouTube/SoundCloud.
4. Choose ringtone fragment from beginning/middle/end.
5. Edit duration and send to iPhone.

### Escalate If

- Search results do not load for any query.
- Sending ringtone to device fails after creation.
