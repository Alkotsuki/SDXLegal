---
title: Evoke — Privacy Policy
permalink: /evoke/privacy/
---

# Evoke — Privacy Policy

**Effective date:** 10 August 2026
**Last updated:** 10 August 2026
**Applies to:** the Evoke iOS app (bundle identifier `com.sdx.Evoke`)

---

## The short version

- **Your photographs stay on your device by default.** Evoke's default enhancement runs entirely
  on‑device. Nothing about the picture leaves your iPhone.
- **The cloud path is opt‑in, per edit.** If — and only if — you choose cloud analysis, a
  **reduced‑resolution copy** (longest edge 1024 px, JPEG) of that one photo is sent to an AI model
  to be looked at, and it is **not stored** by the model provider.
- **Evoke never stores your images.** Not on our servers — we have no photo servers — and not in the
  app's own database. The app saves only the *numeric recipe* of an edit (exposure, contrast, and so
  on), never image data.
- **Evoke has no accounts and no user IDs.** No sign‑up, no email, no profile. There is nothing to
  log in to.
- **Analytics is counts and timings only,** and you can switch it off in **Settings → Privacy →
  Share anonymous usage data**.
- **Nothing derived from the *content* of a photograph is ever sent to analytics** — not the photo's
  identifier, not the text you type into a refinement request, not the AI's description of the
  scene, not any measurement of the image.

The rest of this document is the detail.

---

## 1. Who is responsible for your data

Evoke is published by **Pavel Koval**, an individual developer, who is the data controller for the
purposes of the UK GDPR and EU GDPR.

**Contact:** [evoke-support@proton.me](mailto:evoke-support@proton.me)

Please use that address for any privacy question, request, or complaint.

---

## 2. Your photographs

### 2.1 Access to your photo library

Evoke asks for photo library access so you can pick a picture to edit, and for add‑only access so it
can save the result back. Evoke reads **only the photo you open**. It does not scan, index, upload,
or catalogue your library, and it does not read photo metadata beyond what iOS provides to display
the picker (such as the capture date shown in the grid).

You can change or revoke this access at any time in **iOS Settings → Privacy & Security → Photos →
Evoke**. If you grant limited access, Evoke sees only the photos you selected.

### 2.2 On‑device processing (the default)

By default, Evoke analyses and edits your photo entirely on your device, using Apple's Vision, Core
Image, and — where your device supports it — Apple Intelligence on‑device models. In this mode
**no image data, and nothing computed from your image, leaves your device.**

### 2.3 Cloud analysis (optional)

Evoke can also ask a third‑party AI model to propose an edit. This path is **off by default** and
requires your explicit consent. When you use it, for that single edit:

- Evoke creates a **reduced‑resolution copy** of the photo — downscaled so its longest edge is at
  most **1024 pixels**, encoded as JPEG — and sends that copy, together with a technical description
  of the image's light and colour statistics and the editing instruction, to our AI proxy.
- The proxy forwards the request to **OpenAI**, which returns a proposed edit as structured data.
  The request is sent with retention disabled (`store: false`), asking OpenAI **not to retain** the
  image or the response.
- The reduced copy exists only in memory for the duration of that one request. It is **not written
  to disk, not logged, and not cached** — by the app or by the proxy.
- The edit itself is then applied **locally, at full resolution**. Your full‑resolution photo is
  never transmitted.
- Free‑text refinement requests you type (e.g. "warmer, less contrast") are sent to the AI model as
  part of that request, because they are the instruction. They are not stored by us and are never
  sent to analytics.

The app always tells you which path actually produced an edit, including when a cloud request fell
back to on‑device processing.

You can set cloud analysis to **ask each time** (the default) or to **always allow** in
**Settings → Privacy → Allow cloud analysis**. If you never enable it, no photo data ever leaves
your device.

### 2.4 Our AI proxy

Cloud requests do not go to OpenAI directly. They pass through a stateless proxy we run on
**Cloudflare Workers**, which exists so that no API credential has to be shipped inside the app. The
proxy authenticates each request using Apple's **App Attest**, which proves the request came from a
genuine, unmodified copy of Evoke on a real Apple device. App Attest identifies *the app instance*,
not you: it carries no name, email, account, or advertising identifier. The proxy does not store
request bodies or images.

Cloudflare, as a network provider, may process transient connection metadata (such as IP address)
for security and abuse prevention, as any internet intermediary does.

---

## 3. What Evoke stores on your device

None of this is transmitted to us. It lives on your device and is removed when you delete the app
(except where noted).

