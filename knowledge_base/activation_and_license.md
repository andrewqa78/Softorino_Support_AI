# Activation and Universal License

## Free Trial Limitations by App

| App | Trial |
|---|---|
| WALTR PRO (Mac & Windows) | Books/PDFs: 10 · Movies: 1 · TV Shows: 3 · Music: 10 · Ringtones: 2 · Alt. Apps: Unlimited |
| SYC PRO (macOS) | 3 video files |
| SYC PRO (Windows) | 24-hour unlimited |
| AltTunes | 24-hour full access |
| iRingg | 1 free ringtone download |
| Beamer | 15 minutes per video (no activation needed) |
| Folder Colorizer for Mac | 24-hour unlimited |
| Folder Colorizer 2 (Windows) | 2 folders free (no activation needed) |
| PicFindr | 24-hour unlimited |
| Memory Optimizer 2 | No trial available |
| Task ForceQuit Pro 2 | No trial available |
| Volume Concierge 2 | No trial available |

---

## Current App Versions (License Dashboard snapshot, 2026-07-01)

Use this to check whether a customer's reported version is current before telling them to "update to the latest version." Do not assume a version is outdated without checking this table first (same principle as the iTunes version rule below).

| App | Current Version | Last Release Date |
|---|---|---|
| AltTunes (Windows) | 1.1.5 | February 2026 |
| Beamer (Mac) | 4.2.0 | September 2025 |
| CleanAppsNow (Mac) | 1.0.4 | September 2025 |
| DeskMinder | 2.0.9 | January 2026 |
| Folder Colorizer (Mac) | 4.11.8 | September 2025 |
| Folder Colorizer 2 (Windows) | 4.1.6 | March 2026 |
| iRingg (Mac) | 4.0.16 | January 2022 |
| iRingg (Windows) | 4.3.11 | February 2026 |
| Memory Optimizer 2 (Windows) | 4.1.3 | October 2023 |
| PicFindr | 1.6.13 | September 2025 |
| Softorino Youtube Converter 2 (Mac) | 4.0.22 | February 2023 |
| Softorino Youtube Converter 2 (Windows) | 4.1.8 | July 2024 |
| Softorino Youtube Converter PRO (macOS -- Apple Silicon) | 10.2.0 | March 2026 |
| Softorino Youtube Converter PRO (macOS -- Intel) | 10.2.0 | March 2026 |
| Softorino Youtube Converter PRO (Windows) | 10.2.0 | March 2026 |
| Task ForceQuit Pro 2 (Windows) | 4.1.3 | October 2023 |
| Volume Concierge 2 (Windows) | 4.1.3 | October 2023 |
| WALTR PRO (Mac) | 4.0.122 | September 2025 |
| WALTR PRO (Windows) | 4.3.10 | February 2026 |

### Internal Notes on this table

- **WALTR PRO (Mac) is still on 4.0.122 as of this snapshot** -- this is the exact build with the known Monterey/Intel and Sonoma/Apple Silicon crash bugs documented in `waltr_pro.md`. Do not tell affected customers to "update to the latest version" as a fix -- they're already on it.
- **SYC PRO now ships separate native builds for macOS Apple Silicon and macOS Intel** (both 10.2.0) -- worth confirming whether the Apple Silicon build is a true native binary now, not Rosetta, before repeating the generic Rosetta explanation from `global_rules.md`.
- **iRingg (Mac) shows a download link and version here (4.0.16, Jan 2022)**, which conflicts with `Softorino_Products.md`'s note that "macOS version: suspended indefinitely -- not available for download." Flagged for Andrew to confirm which is accurate before relying on either in a customer reply.
- "Softorino Youtube Converter 2" (non-PRO, v4.x) is a separate legacy-style product line from "Softorino Youtube Converter PRO" (v10.x) -- don't confuse the two when checking a customer's version against this table.
- This table is a point-in-time snapshot from the License Dashboard "Your Applications" view -- re-check against the dashboard if it's been a while since 2026-07-01.

