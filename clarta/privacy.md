---
title: Clarta — Privacy Policy
permalink: /clarta/privacy/
---

# Clarta — Privacy Policy

**Effective date:** 9 October 2026
**Last updated:** 9 October 2026
**Applies to:** the Clarta iOS app (bundle identifier `com.sdx.Clarta`)

---

## The short version

- **Your letters are read on your iPhone.** Text recognition happens on the device.
- **Personal details are hidden before anything leaves your phone.** Names, addresses, bank and card
  numbers, phone numbers, email addresses, dates of birth and ID numbers are replaced with placeholders
  on the device. The page images that are sent have those details covered with black boxes.
- **Only that redacted copy goes to the cloud, and only with your consent.** It is sent to OpenAI,
  through our proxy, to write the explanation. OpenAI processes it in the EU, does **not** store it
  (`store: false`, Zero Data Retention) and does not use it for training.
- **Your explanations, deadlines, cases, documents and details are stored only on your devices** —
  and in your own iCloud if you keep iCloud sync on. We have no servers that store them.
- **The Wallet never leaves your phone for processing.** Documents you add there are read on the device.
- **No account.** Clarta has no sign-up, no email, no user profile.
- **Analytics are counts and bands only.** Nothing derived from a letter — no text, authority names,
  amounts, reference numbers or deadlines — is ever sent to analytics.

The rest of this document is the detail.

---

## 1. Who is responsible for your data

Clarta is published by **Pavel Koval** (the "controller" under the GDPR).

**Contact:** [evoke-support@proton.me](mailto:evoke-support@proton.me)

## 2. Your letters

### 2.1 Scanning and importing

You choose what Clarta sees: a page you scan with the camera, a photo you pick, or a PDF/image you
open in Clarta. Clarta asks for camera access only to scan. It does not need access to your photo
library — the system photo picker hands over only the images you select.

### 2.2 What happens on your iPhone

1. The text is recognised on the device (Apple Vision).
2. Personal details are detected and hidden on the device. Details you saved in **Settings › Your
   details**, your household members' details and your Wallet document numbers are always hidden.
   You can see what is hidden, and hide more, before you explain a letter ("See what we hide").
3. Before anything is sent, Clarta checks the outgoing request again and refuses to send it if any
   saved personal value is still in it.

### 2.3 What is sent to the cloud (with your consent)

To write the explanation, Clarta sends **the redacted text** and **redacted, reduced-resolution page
images** (longest edge 1024 px, up to six pages) to OpenAI through our proxy (§2.5). The same applies
to the free follow-up features you choose to use: questions about a letter, a full translation,
re-explaining in another language or style, drafting a reply, a form-filling guide, a case summary and
a general renewal guide for a document type (which contains only the document type and country).

Cloud explanations need your consent, asked in onboarding or before your first explanation. You can
withdraw it at any time in **Settings › Privacy & security › How your letters are processed**; letters
already explained stay on your iPhone.

### 2.4 OpenAI

OpenAI processes the redacted request to generate the answer, in an OpenAI project with **EU data
residency** and **Zero Data Retention**. Requests are sent with `store: false`. OpenAI does not use
API data to train its models.

### 2.5 Our proxy

Requests pass through a small proxy we run on **Cloudflare Workers** so that no API key is shipped in
the app. The proxy verifies that a request comes from a genuine copy of Clarta (Apple App Attest),
counts requests per device per day to prevent abuse, and forwards the request to OpenAI. It does not
store request contents and does not log them.

### 2.6 Placeholders are filled in on your phone

The cloud answer contains placeholders such as ⟦IBAN_1⟧. Clarta replaces them with the real values on
your iPhone — for example to show the account to pay, or your name and address in a reply letter.

## 3. What Clarta stores, and where

On your device (and in your private iCloud database if iCloud sync is on): page images, recognised
text, explanations, deadlines, cases, notes, replies and their PDFs, form answers, Wallet documents and
their photos, vocabulary, household members, your details and your signature. **We cannot access any
of it.** You can export it (**Settings › Privacy & security › Export my data**) or delete it (**Delete
all data**). Turning iCloud sync off keeps the data on this iPhone only.

