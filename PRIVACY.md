# Think Backwards — Privacy Policy

Last updated: 2026-05-17

This policy explains what information the Think Backwards application
("the App") and its hosted website at **thinkbackwards.app** collect,
store, or transmit. The short version: **the App does not collect any
personal information**. The longer version is below.

---

## 1. What the App does NOT do

The App has no accounts, no sign-up, no login. It does not collect:

- Your name, email address, phone number, or any other identifier.
- Your real-world location.
- Analytics, telemetry, usage metrics, crash reports, or behavioral
  tracking of any kind.
- Player names you enter for in-app scorekeeping — those stay on the
  device they were typed on and are never transmitted anywhere.
- Cookies for tracking purposes. The hosted webapp uses local browser
  storage (IndexedDB and `localStorage`) only to remember your
  settings, your category library, and your local leaderboard between
  sessions on the same device.

The App contains no third-party advertising, no ad SDKs, and no
trackers.

---

## 2. What the App stores locally on your device

Your settings, the categories you have installed, and your local
leaderboard are stored on your device using the browser's built-in
IndexedDB (via Dexie) and `localStorage`. This data:

- Stays on your device.
- Is never transmitted to the author or any third party.
- Can be cleared at any time via your browser's site-data settings,
  by uninstalling the native installer, or via the App's Settings
  screen.

---

## 3. Network requests the App makes

The App is offline-first. After the first visit, the web version
caches itself via a service worker and works without an internet
connection. The native installers (APK, EXE, MSI) bundle the App
directly and don't need a network connection at all to play.

The App makes outgoing network requests in only one scenario:

- **Downloading category packs.** When you visit the **Categories →
  Available** tab, the App makes requests to the **GitHub API**
  (`api.github.com`) to list packs and to **raw.githubusercontent.com**
  to download them. By default these target the author's repository
  (`SenalKaranda/ThinkBackwardsCategories`); you can change the target
  to any other GitHub repository in Settings.

  These requests do not include any identifying information about
  you beyond what your browser or operating system normally sends
  (your IP address, user agent string, etc.). Those requests are
  governed by **GitHub's privacy policy**:
  <https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement>

---

## 4. The hosted website (thinkbackwards.app)

The hosted version of the App is served by **Vercel**. As part of
standard web hosting, Vercel may log routine request metadata (IP
address, timestamp, requested URL, user agent) in its server logs.
The author does not directly receive or process those logs. Vercel's
data practices are described here:
<https://vercel.com/legal/privacy-policy>

The hosted website does not run analytics scripts.

---

## 5. Third parties at a glance

| Service | Why it's involved | Their privacy policy |
|---|---|---|
| GitHub | Hosts the downloadable category packs and the public installer releases | https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement |
| Vercel | Hosts the web version (thinkbackwards.app) | https://vercel.com/legal/privacy-policy |

No other third parties are involved in normal use of the App.

---

## 6. Children

The App is suitable for general audiences and is not directed at
children under 13. The App does not knowingly collect any information
from anyone, including children. Parents and guardians should
supervise their children's use of any internet-connected service.

---

## 7. Your rights (GDPR / CCPA / etc.)

Because the App does not collect or store any personal data on the
author's servers, there is nothing for the author to delete, export,
correct, or restrict on your behalf — your data simply isn't held by
the author. Data stored locally on your device is fully under your
control: clear it through your browser settings or by uninstalling
the App.

For data held by third parties (GitHub, Vercel) as part of their
normal hosting operations, please contact those services directly to
exercise your rights under their own policies.

---

## 8. Changes to this policy

The author may update this policy from time to time. The current
version is always available in the App (Main Menu → Legal) and at the
project repository. Material changes will be reflected in the
"Last updated" date at the top of this document.

---

## 9. Contact

Questions about this Privacy Policy: **catdadstudios@gmail.com**.

Copyright (c) 2026 Senal Karanda.