---

## Universal License — "Reset" vs "Activate" button in the dashboard

### Summary

**Issue:** Agent or user confused about which button to use for activation in the Universal License Dashboard.

### How the Dashboard Works

- **Before first activation:** The button next to an app shows **"Activate"** -- click this to activate the app for the first time.
- **After activation:** The button changes to **"Reset License"** -- this resets the local activation so the user can re-activate (useful when switching computers or fixing a stuck activation).

### Common Mistakes

- Telling a user to click "Reset" when they have never activated the app -- the button does not exist yet, so the user cannot find it.
- Telling a user to click "Activate" when activation is already recorded and they need to reset first.

### Resolution

1. If the user has **never activated** the app: guide them to click **"Activate"** next to the app in the dashboard.
2. If the app was previously activated and activation is stuck or failing: guide them to click **"Reset License"**, then click **"Activate"** again.
3. If the user cannot find either button: ask them to open the dashboard in a Private/Incognito window -- the page may be cached or the session may be expired.
4. If the dashboard shows no apps at all: they may be on the wrong OS tab (Windows vs macOS). Check first.

### Internal Notes

- The Reset button only appears after a successful first activation. Do not tell users to click Reset if they have never activated.

---

## Universal License — Dashboard frozen / clicking Activate or Download does nothing

### Summary

**Product:** Universal License Dashboard
**Issue:** Dashboard page appears but nothing happens when clicking Activate, Download, or any tab. Page appears frozen.

### Symptoms

- User logs into the dashboard and sees the app list.
- Clicking Activate or Download produces no response.
- Clicking OS tabs (Windows / macOS) does nothing.
- Page appears visually correct but is non-interactive.
- May also present as: app list missing entirely, or page redirects back to sign-in after clicking anything.

### Common Customer Phrases

- "Nothing happens when I click Activate."
- "The screen is frozen."
- "I can't click anything on the page."
- "It takes me back to the sign-in page."
- "The download button doesn't work."

### Questions to Ask

- Which browser and OS is the user on?
- Have they tried a Private / Incognito window?
- Are they on the correct OS tab in the dashboard (Windows vs macOS)?

### Root Cause Candidates

- **Wrong OS tab selected** -- user is on macOS but has the Windows tab active (or vice versa). Clicking Activate on the wrong OS tab does nothing.
- **Expired or corrupted browser session / cache** -- causes the page to freeze or redirect to sign-in on any click.
- **Browser extension or security setting** blocking dashboard interactions.

### Resolution

Step 1 -- Check the OS tab first:
1. Ask the user which device they are on (Mac or Windows).
2. Make sure they are on the matching tab in the dashboard (macOS tab for Mac users, Windows tab for Windows users).
3. If they were on the wrong tab -- switching is the fix. Ask them to click the correct OS tab and try Activate again.

Step 2 -- If correct tab but still frozen:
4. Ask them to open the dashboard in a Private / Incognito window:
   - Safari: File → New Private Window
   - Chrome: File → New Incognito Window
   - Edge: Ctrl + Shift + N
5. Send them their direct license link (from the system): https://softorino.com/submanager/a-[user-token]
6. In the private window, make sure the correct OS tab is selected, then click Activate or Download.

Step 3 -- If still not working:
7. Ask them to clear browser cache and cookies, then try again in a regular window.
8. Ask which browser they are using -- if Safari on old macOS, suggest trying Chrome or Firefox.

### Escalate If

- Private/Incognito window also frozen after clearing cache.
- User cannot install any other browser (old macOS, corporate restrictions).
- License is not showing in the system or the direct link also fails.

### Internal Notes

