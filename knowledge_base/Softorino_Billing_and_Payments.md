# Softorino Billing and Payments Knowledge Base

---

# Global Billing Rules

- Always check the customer's account in FastSpring before confirming or denying a charge.
- If a charge does not appear under the customer's primary email, check alternative emails they provide.
- PayPal is a payment processor only -- FastSpring remains the merchant of record. A PayPal receipt does not mean the order bypassed FastSpring.
- Never confirm a refund is impossible without first locating the actual order in FastSpring.
- Never promise a refund without confirming the charge exists and falls within the 30-day refund window.
- If an order cannot be located in FastSpring, escalate to Andrew with the PayPal Transaction ID and any receipt attachments.
- Refund policy: 30 days from the charge date.

---

# Suspicious Emails / Possible Phishing

## Customer Reports Unexpected Renewal or Payment Email

### Summary

**Issue:** Customer receives an email about a failed renewal or payment that doesn't match their actual subscription schedule. They suspect phishing.

### Symptoms

- Customer reports an email claiming their license renewal failed or a payment was charged.
- The email does not match their known renewal date.
- Customer is unsure if the email came from Softorino.
- Customer has not clicked any links yet.

### Common Customer Phrases

- "I received an email saying my renewal failed but my subscription isn't due until..."
- "Is this a phishing attempt?"
- "I'm concerned this email didn't come from you."
- "Can I forward this to you to verify?"

### Resolution

1. Check the customer's subscription status in FastSpring before responding.
2. Confirm whether any renewal or payment activity exists on their account.
3. Reply with what you found -- if no renewal activity matches the email, say so clearly.
4. Ask the customer to forward the suspicious email or send a screenshot including the sender's email address.
5. Do not ask the customer to click any links in the suspicious email.
6. Check whether the customer may have a second subscription under a different email address -- the email may relate to that account.
7. Once you receive the forwarded email, check the sender domain -- legitimate Softorino emails come from @softorino.com or via FastSpring's domain. Any other domain is suspicious.

### Escalate If

- The email appears to be a genuine phishing attempt targeting Softorino customers -- flag to the team.
- The customer has already clicked a link or entered payment details in response to the suspicious email.

### Internal Notes

- Commend the customer for checking before taking any action -- this is the right behavior.
- Do not speculate about whether it's phishing before reviewing the email. Say "we'd like to verify it" rather than "it sounds like phishing."
- FastSpring sends renewal reminders before the renewal date, not failure notices unless a payment actually failed.

---

# Refunds

## Refund Request — Charge not visible in FastSpring but customer has PayPal receipt

### Summary

**Issue:** Customer claims a recent charge but it does not appear in FastSpring under their email.

### Symptoms

- Customer provides a PayPal receipt for a Softorino subscription renewal.
- FastSpring search by email returns no matching recent charge.
- Customer may have multiple email addresses or the original purchase was made under a different email.

### Common Customer Phrases

- "I was charged but I want a refund."
- "I didn't mean to renew."
- "I thought I cancelled this."
- "Can you please refund and cancel?"

### Questions to Ask

- What email was used to purchase the original license?
- Do they have any alternative email addresses linked to Softorino?
- Can they provide the PayPal Transaction ID from the receipt?
- Does the receipt mention FastSpring as the merchant?

### Root Cause Candidates

- Original subscription was created under a different email address.
- Renewal was processed by FastSpring via PayPal but indexed under the original purchase email.
- Order may exist in FastSpring but is not surfaced by the primary support email.

### Resolution

1. Search FastSpring by all email addresses the customer provides.
2. If still not found, ask customer for PayPal Transaction ID and a copy of the receipt.
3. Escalate to Andrew with Transaction ID and receipt -- FastSpring can locate orders by transaction reference.
4. Once located, confirm whether the charge falls within the 30-day refund window.
5. If eligible, process refund and cancel the subscription.
6. Inform customer the refund may take a few business days to appear depending on PayPal or their bank.

### Escalate If

- Charge cannot be located after checking all email addresses.
- Customer provides a Transaction ID -- always escalate to Andrew for FastSpring lookup.
- Receipt does not mention FastSpring as merchant (possible different reseller).

### Internal Notes

- If purchased via PayPal through FastSpring: FastSpring is always the merchant of record. The order exists in FastSpring even if the customer only has a PayPal receipt.
- If the order truly cannot be found in FastSpring, it may have been purchased through a different reseller or marketplace.
- When informing the customer, do not say "there is no charge on your account" before exhausting all email options and escalating -- this may be factually incorrect and creates distrust.

---

## Refund Request — Automatic renewal customer did not expect

### Summary

**Issue:** Customer did not realize their subscription would auto-renew and requests a refund.

### Symptoms

- Customer says they thought they had cancelled.
- Renewal charge appears unexpectedly.
- Customer may be in financial difficulty.

