# PicFindr

## PicFindr — Quick Reference

### System Requirements
- **macOS:** 11.0 (Big Sur) or later, 2GB RAM, 100MB disk
- Requires internet connection for image search

### Trial Limitations
- 24-hour unlimited trial

### Feature Limitations & Restrictions
- macOS only (no Windows or mobile)
- Two image sources only: Pexels & Pixabay
- Images downloaded as-is (no built-in editor)
- No advanced filtering (keywords only -- no resolution or orientation filters)
- Collections stored locally (no cloud sync)

---

## PicFindr — Crashes on Apple Silicon / new macOS

### Summary

**Product:** PicFindr
**Issue:** Crashes on Apple Silicon / new macOS

### Symptoms

- PicFindr crashes immediately after launch or after typing search query.
- Customer sends crash log.
- Mac M1/M2 and newer macOS/Tahoe common.

### Common Customer Phrases

- "PicFindr crashes within seconds."
- "Search causes crash."
- "The app is unusable."

### Questions to Ask

- Mac chip and macOS version?
- PicFindr version?
- Crash report attached?

### Root Cause Candidates

- Known compatibility issue with newer macOS and Apple Silicon.

### Resolution

1. Acknowledge known issue.
2. Thank customer for crash log.
3. Forward report to development team.
4. No ETA unless confirmed.
5. Consider license extension for paid Universal License users if strongly affected.

### Escalate If

- Crash occurs on older Intel/macOS not matching known pattern.
- New crash signature appears.

### Internal Notes

- If compensation approved, 1--2 month Universal License extension is appropriate.

---

# Folder Colorizer

## Folder Colorizer for Mac — Quick Reference

### System Requirements
- **macOS:** Big Sur or later, 2GB RAM, 50MB disk
- Requires Full Disk Access permissions

### Trial Limitations
- 24-hour unlimited trial