- Wrong OS tab is the most common cause and easiest fix -- always check this first before assuming a technical issue.
- The direct license link (submanager/a-[token]) bypasses the sign-in flow and loads the dashboard in an already-authenticated state -- useful when session issues prevent normal login.
- Redirect back to sign-in on click = expired session. Incognito + direct link almost always fixes this.
- Do not suggest Chrome if user is on a very old macOS (Big Sur or earlier) -- Chrome may not install. Suggest Safari Private Window first.

---

## Universal License / Any App — Activate button does nothing or returns to activation loop

### Summary

**Product:** Universal License / Any App
**Issue:** Activate button does nothing or returns to activation loop

### Symptoms

- User can open License Dashboard but app keeps asking for activation.
- Activate button briefly changes color then returns.
- App may show active in dashboard but local app still asks to activate.

### Common Customer Phrases

- "I already activated it."
- "The Activate button does nothing."
- "It keeps asking me to activate."
- "There is no Reset button."

### Questions to Ask

- Which app is affected?
- Does the backend show the activation attempt?
- Does another app activate under the same license?
- Windows or macOS?

### Root Cause Candidates

- Local license cache corrupted.
- Activation state not saved locally.
- Backend entitlement not updated.
- Browser/session issue in License Dashboard.

### Resolution

1. Confirm subscription is active in backend.
2. Ask user to close the app.
3. On Windows, delete local license files from C:\ProgramData\Softorino\AppName\.
4. Delete license.dat, license2.dat, license3.dat if present.
5. Open License Dashboard in an incognito/private browser window.
6. Click Activate for the affected app again.

### Escalate If

- Backend does not record activation attempts.
- Only one app fails while other apps activate.
- Multiple users report same activation behavior.

### Internal Notes

- Do not tell the customer internal backend flags were blocked unless needed. Say "we made an adjustment on our side."

---

## Universal License / Canceled Subscription — Customer canceled renewal but app still should work until expiry

### Summary

**Product:** Universal License / Canceled Subscription
**Issue:** Customer canceled renewal but app still should work until expiry

### Symptoms

- Customer requested cancellation.
- App asks to activate before subscription expiry.
- Customer worries cancellation killed access immediately.

### Common Customer Phrases

- "I canceled but I should still have access."
- "It asks me to activate again."
- "Will I be charged again?"

### Questions to Ask

- What is the expiration date?
- Is cancellation processed only for renewal or immediate access?
- Which app asks for activation?

### Root Cause Candidates

- Local activation cache expired/corrupted.
- Customer confuses cancellation with immediate deactivation.

### Resolution

1. Confirm cancellation prevents future renewal only.
2. Confirm license remains valid until expiration date.
3. Ask user to delete local license files and reactivate through License Dashboard.

### Escalate If

- License is inactive before paid period ends.
- Backend and dashboard disagree.

### Internal Notes

- Reassure: cancellation does not remove access before expiry.

---

## Universal License / Billing — Lifetime license shows renews every 3 years

### Summary

**Product:** Universal License / Billing
**Issue:** Lifetime license shows renews every 3 years

### Symptoms

- Customer sees old promo text saying lifetime renews every 3 years.
- Customer asks whether lifetime is one-time or recurring.

### Common Customer Phrases

- "How can lifetime renew every three years?"
- "Is it really lifetime?"
- "Will I be charged again?"

### Questions to Ask

- Ask for screenshot of offer/payment page.
- Check whether screenshot is from outdated promotion.

### Root Cause Candidates

- Outdated promotional text.
- Old FastSpring/order wording.
- Current offer differs from legacy promotion.

### Resolution

1. Explain current Lifetime Universal License is one-time purchase only.
2. Clarify no recurring charges after purchase.
3. If promo applies, mention current discount without overexplaining old campaign.

### Escalate If

- Payment page currently still shows incorrect wording.
- Customer already purchased and order metadata shows renewal.

### Internal Notes

- Be direct: "No, the current lifetime license does not renew every 3 years."

---

## Beamer — Activation error #2002

### Summary

**Product:** Beamer
**Issue:** Activation error #2002

### Symptoms