### Common Customer Phrases

- "I thought I cancelled this."
- "I didn't expect to be charged."
- "Can you refund and cancel?"

### Questions to Ask

- When was the charge made?
- What email is the account under?
- Does the charge appear in FastSpring?

### Resolution

1. Locate the charge in FastSpring.
2. Check whether it falls within the 30-day refund window.
3. If eligible -- process refund and cancel subscription.
4. If not eligible -- cancel future renewals only and explain the policy clearly.
5. Be empathetic but do not make exceptions to the 30-day policy without manager approval.

### Escalate If

- Customer is in genuine financial hardship and requests a goodwill exception -- flag to manager.
- Charge is outside 30 days but customer was clearly unaware of renewal.

### Internal Notes

- Cancelling auto-renewal does not refund a charge that already happened.
- Always cancel future renewals as a minimum action, even if refund is not possible.
- Be specific when communicating: tell the customer exactly when their access expires after cancellation.

---

## Billing — Subscription under a different email, charged to customer's PayPal (gifted subscription)

### Summary

**Issue:** Customer's PayPal is charged for a subscription that was originally registered under a different email address -- typically a gift subscription set up for a friend. The charge cannot be found in FastSpring under the customer's own email.

### Symptoms

- Customer provides a PayPal receipt showing a Softorino charge.
- FastSpring search by the customer's email returns no matching order.
- Charge is real and recurring.
- Customer may not initially remember the subscription was created under a different email.

### Common Customer Phrases

- "I can't find this charge on my account."
- "I thought I had cancelled but I keep getting charged."
- "I may have set up a subscription for a friend."
- "I don't have an email from you but PayPal shows the charge."

### Questions to Ask

- Do you have any other email addresses linked to a Softorino purchase?
- Did you ever purchase or set up a subscription for someone else?
- Can you provide the PayPal Transaction ID from the receipt?

### Root Cause

Subscription was created under a different email (e.g., gifted to another person). FastSpring indexed it under that email, not the payer's. Cancellation attempts on the wrong account have no effect -- the charge keeps hitting the payer's PayPal.

### Resolution

1. Search FastSpring by all email addresses the customer provides.
2. If still not found -- ask for the PayPal Transaction ID.
3. Escalate to @AndrewQA with the Transaction ID. FastSpring can locate any order by transaction reference regardless of email.
4. Once found, cancel the subscription and confirm whether any charges fall within the 30-day refund window.
5. Only the most recent charge within 30 days is eligible for refund. Be clear about this upfront.
6. If customer requests refunds on older charges (outside 30 days) -- escalate to manager for a goodwill decision. Do not promise anything.

### Escalate If

- Transaction ID provided but order still cannot be located -- may be a different reseller.
- Customer requests refunds on multiple charges spanning many months -- manager decision required.
- The subscription is under someone else's email and that person cannot be reached to authorize cancellation -- escalate to @AndrewQA, do not decide yourself.

### Internal Notes

- This case type takes longer than average because FastSpring lookup by Transaction ID requires direct contact with FastSpring support.
- Do not say "I cannot find this charge" more than once without escalating. Get the Transaction ID on the second exchange at the latest.
- Past case lesson: support spent multiple months asking for more screenshots instead of going to FastSpring early. The Transaction ID is the key -- get it fast.
- If the subscription was a gift and the original recipient has medical or personal circumstances preventing them from responding, @AndrewQA may authorize cancellation without their email confirmation. Escalate -- do not make this call yourself.

---

## Billing — FastSpring shows no payment but customer has PayPal/bank proof

### Summary

**Product:** Universal License / Billing
**Issue:** FastSpring reports no successful payment for the customer's email, but the customer has a PayPal receipt or bank statement showing the charge cleared.

### Symptoms

- Customer purchased a license and received a checkout summary or order confirmation.
- FastSpring search by email returns no completed order.
- Customer has PayPal or credit card proof showing funds were taken.

### Common Customer Phrases

- "I have proof the payment went through."
- "My credit card/PayPal shows the charge."
- "FastSpring says it didn't go through but I was charged."
- "Why are you saying I didn't pay when I have the receipt?"

### Root Cause Candidates

- Payment initiated but not fully settled -- FastSpring generates an order document before payment completes, which customer may mistake for a receipt. Pre-auth holds look like charges but are voided if payment fails.
- Payment completed but indexed under a different email in FastSpring.
- FastSpring processing delay -- payment settled but not yet reflected at time of first lookup.

### Resolution

1. Do NOT tell the customer "the payment didn't go through" after a single FastSpring check. Say: "We're investigating and will follow up."
2. Ask the customer for:
   - PayPal Transaction ID (if PayPal was used)
   - Screenshot of bank or credit card statement showing the charge as fully settled (not pending)