Your purchased letter balance is stored in your iCloud Keychain so it survives a new phone; it is not
deleted by "Delete all data".

## 4. Purchases

Purchases are handled by Apple. We never see your payment details. The app records which product was
bought, its price and currency, and the App Store country, to keep your balance correct and to report
revenue in analytics (§5).

## 5. Analytics and crash reports

### 5.1 What is collected

Clarta uses Google Firebase (Analytics, Crashlytics, Performance, Remote Config), Amplitude (EU data
centre) and Meta's Facebook SDK (App Events) to understand how the app is used and to fix crashes.
Events describe actions and their outcome — for example that a letter was explained, how many pages
it had (as a band), how long it took, whether a deadline was found, and which plan is active. Your
country, region, app language and explanation language are sent as settings.

### 5.2 What is never collected

No letter text or images, no authority names, no amounts, no reference numbers, no deadlines or dates
from letters, no scam notes, no glossary words, no reply text, no names or contact details, and no
record identifiers. Numbers are sent as ranges ("2–3 pages"), never as raw values from a letter.

### 5.3 App Tracking Transparency

Clarta asks once whether you allow tracking. If you allow it, Firebase and Facebook may receive your
device's advertising identifier to measure which ads bring people to Clarta. You can change this at
any time in **iOS Settings › Privacy & Security › Tracking**.

## 6. Third parties who process data for us

| Provider | Purpose | Data |
|---|---|---|
| OpenAI (EU, ZDR) | Writing explanations and the other cloud features | Redacted letter text and redacted images |
| Cloudflare | Proxy between the app and OpenAI | The same redacted request, in transit only |
| Apple | Purchases, iCloud sync, App Attest | As per Apple's privacy policy |
| Google Firebase | Analytics, crash reports, performance, remote settings | Usage events, crash data, device identifiers |
| Amplitude (EU) | Product analytics | Usage events |
| Meta (Facebook SDK) | Measuring ad campaigns | Usage events; advertising identifier only if you allow tracking |

## 7. Legal bases (EU / UK GDPR)

- **Your consent** (Art. 6(1)(a)) for cloud explanations and, where applicable, for processing of
  special categories of data that a letter may contain (Art. 9(2)(a)), and for tracking.
- **Performance of a contract** (Art. 6(1)(b)) for providing the features you use and purchases.
- **Legitimate interests** (Art. 6(1)(f)) for analytics limited as described in §5 and crash reports.

## 8. Retention

Letters and everything derived from them stay on your devices until you delete them. OpenAI and our
proxy keep no copy. Analytics data is kept by the providers for their standard retention periods
(Firebase and Amplitude: up to 14 months for event data).

## 9. Your rights

You have the right to access, rectify, erase, restrict and port your data, to object, and to withdraw
consent at any time. Because your letters and details are stored only on your devices, you can
exercise most of these rights directly in the app (export and delete). For analytics data, contact us
(§1). You can also lodge a complaint with your data protection authority.

**California residents (CCPA/CPRA):** we do not sell personal information. If you allow tracking, the
advertising identifier may be shared with Meta and Google for ad measurement; you can refuse in iOS.

## 10. International transfers

OpenAI processing takes place in the EU. Analytics providers may process data outside your country,
including in the United States, under the EU Standard Contractual Clauses or equivalent safeguards.

## 11. Children

Clarta is not directed at children under 16.

## 12. Security

Personal details are hidden before any upload; outgoing requests are checked again before sending;
the proxy accepts only requests from genuine copies of Clarta; all traffic is encrypted (TLS). You can
protect the app or the Wallet with Face ID (**Settings › Privacy & security › Face ID lock**).

## 13. Not legal advice

Clarta explains letters. It does not give legal advice.

## 14. Changes to this policy

We will update this page when the app changes how it handles data, and bump the dates above.

## 15. Contact

**Pavel Koval** — [evoke-support@proton.me](mailto:evoke-support@proton.me)