- Beamer fails activation.
- Other apps under Universal License work.
- Customer reinstalled app and reset license without success.

### Common Customer Phrases

- "Beamer is not activating."
- "I get error #2002."
- "DeskMinder works but Beamer does not."

### Questions to Ask

- Does the issue happen only with Beamer?
- What Beamer version?
- macOS/Windows and chip?

### Root Cause Candidates

- Backend entitlement/license flag blocked for Beamer.
- App-specific license mapping issue.

### Resolution

1. Check backend entitlement for Beamer.
2. Unblock/enable Beamer entitlement if needed.
3. Ask customer to try activation again.

### Escalate If

- Entitlement is enabled but error persists.
- Multiple apps show error #2002.

### Internal Notes

- Customer does not need to know internal entitlement was blocked. Say: "We made an adjustment on our side."

---

## Universal License / Any App — Error 509 during activation

### Summary

**Product:** Universal License / Any App
**Issue:** Error 509 during activation -- expired activation token

### Symptoms

- App activates on first attempt.
- User returns to License Dashboard without refreshing the page.
- User clicks Activate again for the same app.
- System returns Error 509.
- After refreshing the page, the Activate button is replaced by Reset License -- the app is already activated.

### Common Customer Phrases

- "I get error 509 when trying to activate."
- "Activation fails with error 509."
- "I clicked Activate and got an error but the app seems to be activated?"

### Questions to Ask

- Does the License Dashboard show Reset License or Activate next to the affected app?
- Did the app open or work before the error appeared?

### Root Cause Candidates

- User clicks Activate a second time on a stale, un-refreshed License Dashboard page.
- The activation token was already consumed on the first click.
- System returns 509 (wrong/expired token) on the second attempt.
- Known minor bug; fix is planned.

### Resolution

1. Ask user to refresh the License Dashboard page.
2. If the button now shows Reset License, the app is already activated -- ask them to open the app and confirm it works.
3. If the app still asks for activation: click Reset License, then click Activate again.
4. Launch the app and confirm activation is complete.

### Escalate If

- Reset License + Activate cycle does not resolve the error.
- Error 509 appears on the very first activation attempt with no prior click.

### Internal Notes

- Error 509 = wrong or expired activation token. Almost always caused by clicking Activate twice on a stale dashboard page.
- Known bug; fix is planned.
- Do not ask macOS users to delete license files manually -- this is not possible. Only SYC PRO for macOS has a built-in option for local license file removal.

---

## Universal License Dashboard — Expired subscriptions still showing as active

### Summary

**Product:** Universal License Dashboard
**Issue:** Dashboard displays cancelled or expired subscriptions alongside the active one, making it appear as if the customer has multiple active charges.

### Symptoms

- Dashboard shows 2 or more subscription entries.
- Customer believes they are being billed for multiple subscriptions.
- Old subscriptions show seemingly valid expiry dates even though they were cancelled.

### Common Customer Phrases

- "Why am I seeing 2 active subscriptions?"
- "Am I being charged for two accounts?"
- "Please cancel the second subscription."
- "I want a refund for the duplicate."

### Questions to Ask

- Can they share a screenshot of the dashboard?
- What email is the account under?

### Root Cause Candidates

- Known dashboard UI bug: expired and cancelled subscriptions are not consistently filtered out. They remain visible with misleading expiry dates.

### Resolution

1. Check the backend to confirm which subscriptions are actually active and being billed.
2. Tell the customer which one is active and when it expires.
3. Confirm that the other entries are NOT being billed -- they are display artefacts from past subscriptions.
4. Explain this is a known display issue the team is aware of.
5. If the customer insists a specific old subscription is still charging them: locate the charge in FastSpring before confirming or denying.

### Escalate If

- Backend confirms more than one subscription is genuinely active on the same account.
- Customer provides a PayPal or bank charge that matches a subscription that should be inactive.

### Internal Notes