3. Re-escalate to FastSpring with this proof -- they can trace completed payments even without a matching email.
4. FastSpring will either confirm the payment and provide the order number, or confirm it was a pre-auth hold that was voided.
5. If payment confirmed: FastSpring activates the license. Guide the customer to the dashboard.
6. If payment voided: explain clearly that no funds were captured and the document they saw was generated before payment completed.

### Escalate If

- FastSpring confirms payment completed but license was not generated on our side.
- Customer insists payment went through but cannot provide a Transaction ID or settled bank statement.

### Internal Notes

- A pre-authorization hold is NOT a charge. FastSpring generates a checkout document before payment completes -- this looks like a receipt but does not confirm the payment succeeded.
- Never relay FastSpring's "no payment found" response directly to the customer after only one search. Always ask for proof first.
- Correct holding phrase: "We're checking with our payment team and will follow up shortly."

---

# Subscription Cancellation

## Cancel Subscription — Full cancellation steps

### Summary

**Issue:** Customer wants to cancel their Universal License subscription.

### Resolution

1. Go to https://softorino.com/submanager/
2. Enter the email address used to purchase.
3. Check inbox for the "Softorino Access Link" email and click the sign-in link.
4. In the dashboard, click "Manage Subscription" (redirects to FastSpring).
5. On the FastSpring page, enter the email address again.
6. Open the "Softorino Checkout" email from FastSpring and click the link inside.
7. In the Orders Management Dashboard, go to the **Subscriptions** tab.
8. Find Universal License → click **Manage** → click **Cancel Subscription**.
9. Confirm cancellation -- customer should receive a confirmation email from FastSpring.

If the "Manage Subscription" button is missing:
- The button appears inside the license detail view, not on the main dashboard page. Ask the customer to click into their license first, then look for "Manage Subscription" in the detail area.
- If still missing after correct navigation -- escalate to @AndrewQA.

### Internal Notes

- Cancellation prevents future renewals only -- access continues until the current paid period ends.
- Always tell the customer the exact date their access will expire.
- Do not call a missing button a bug unless confirmed -- it is usually a navigation issue.

---

# FastSpring — Payment Lookup

## How to locate an order when the email does not match

1. Search FastSpring by every email address the customer has provided.
2. If no result -- ask for PayPal Transaction ID.
3. Escalate to Andrew with Transaction ID. FastSpring support can locate orders by transaction reference even without a matching email.
4. If the receipt does not mention FastSpring as merchant -- the purchase may have gone through a different reseller. Flag to Andrew.

## PayPal + FastSpring relationship

- FastSpring is always the merchant of record when PayPal is used as the payment method on softorino.com.
- PayPal processes the money; FastSpring holds the order record.
- A PayPal receipt alone is not enough to confirm a FastSpring order exists -- always verify in FastSpring.

---

# Billing — Duplicate monthly subscription while old yearly license inactive

### Summary

**Product:** Billing
**Issue:** Duplicate monthly subscription while old yearly license inactive

### Symptoms

- Customer bought 1-month license thinking yearly existed.
- Old yearly license already expired/deactivated.
- Customer asks to extend old license by month.

### Common Customer Phrases

- "Can you cancel the new one and extend the old one?"
- "I wasted a monthly subscription."

### Questions to Ask

- Is old license active or expired?
- Is new monthly active?
- Does dashboard show Manage Subscription?

### Root Cause Candidates

- Old license expired; cannot extend deactivated license.
- Customer misunderstanding subscription states.

### Resolution

1. Explain old license is deactivated and cannot be extended.
2. Guide to Subscription Dashboard for cancellation.
3. If Manage button missing, explain user must first click Activate My Apps/license manager, then Manage Subscription appears in license detail area.

### Escalate If

- Manage Subscription button missing after correct navigation.

### Internal Notes

- Do not call it bug unless confirmed; often user is on wrong dashboard view.

---

# Billing / Angry Customer — Refund denied or customer distrusts remote session

### Summary

**Product:** Billing / Angry Customer
**Issue:** Refund denied or customer distrusts remote session

### Symptoms

- Customer accuses company of money grab.
- Customer refuses renewal.
- Customer thinks remote session is privacy risk.

### Common Customer Phrases

- "This is a money grab."
- "I do not trust remote access."
- "Cancel my subscription."

### Questions to Ask

- Does customer want troubleshooting, cancellation, or refund?
- Was refund policy already explained?

### Root Cause Candidates

- Unresolved product issue and poor communication.
- Remote session misunderstood.

### Resolution

1. Acknowledge frustration specifically.
2. Offer to continue helping via email if they want.
3. If they ask to cancel, provide cancellation steps without arguing.

### Escalate If

- Threats/legal claims.
- Refund exception needed.

### Internal Notes

- Do not be defensive. Do not over-explain policy if user asks only to cancel.