| What | Where | Why |
| --- | --- | --- |
| **Edit recipes** — numeric adjustment values per photo, keyed to the photo | App database (SwiftData) | So reopening a photo restores your edit. **No image bytes are ever stored.** |
| **Taste history** — that you kept or rejected an edit, and the direction of its adjustments | App database (SwiftData) | So suggestions drift towards the look you prefer. Clearable via **Settings → Privacy → Clear taste history**. |
| **Preferences** — cloud consent answer, preferred processing path, analytics opt‑out, install week | `UserDefaults` | App settings. |
| **Purchased credit balance and free‑edit counter** | iOS Keychain | To remember what you bought. The purchased balance is **synced through your own iCloud Keychain** so it survives a new device; the free counter is device‑local. We cannot read your Keychain. |

---

## 4. Purchases

Evoke offers an unlimited subscription and consumable edit packs. All payment processing is handled
by **Apple** through the App Store.

- **We never see or receive your payment details** — no card numbers, no billing address, no Apple
  Account credentials.
- There is **no purchase backend and no receipt server**. Entitlement is verified on your device
  against StoreKit and stored in your Keychain, as described above.
- Prices shown in the app come from the App Store for your region.
- Purchase and subscription **management, refunds, and cancellation** are handled by Apple. See
  Apple's own privacy policy for how it processes your purchase data.

The fact that a purchase or subscription event occurred, and its product identifier, price, and
currency, are sent to our analytics providers as revenue data (see §5). This is transaction
information, not payment information.

---

## 5. Analytics

Evoke collects anonymous usage analytics to understand which features are used and where the app is
slow or failing. Events are sent to **Google Firebase Analytics** and **Amplitude** (EU data
region).

### 5.1 What is collected

- **Product interaction** — which screens were opened, which actions were taken, which step of a
  flow was reached, whether an edit was kept or rejected.
- **Performance** — how long operations took (in milliseconds and as coarse bands), and error or
  failure categories.
- **Purchase events** — subscription and pack purchases, restores, and revocations, as described in §4.
- **Coarse install attributes** — 17 "user properties" describing this installation, such as whether
  cloud analysis is enabled, the current subscription state, whether on‑device AI is available, the
  ISO week the app was installed, and *banded* counts of lifetime edits (e.g. "11–50" rather than an
  exact number).
- **Identifiers assigned by the analytics providers themselves** — Firebase's app‑instance ID and
  Amplitude's device ID. These are per‑app pseudonymous identifiers. **Evoke does not create a user
  ID of its own** and deliberately does not use your device's vendor identifier as one.
- **The advertising identifier (IDFA)** — **only** if you allow tracking when iOS asks (see §5.4).

### 5.2 What is never collected

This is enforced in the app's code, not merely promised here. Analytics **never** receives:

- your photographs, or any part of them;
- the identifier of any photo in your library;
- the free‑text refinement requests you type;
- the AI's textual explanation, intent, or scene label for a photo;
- any raw numeric measurement of an image — the app's analytics layer has **no facility for sending a
  raw decimal value at all**, so an image measurement cannot be transmitted even by mistake. Where a
  magnitude is meaningful, only a coarse band is sent;
- your name, email address, phone number, contacts, precise location, or health data — Evoke does not
  ask for or access any of these.

### 5.3 Turning it off

**Settings → Privacy → Share anonymous usage data.** Switching this off stops event collection for
both providers, and the choice persists across app launches and updates. Analytics is **on by
default** for a user who has not made a choice.

### 5.4 App Tracking Transparency

Evoke asks the iOS "Allow tracking?" prompt **once**, and only *after* you have kept your first
edit — never on first launch. If you allow it, the IDFA is shared with Firebase so we can tell which
promotions bring people to the app. If you deny it — or never answer — no advertising identifier is
collected, and everything else in the app works identically. You can change this at any time in
**iOS Settings → Privacy & Security → Tracking**.

Amplitude never receives an advertising identifier.

---

## 6. Third parties who process data for us

| Provider | Role | What it receives |
| --- | --- | --- |
| **Apple** | App distribution, in‑app purchases, on‑device AI, App Attest | Purchase and subscription data; attestation. Governed by Apple's privacy policy. |
| **Cloudflare** | AI request proxy (only when you use cloud analysis) | Transient request traffic, including the reduced photo copy in transit; connection metadata. Not stored. |
| **OpenAI** | AI model that proposes an edit (only when you use cloud analysis) | The reduced‑resolution photo copy and the editing instruction, sent with retention disabled. |
| **Google (Firebase Analytics)** | Product analytics | The events and identifiers in §5, plus the IDFA only if you allowed tracking. |
| **Amplitude** | Product analytics (EU data region) | The events and identifiers in §5. No advertising identifier. |