- Do not tell the customer this is "expected behavior" -- acknowledge it as a known display issue.
- Never confirm to a customer they are not being charged without first verifying in the backend.

---

## Universal License — Magic link / login email not received

### Summary

**Product:** Universal License Dashboard
**Issue:** Customer enters their email at softorino.com/submanager but never receives the login email.

### Symptoms

- Customer cannot access their dashboard at all.
- No magic link email arrives after multiple attempts.
- May have been waiting minutes or hours.
- Contact form on the site may also appear non-functional.

### Common Customer Phrases

- "I never receive the login email."
- "No code or credentials arrive."
- "I can't access my account."
- "When I click contact us, nothing happens."

### Questions to Ask

- Which exact email did they enter?
- Have they checked their spam/junk folder?
- Do they have another email the purchase might be under?

### Root Cause Candidates

- Email entered doesn't match any account (typo or wrong address).
- Magic link landed in spam/junk.
- Email provider blocking automated mail.
- Customer is entering a different email than the one used to purchase.

### Resolution

1. Ask them to check spam/junk immediately -- magic links often land there.
2. Ask them to confirm the exact email address they entered.
3. If not in spam: ask whether they have another email a Softorino purchase could be under.
4. Try resending the magic link from the backend to their confirmed email.
5. If confirmed correct but still not arriving after multiple attempts: escalate to @AndrewQA -- possible mail delivery issue.

### Escalate If

- Email confirmed correct, spam checked, still not received after multiple attempts.
- Customer has no other email addresses to try.
- Multiple users report the same issue simultaneously (possible mail delivery outage).

### Internal Notes

- "Can't access my account" is almost always an email mismatch, not a backend failure. Start there.
- Do not assume the account doesn't exist -- the purchase email might simply differ from what they're entering.

---

## Universal License — Old license activates instead of newly purchased one

### Summary

**Product:** Universal License / Any App
**Issue:** Customer purchased a new license but the app keeps activating with an old, expired license from the same account.

### Symptoms

- App shows an expiry date from months or years ago, not the recent purchase.
- Dashboard shows multiple license entries for the same email.
- Customer followed activation steps correctly.
- New purchase confirmation email exists but the old license keeps being picked up.

### Common Customer Phrases

- "It shows a license from [old date], not my new one."
- "I just bought a license but it's activating the wrong one."
- "The app shows expired even though I purchased last month."
- "It keeps bringing up the old license."

### Questions to Ask

- What expiry date is the app currently showing?
- What email was used for the new purchase?
- Do they have a second email that might also have a license?
- Can they share a screenshot of the dashboard showing all license entries?

### Root Cause Candidates

- Two licenses exist on the same account; app or dashboard picks the older one.
- New license was purchased under a different email than the one being used for activation.
- Legacy license key (old XXXXX-XXXXX format) is cached locally and overrides Universal License activation.

### Resolution

1. Ask for a screenshot of the dashboard showing all licenses and expiry dates.
2. Confirm which entry is the new license based on the purchase date.
3. If both licenses are on the same email: try clicking Reset License on the old entry, then Activate on the new one.
4. If the new license is under a different email: guide the customer to use the correct email in the dashboard.
5. If the old license appears to be a legacy key (XXXXX-XXXXX format): direct them to https://softorino.com/earlier-versions and explain the difference between legacy keys and Universal License.
6. If none of the above works: escalate to @AndrewQA to manually deactivate the old license on the backend.

### Escalate If

- Both licenses are under the same email and reset + reactivate doesn't help.
- App consistently activates the wrong license even after the correct email is confirmed.
- Customer has been stuck on this for more than 2 exchanges.

### Internal Notes

- Do not ask the customer to "just try again" after they have already tried multiple times.
- When two licenses exist on the same account, a backend fix is almost always needed. Escalate early rather than repeating the same steps.
- If the customer mentions "Anniversary Edition" of SYC PRO: this refers to a specific promotional version. Verify with @AndrewQA what build is currently available and how to download it -- do not guess.

