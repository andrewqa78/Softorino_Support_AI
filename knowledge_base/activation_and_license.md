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