We do not sell your personal information, and we do not share it for cross‑context behavioural
advertising.

---

## 7. Legal bases (EU / UK GDPR)

| Purpose | Legal basis |
| --- | --- |
| Editing the photo you chose, on device | Performance of a contract — it is the service you asked for (Art. 6(1)(b)) |
| Sending a reduced photo copy for cloud analysis | Your **consent**, given per edit or via the "always allow" setting (Art. 6(1)(a)) |
| Usage analytics and performance measurement | Your **consent**, withdrawable at any time via the Settings toggle (Art. 6(1)(a)) |
| Advertising identifier / attribution | Your **consent**, given through the iOS tracking prompt (Art. 6(1)(a)) |
| App Attest verification and abuse prevention on our proxy | Legitimate interests — protecting the service from misuse (Art. 6(1)(f)) |
| Recording your purchase entitlement | Performance of a contract (Art. 6(1)(b)) |

Withdrawing consent does not affect processing already carried out.

---

## 8. Retention

- **On your device:** kept until you delete it (clear taste history, remove a saved edit) or delete
  the app. Deleting Evoke removes its database and preferences. The iCloud‑synced purchase balance
  may persist in your iCloud Keychain so that reinstalling restores what you bought.
- **Photos sent for cloud analysis:** not retained. The request asks the model provider not to store
  it, and the copy is discarded from memory as soon as the edit is returned.
- **Analytics events:** retained by Firebase and Amplitude under their configured retention periods,
  currently no longer than **14 months**, after which they persist only in aggregate reports.

---

## 9. Your rights

Depending on where you live, you may have the right to access, correct, delete, or export your
personal data, to object to or restrict processing, to withdraw consent, and to lodge a complaint
with a supervisory authority.

Because Evoke has **no accounts**, most of your data is under your direct control:

- **Stop analytics collection:** Settings → Privacy → Share anonymous usage data.
- **Stop all photo transmission:** leave cloud analysis off, or set it back to "ask each time".
- **Delete your taste history:** Settings → Privacy → Clear taste history.
- **Delete everything the app holds:** delete the app from your device.
- **Revoke tracking:** iOS Settings → Privacy & Security → Tracking.
- **Revoke photo access:** iOS Settings → Privacy & Security → Photos → Evoke.

For anything you cannot do yourself — including a request that we ask our analytics providers to
delete the pseudonymous records associated with your installation — email
[evoke-support@proton.me](mailto:evoke-support@proton.me). Please note that because we hold no
account identifier, we may need the analytics app‑instance ID from your device to locate any
records; we will explain how to find it. We will respond within one month.

**California residents (CCPA/CPRA):** we do not sell or share personal information as those terms
are defined, and we do not use it for cross‑context behavioural advertising beyond the attribution
described in §5.4, which is subject to your consent. You may exercise your rights to know, delete,
and correct through the same address, and you will not be discriminated against for doing so.

---

## 10. International transfers

Evoke's providers may process data outside your country, including in the United States. Amplitude
is configured to use its **EU data region**. Transfers by Google, Amplitude, Cloudflare, OpenAI, and
Apple rely on the safeguards those providers offer, including the European Commission's Standard
Contractual Clauses and, where applicable, the EU–US Data Privacy Framework.

---

## 11. Children

Evoke is not directed at children and is not intended for anyone under 13 (or the minimum age of
digital consent where you live, if higher). We do not knowingly collect personal data from
children. If you believe a child has provided data to us, contact us and we will address it.

---

## 12. Security

- Photographs are processed on your device wherever possible; when they are not, only a
  reduced‑resolution copy travels, over TLS.
- Our proxy holds no API credential in the app, and accepts only requests attested by Apple's App
  Attest.
- Purchase balances are stored in the iOS Keychain, protected by the system. A stored record that
  cannot be validly read is never overwritten — a corrupted balance is preserved rather than
  silently zeroed.
- No system is perfectly secure, and we cannot guarantee absolute security.

---

## 13. Changes to this policy

If we change how Evoke handles data, we will update this page and its "Last updated" date. Material
changes will be signalled in the app. The current version is always available at the link in
**Settings → Privacy**.

---

## 14. Contact

**Pavel Koval**
[evoke-support@proton.me](mailto:evoke-support@proton.me)

If you are in the EU or UK and are unhappy with our response, you may complain to your local data
protection authority.