---

## Universal License — Refunded subscription still visible in dashboard but cannot activate

### Summary

**Product:** Universal License
**Issue:** A past refund automatically cancelled the subscription. The license is inactive. But the dashboard still displays it, making the customer believe they have valid access.

### Symptoms

- Customer sees a subscription entry in the dashboard with what looks like a valid expiry date.
- App fails to activate or shows "no active license."
- Customer is confused or angry because the dashboard clearly shows a license.
- Account history shows a past refund.

### Common Customer Phrases

- "I can see my license right here -- why can't I activate?"
- "The dashboard shows I have a license."
- "I've reset and activated many times and nothing works."
- "I've had this for years, it always worked."

### Root Cause

When a refund is processed, FastSpring automatically cancels the subscription. The license becomes inactive immediately. The dashboard continues to display the entry due to the known display bug -- it does not indicate that the subscription was cancelled due to a refund.

### Resolution

1. Check account history for any past refunds on this email before responding.
2. If a refund was processed: confirm the subscription was cancelled as part of that refund.
3. Explain to the customer:
   - The subscription shown in the dashboard was cancelled when the refund was processed.
   - The license is no longer active -- that is why activation fails.
   - The dashboard still displaying it is a known display issue.
4. To use the app again: they need to purchase a new license. Offer the link: https://softorino.com/universal-license

### Escalate If

- No refund found in account history but subscription still shows as unactivatable.

### Internal Notes

- Do NOT open with "you have no license." That reads as an accusation. Open with: "I checked your account and found the explanation." Then explain the refund → auto-cancel chain.
- Be empathetic -- customers who got a refund years ago often forget, and the dashboard entry genuinely looks like proof of access. Acknowledge the confusion before explaining.
- This is distinct from the "expired subscription" display bug -- here the subscription was explicitly cancelled by a refund action, not just expired by time.

---

## Universal License — One license = one device; managing multiple Macs

### Summary

**Product:** Universal License
**Issue:** Customer wants to use one license on multiple Macs simultaneously, or bought a second license by mistake thinking they needed one per device.

### Symptoms

- Customer asks if one license covers more than one computer.
- Customer accidentally bought a second subscription for a second Mac.
- Customer cannot identify which license or email is active on a specific machine from inside the app.

### Common Customer Phrases

- "Can I install it on more than one Mac?"
- "I bought a second license for my MacBook -- do I need to?"
- "How do I know which license is active on this computer?"
- "There's no way to see my email from inside the app."

### Root Cause Candidates

- Customer assumes multi-device coverage (like Microsoft 365).
- Customer bought a second license for a second Mac not realizing the license can be transferred.

### Resolution

**If customer asks about multi-device:**
1. Clarify: one Universal License = one active device at a time.
2. Options for a second Mac:
   - **Transfer:** Reset License on the old device → Activate on the new one. Use both sequentially.
   - **Second license:** Buy a second subscription to use both Macs simultaneously.

**If customer bought a duplicate by mistake:**
1. Check if the duplicate is within the 30-day refund window.
2. If yes and they only need one device: process refund on the duplicate.
3. If they want to keep both (one per Mac): confirm both are active and explain they work independently under different emails.

**If customer can't identify which email is active on a device:**
1. There is no way to see the active license email from inside the app -- this is a known UX gap.
2. Ask the customer to check each email they may have used at softorino.com/submanager.
3. Confirm which email has the subscription matching the activation period on that device.

### Escalate If

- Customer wants to merge two subscriptions under one email -- not currently possible. Escalate to @AndrewQA.

### Internal Notes

- Universal License is strictly 1 device at a time. Do not imply otherwise.
- The app does not display the associated email address anywhere in the UI. Only the dashboard shows this. Known UX gap -- customers notice and are frustrated by it.
- The "1 device" limitation is a common customer complaint vs. competitors. Acknowledge it genuinely rather than dismissing it.