### Feature Limitations & Restrictions
- macOS only (no Windows)
- Folders only -- cannot colorize individual files
- Emoji & decal collections are fixed (no custom uploads)
- Color changes are Mac-to-Mac compatible only (other systems won't see custom colors)
- AI Magic styling depends on folder name

---

## Folder Colorizer 2 (Windows) — Quick Reference

### System Requirements
- **Windows:** 7, 8, 10, or 11, 1GHz processor, 2GB RAM, 50MB disk
- Requires Administrator privileges

### Trial Limitations
- 2 folders free (no trial activation needed)

### Feature Limitations & Restrictions
- Windows only (no macOS)
- Folders only -- cannot color individual files
- Colors may reset after major Windows updates
- No folder grouping or organizing features

---

## Folder Colorizer for Mac — Possible OneDrive conflict / OneDrive closes

### Summary

**Product:** Folder Colorizer for Mac
**Issue:** Possible OneDrive conflict / OneDrive closes

### Symptoms

- User reports OneDrive closes after using Folder Colorizer.
- No crash window or report.
- Folder Colorizer version provided.

### Common Customer Phrases

- "OneDrive crashes after Folder Colorizer."
- "Is this known compatibility conflict?"

### Questions to Ask

- Folder Colorizer version?
- macOS version?
- Any crash log in Console?
- Does OneDrive crash only after colorizing folders?

### Root Cause Candidates

- Potential conflict with file metadata/icons in synced folders.
- OneDrive sync engine issue.
- Folder Colorizer local components corrupted.

### Resolution

1. Ask for crash log if available.
2. Suggest full uninstall via CleanAppsNow.
3. Reinstall Folder Colorizer.
4. Avoid modifying active OneDrive synced folders during test.

### Escalate If

- Reproducible crash only when colorizing OneDrive folders.
- Multiple OneDrive users report same behavior.

### Internal Notes

- CleanAppsNow is part of Universal License and can remove app components.

---

# Beamer

## Beamer 4 — Quick Reference

### System Requirements
- **macOS:** 10.15 (Catalina) or later, Intel Core i5+, 2GB RAM, 100MB disk
- Mac and Apple TV/Chromecast must be on the same Wi-Fi network

### Trial Limitations
- 15 minutes per video (no trial activation needed)

### Feature Limitations & Restrictions
- macOS only (no Windows)
- Apple TV (tvOS 16+) or Chromecast only -- no DLNA or Roku
- Wi-Fi required (no Ethernet-only devices)
- Streaming only -- does not save files to TV or Chromecast
- No playback controls on TV (control from Mac only)
- No manual conversion or export

---

## Beamer — MKV file fails to stream to Apple TV / AirPlay issue

### Summary

**Product:** Beamer 4
**Issue:** MKV file fails to stream wirelessly to Apple TV 4K

### Symptoms

- Streaming works with MP4 but fails or is unreliable with .mkv files.
- User has Apple TV 4K (A2843 or similar).
- Older Beamer version did not support Apple TV 4K; user upgraded to Beamer 4.
- Issue may appear intermittent -- sometimes resolves after trying MP4 first.

### Common Customer Phrases

- "MKV files won't stream to Apple TV."
- "It worked once but stopped again."
- "MP4 works but MKV does not."
- "I had no issues with older Apple TV generations."

### Questions to Ask

Ask these in the first reply before troubleshooting:

- Where is it streaming? Apple TV (model/year), TV with AirPlay 2 (brand/model), or Chromecast (model/year)?
- What is the file format? (mp4, mkv, avi, etc.)
- What resolution? 4K, 1080p, or 720p?
- What Mac are you streaming from? (M1, M2, Intel i5/i7, etc.)
- Where is the file stored? Internal SSD, HDD, or external drive?

### Root Cause Candidates

- Beamer cannot reliably transcode all MKV variants for Apple TV in real time.
- Apple TV 4K requires Apple-compatible codec. MKV is a container and may carry codecs that AirPlay rejects.
- Intermittent success may be related to prior MP4 playback warming up the pipeline.

### Resolution

1. Confirm MP4 works on the same Apple TV -- if yes, the issue is MKV codec compatibility, not the connection.
2. Recommend converting the MKV file to an Apple-compatible format using **WALTR PRO** (included in Universal License):
   - Install and activate WALTR PRO.
   - Open WALTR PRO -- find the **Local Folder** tile in the left panel of the app interface.
   - Drop the MKV file into that folder. WALTR PRO will convert it to an Apple-compatible format automatically.
   - Once converted, stream the new file through Beamer.
3. After conversion, streaming to Apple TV 4K should work without issues.

### Escalate If

- All file formats fail, not only MKV.
- MP4 also fails on the same Apple TV and network.
- WALTR PRO conversion fails or the converted file also does not stream.

### Internal Notes

- WALTR PRO conversion is the primary workaround for MKV codec incompatibility with Apple TV via Beamer.
- Do not promise a native MKV fix in Beamer without confirmed release info.
- If customer does not have Universal License, check whether WALTR PRO is available to them before recommending.

---

## Beamer — App crashes when connecting to Chromecast

### Summary

**Product:** Beamer
**Issue:** Beamer crashes immediately when the user tries to connect to a Google Chromecast (or Google TV). AirPlay to a different TV may work fine. App shuts down with an error/crash report.

### Symptoms

- Beamer crashes when attempting to connect to a Chromecast or Google TV device.
- Error/crash report dialog appears after the crash.
- AirPlay to another TV may work normally on the same Mac.
- Issue is not resolved by reactivating the Universal License.
- User may send a photo of the Crash Reporter window -- this is not sufficient for diagnosis.

### Common Customer Phrases

- "The app shuts down and gives an error message."
- "It won't connect to my Chromecast."
- "AirPlay works but Chromecast doesn't."
- "It crashes every time I try to cast."

### Questions to Ask

1. Does it crash with every video file, or only specific ones?
2. What file format are you trying to stream? (.mp4, .mkv, .avi, .mov, etc.)
3. Does Beamer crash every time you try to connect to Chromecast, or only with certain videos?
4. Can you stream the same file successfully using AirPlay?
5. What Chromecast model / Google TV device are you using?
6. What macOS version and Mac model?

### Root Cause Candidates

- Codec/container incompatibility between the video file and Chromecast's transcoding pipeline in Beamer.
- Chromecast-specific crash in Beamer's streaming module (not triggered by AirPlay path).
- Known crash pattern requiring crash log to diagnose -- photo of Crash Reporter is insufficient.

### Resolution

1. **Do not suggest reactivation** -- this is a crash/streaming issue, not an activation problem.
2. Ask the user for the full crash log from Console.app (not a photo of the crash dialog):
   - Press Command + Space → type **Console** → open Console app.
   - In the left sidebar, select **Crash Reports**.
   - Find the most recent Beamer crash report.
   - Export the file or copy its contents and send to support.
3. Ask all Questions to Ask (file format, whether it happens with all files, Chromecast model, AirPlay comparison).
4. If the crash is file-format-specific and AirPlay works with the same file: the issue is likely Beamer's Chromecast transcoding pipeline. Escalate with the crash log.
5. If all formats crash on Chromecast: escalate to dev team with crash log + device details.

### Escalate If

- Full crash log provided and crash is reproducible with any file on Chromecast.
- Multiple users report the same crash on the same Chromecast model/generation.
- Crash also occurs with AirPlay -- different root cause, escalate separately.

### Internal Notes

- Do NOT suggest reactivation as a first step for Beamer crashes -- activation is unrelated to streaming failures.
- A photo of the Crash Reporter is not useful. Always ask for the full Console.app crash log.
- AirPlay working while Chromecast crashes = issue is in Beamer's Chromecast code path, not the file itself.
- Sky Glass / Sky TV uses AirPlay 2 internally -- if the user says "Sky TV works but Chromecast doesn't", that confirms the split between AirPlay and Chromecast paths.

---

## Beamer — Chromecast playback stops / default media player message

### Summary

**Product:** Beamer
**Issue:** Chromecast playback stops / default media player message

### Symptoms

- Beamer starts connection but playback stops.
- Message similar to "Default Media Player playing".

### Common Customer Phrases

- "Beamer stops playing on Chromecast."
- "It shows default media player."

### Questions to Ask

- File format?
- Chromecast model?
- Does another file work?
- Same network?
- VPN/firewall?

### Root Cause Candidates

- Unsupported media codec/container.
- Chromecast incompatibility with specific file.
- Network issue.

### Resolution

1. Ask user to test another file.
2. Ask file format/codec.
3. Try MP4/H.264 if possible.
4. Restart Chromecast/router/Mac.

### Escalate If

- All files fail.
- Same file works in previous Beamer build.

---

# CleanAppsNow

## CleanAppsNow — Quick Reference

### System Requirements
- **macOS:** 10.14 (Mojave) or later, 2GB RAM, 100MB disk
- Requires Full Disk Access permissions

### Trial Limitations
- Included in the Universal License (no separate trial)

### Feature Limitations & Restrictions
- macOS only (no Windows)
- Drag-and-drop only (no file browser)
- Cannot remove system files or macOS extensions
- Cannot uninstall pre-installed macOS system apps
- Requires Full Disk Access to detect all app components

---

# Volume Concierge 2

## Volume Concierge 2 — Quick Reference

### System Requirements
- **Windows only**

### Trial Limitations
- No trial available

### Feature Limitations & Restrictions
- Windows only (no macOS)
- Up to 15 volume rules maximum
- System volume only (no per-app volume control)
- Time/day scheduling only (no app-based triggers)
- Runs in system tray (no visible UI window)
- Manual setup required (no auto-detection)

---

# Memory Optimizer 2

## Memory Optimizer 2 — Quick Reference

### System Requirements
- **Windows only**

### Trial Limitations
- No trial available

### Feature Limitations & Restrictions
- Windows only (no macOS)
- RAM only (no CPU, GPU, or storage optimization)
- Manual cleanup (no auto-cleaning)
- Does not identify specific memory-hogging apps
- Effectiveness varies depending on app memory usage

---

# Task ForceQuit Pro 2

## Task ForceQuit Pro 2 — Quick Reference

### System Requirements
- **Windows only**

### Trial Limitations
- No trial available

### Feature Limitations & Restrictions
- Windows only (no macOS)
- Shows active user-level apps only (no system services)
- No CPU/RAM stats per app
- No confirmation dialog before closing apps (easy to close by mistake)
- No keyboard shortcuts or automation
- English interface only
