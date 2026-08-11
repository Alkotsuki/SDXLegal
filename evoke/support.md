---
title: Evoke — Support & FAQ
permalink: /evoke/support/
---

<style>
.evoke-hero {
  border-radius: 18px;
  padding: 2.25rem 1.75rem;
  margin: 0 0 2rem;
  color: #fff;
  background: linear-gradient(135deg, #1d1b25 0%, #3a3550 55%, #6f5bd0 100%);
  box-shadow: 0 12px 32px rgba(29, 27, 37, .22);
}
.evoke-hero h1 { margin: 0 0 .5rem; border: 0; color: #fff; font-size: 2rem; }
.evoke-hero p { margin: 0; color: rgba(255,255,255,.82); font-size: 1.05rem; line-height: 1.55; }
.evoke-hero .evoke-eyebrow {
  display: inline-block; margin-bottom: .9rem; padding: .25rem .7rem;
  border-radius: 999px; background: rgba(255,255,255,.14);
  font-size: .72rem; letter-spacing: .12em; text-transform: uppercase;
  color: rgba(255,255,255,.9);
}
.evoke-actions { display: flex; flex-wrap: wrap; gap: .65rem; margin: 1.5rem 0 2.25rem; }
.evoke-btn {
  display: inline-block; padding: .7rem 1.15rem; border-radius: 12px;
  font-weight: 600; font-size: .95rem; text-decoration: none;
  border: 1px solid rgba(120,110,160,.35); color: #2f2a45; background: #f4f2fb;
  transition: transform .12s ease, box-shadow .12s ease;
}
.evoke-btn:hover { text-decoration: none; transform: translateY(-1px); box-shadow: 0 6px 16px rgba(60,50,110,.14); }
.evoke-btn-primary { background: #5b46c4; border-color: #5b46c4; color: #fff; }
.evoke-btn-primary:hover { color: #fff; }
.evoke-section-title {
  margin: 2.25rem 0 .75rem; font-size: .78rem; letter-spacing: .14em;
  text-transform: uppercase; color: #6a6480; font-weight: 700;
}
.evoke-faq {
  border: 1px solid #e3e0ee; border-radius: 12px; margin-bottom: .6rem;
  background: #fff; overflow: hidden;
}
.evoke-faq > summary {
  cursor: pointer; padding: .95rem 1.1rem; font-weight: 600; color: #2f2a45;
  list-style: none; position: relative; padding-right: 2.4rem;
}
.evoke-faq > summary::-webkit-details-marker { display: none; }
.evoke-faq > summary::after {
  content: "+"; position: absolute; right: 1.1rem; top: .85rem;
  font-size: 1.25rem; line-height: 1; color: #8a83a8; font-weight: 400;
}
.evoke-faq[open] > summary::after { content: "\2013"; }
.evoke-faq[open] > summary { border-bottom: 1px solid #efedf6; }
.evoke-faq > div { padding: .9rem 1.1rem 1.1rem; color: #3d3853; line-height: 1.6; }
.evoke-faq > div p { margin: 0 0 .7rem; }
.evoke-faq > div p:last-child { margin-bottom: 0; }
.evoke-faq > div ul { margin: 0 0 .7rem 1.1rem; padding: 0; }
.evoke-contact {
  margin: 2.5rem 0 1rem; padding: 1.6rem 1.5rem; border-radius: 16px;
  background: #f4f2fb; border: 1px solid #e3e0ee; text-align: center;
}
.evoke-contact h2 { margin: 0 0 .4rem; border: 0; font-size: 1.25rem; color: #2f2a45; }
.evoke-contact p { margin: 0 0 1.1rem; color: #5c5675; }
.evoke-meta { color: #6a6480; font-size: .85rem; }
@media (prefers-color-scheme: dark) {
  .evoke-faq { background: rgba(255,255,255,.03); border-color: rgba(255,255,255,.14); }
  .evoke-faq > summary, .evoke-faq > div, .evoke-contact h2 { color: inherit; }
  .evoke-faq[open] > summary { border-bottom-color: rgba(255,255,255,.1); }
  .evoke-contact { background: rgba(255,255,255,.04); border-color: rgba(255,255,255,.14); }
  .evoke-contact p, .evoke-meta { color: rgba(255,255,255,.65); }
  .evoke-btn { background: rgba(255,255,255,.06); border-color: rgba(255,255,255,.18); color: inherit; }
  .evoke-btn-primary { background: #6f5bd0; border-color: #6f5bd0; color: #fff; }
}
</style>

<div class="evoke-hero">
  <span class="evoke-eyebrow">Evoke for iPhone</span>
  <h1>Support &amp; FAQ</h1>
  <p>One tap turns a photo into a graded edit. Here is how it works, what it costs, and where your
  pictures go — plus a way to reach a human.</p>
</div>

<div class="evoke-actions">
  <a class="evoke-btn evoke-btn-primary" href="mailto:evoke.support@gmail.com?subject=Evoke%20support">Contact support</a>
  <a class="evoke-btn" href="https://alkotsuki.github.io/SDXLegal/evoke/privacy/">Privacy Policy</a>
  <a class="evoke-btn" href="https://www.apple.com/legal/internet-services/itunes/dev/stdeula/">Terms of Use (EULA)</a>
</div>

<p class="evoke-section-title">Getting started</p>

<details class="evoke-faq">
  <summary>What does Evoke actually do?</summary>
  <div>
    <p>Pick a photo, tap <strong>Evoke</strong>, and the app proposes a complete edit — exposure,
    contrast, colour, and local adjustments such as lifting the subject away from the background.
    You compare it against the original, keep it or reject it, and export the result to your photo
    library. The original is never modified.</p>
  </div>
</details>

<details class="evoke-faq">
  <summary>How do I change the result I was given?</summary>
  <div>
    <p>Two ways. You can nudge the individual sliders on the edit, or you can ask for a refinement in
    plain words — “warmer”, “less contrast”, “brighten the face”. Refinements never cost an edit.</p>
  </div>
</details>

<details class="evoke-faq">
  <summary>Where does the edited photo go?</summary>
  <div>
    <p>Exporting writes a <em>new</em> image into your photo library at full resolution. Your original
    stays exactly as it was. Evoke needs add-only photo access for this, which iOS asks for the first
    time you export.</p>
  </div>
</details>

<details class="evoke-faq">
  <summary>Evoke can't see my photos.</summary>
  <div>
    <p>Open <strong>iOS Settings → Privacy &amp; Security → Photos → Evoke</strong> and choose
    <em>Full Access</em>, or <em>Limited Access</em> plus the photos you want to edit. If you picked
    limited access, Evoke only ever sees the pictures you selected there.</p>
  </div>
</details>

<p class="evoke-section-title">On-device and cloud</p>

<details class="evoke-faq">
  <summary>Is my photo uploaded anywhere?</summary>
  <div>
    <p>Not by default. Evoke's standard path runs entirely on your iPhone using Apple's Vision and
    Core Image, and on supported devices Apple Intelligence. Nothing about the picture leaves the
    phone.</p>
    <p>Cloud analysis is opt-in and per edit. When you choose it, a reduced-resolution copy of that
    one photo (longest edge 1024 px, JPEG) is sent to the AI model to be looked at, with retention
    disabled. The edit itself is then applied locally at full resolution. The full details are in the
    <a href="https://alkotsuki.github.io/SDXLegal/evoke/privacy/">Privacy Policy</a>.</p>
  </div>
</details>

<details class="evoke-faq">
  <summary>The app says it used a different mode than I picked. Why?</summary>
  <div>
    <p>If a requested path is unavailable — Apple Intelligence not ready on your device, no network,
    or the cloud model failing — Evoke falls back to the next best one rather than showing you
    nothing. It always tells you when that happens instead of quietly substituting. A fallback to an
    on-device result is never charged as a cloud edit.</p>
  </div>
</details>

<details class="evoke-faq">
  <summary>Why is Apple Intelligence unavailable for me?</summary>
  <div>
    <p>Apple Intelligence requires a supported iPhone, a supported language and region, and needs to
    have finished downloading its models in iOS Settings. Until then Evoke uses its own on-device
    rules, which work on every supported device.</p>
  </div>
</details>

<details class="evoke-faq">
  <summary>It said I've reached a daily limit.</summary>
  <div>
    <p>That is a fair-use pause on the shared cloud service, not a problem with your account or your
    purchase. On-device editing keeps working, and the cloud path becomes available again shortly.</p>
  </div>
</details>

<p class="evoke-section-title">Purchases</p>

<details class="evoke-faq">
  <summary>What is free, and what costs money?</summary>
  <div>
    <p>Everything on-device is free and unlimited. Cloud analysis is what is metered: you get three
    free cloud edits, after which you can subscribe for unlimited cloud edits or buy a one-off pack
    of credits. If you never turn on cloud analysis, you will never meet the paywall.</p>
  </div>
</details>

<details class="evoke-faq">
  <summary>I paid but my edits weren't unlocked.</summary>
  <div>
    <p>Open <strong>Settings → Restore purchases</strong> in the app. A subscription is always
    restored from your Apple Account; credit packs are stored in your iCloud Keychain and follow you
    to a new device signed in with the same Apple Account. If it still doesn't appear, email us with
    the date of purchase and we'll sort it out.</p>
  </div>
</details>

<details class="evoke-faq">
  <summary>How do I cancel my subscription?</summary>
  <div>
    <p>Subscriptions are billed by Apple, so they are cancelled in Apple's own settings:
    <strong>iOS Settings → your name → Subscriptions → Evoke → Cancel</strong>. You keep access until
    the end of the period you've already paid for.</p>
  </div>
</details>

<details class="evoke-faq">
  <summary>Can I get a refund?</summary>
  <div>
    <p>Refunds for App Store purchases are handled by Apple, not by us — request one at
    <a href="https://reportaproblem.apple.com">reportaproblem.apple.com</a>. If something in the app
    went wrong, please write to us as well so we can fix it.</p>
  </div>
</details>

<details class="evoke-faq">
  <summary>Do I need an account?</summary>
  <div>
    <p>No. Evoke has no sign-up, no login and no user profile. Purchases are tied to your Apple
    Account, and everything else lives on your device.</p>
  </div>
</details>

<p class="evoke-section-title">Privacy and data</p>

<details class="evoke-faq">
  <summary>What does Evoke store about me?</summary>
  <div>
    <p>Only the numeric recipe of an edit — exposure, contrast, and so on — and a record of which
    edits you kept or rejected, so suggestions match your taste over time. No image data is ever
    stored by the app, and nothing derived from a photo's content is ever sent to analytics.</p>
  </div>
</details>

<details class="evoke-faq">
  <summary>How do I turn off analytics, or delete what Evoke remembers?</summary>
  <div>
    <p>Analytics: <strong>Settings → Privacy → Share anonymous usage data</strong>. Taste history and
    saved edits can be cleared from Settings, and deleting the app removes everything held on the
    device.</p>
  </div>
</details>

<details class="evoke-faq">
  <summary>Something crashed, or an edit looks wrong.</summary>
  <div>
    <p>Email us with your iPhone model, your iOS version, the Evoke version from
    <strong>Settings → About</strong>, and what you were doing at the time. A screenshot of the
    result helps. Please don't send photos you'd rather not share — a description is usually enough.</p>
  </div>
</details>

<div class="evoke-contact">
  <h2>Still stuck?</h2>
  <p>Write to us and a person will read it. We usually reply within two business days.</p>
  <a class="evoke-btn evoke-btn-primary" href="mailto:evoke.support@gmail.com?subject=Evoke%20support">Email evoke.support@gmail.com</a>
</div>

<p class="evoke-meta">Evoke is published by Pavel Koval.
<a href="https://alkotsuki.github.io/SDXLegal/evoke/privacy/">Privacy Policy</a> ·
<a href="https://www.apple.com/legal/internet-services/itunes/dev/stdeula/">Terms of Use</a> ·
Last updated 11 August 2026.</p>
