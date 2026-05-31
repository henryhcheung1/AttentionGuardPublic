# Attention Guard — Privacy Policy

**Last updated:** 2026-05-25

This is the privacy policy for **Attention Guard**, a Chrome browser extension that enforces a minimum watch time on YouTube videos before another video can be opened. The extension is intended for adults — most commonly parents — who want to manage their own viewing habits or those of someone they supervise.

This policy explains exactly what data the extension handles, where it goes, and what it does *not* do.

## TL;DR

- Attention Guard does **not** collect, transmit, or sell any personal information.
- It stores **two values** in your browser's local synced storage: your watch-time threshold (a number of seconds) and whether the extension is enabled (a boolean).
- It does **not** track browsing history, video titles, channels viewed, watch time, or any other YouTube activity.
- It does **not** use analytics, advertising networks, or third-party trackers.
- The optional feedback form is hosted by Google Forms; if you choose to fill it out, your responses go to the form's owner and are governed by Google's privacy policy.

---

## Information We Collect

### Stored locally in your browser

The extension stores **two pieces of configuration** via Chrome's `chrome.storage.sync` API:

| Key | Type | Default | What it is |
|---|---|---|---|
| `threshold_seconds` | integer | 60 | The minimum seconds a YouTube video must play before another can be opened. |
| `enabled` | boolean | true | Whether the extension is currently enforcing the lockout. |

These values are stored in your browser (and synced to your Google account if you have Chrome sync enabled, controlled entirely by Chrome's own sync settings). **They never leave your browser through any channel controlled by the extension.**

We collect nothing else. We do not store:

- Which videos you watch
- How long you watch them
- Channel names or video metadata
- Browsing history
- IP addresses
- Cookies
- Device identifiers
- Account information of any kind

### Permissions and why we have them

The extension declares two permissions in its manifest:

- **`storage`** — used solely to read and write the two configuration values above. No data is sent over the network.
- **`host_permissions: *://*.youtube.com/*`** — required to inject the content script that enforces the watch-time lockout on YouTube pages. The extension does not communicate with any server, including YouTube's, beyond what your browser does normally to load YouTube.

---

## How We Use Information

The two stored values are read by the extension on each YouTube page load to determine:

1. How long to wait before unlocking the page (`threshold_seconds`)
2. Whether to enforce the lockout at all (`enabled`)

That is the entirety of how data is used.

---

## Information Sharing

We do not share, sell, transmit, or license any information to any party.

There is no server. There is no backend. There is no third-party SDK, analytics tool, or advertising network bundled with the extension. The full source code is available for inspection on request — contact the developer at the email below.

---

## The Optional Feedback Form

The extension's options page includes a "Send feedback" link that opens a Google Form in a new tab. The form is **entirely optional** and **not required** to use the extension.

If you choose to fill out the form:

- Your responses are submitted to a Google Form owned by the developer.
- The form does not require sign-in. Responses are anonymous unless you choose to provide your email in the optional final question.
- Responses are stored in Google's infrastructure and governed by [Google's Privacy Policy](https://policies.google.com/privacy).
- The developer reviews responses to decide what to build next. Responses are not shared with third parties.

If you do not click "Send feedback," nothing about you is submitted anywhere.

---

## Data Retention and Deletion

Because no data leaves your browser, there is nothing for us to retain or delete server-side. The two stored values live in your browser and are deleted automatically when you uninstall the extension.

If you submitted the optional feedback form and want your response removed, contact the developer (below) with enough context to identify the response (timestamp, approximate content). It will be deleted from the linked spreadsheet on request.

---

## Children's Privacy

The extension is intended for adults who want to manage their own viewing habits or supervise a child's viewing. The extension itself does not interact directly with children, does not collect any data from any user (regardless of age), and is not designed to be operated by children.

Because the extension does not collect personal information, it falls outside the scope of laws designed to protect children's data (such as the United States' Children's Online Privacy Protection Act, COPPA). If you are a parent or guardian and have questions about how Attention Guard is used in your household, the source code is available on request and there is no data collection to worry about.

---

## Security

Because no data is transmitted, there is no risk of interception or unauthorized access to data the extension manages.

The two configuration values live in Chrome's `chrome.storage.sync` storage area, which is encrypted by Chrome and synced (if your Chrome sync is enabled) by Google's standard sync infrastructure. The security of that synchronization is governed by Chrome's and Google's terms.

---

## Your Rights and Controls

You have full control over the data stored by the extension:

- **Change it:** open the extension's options page and modify the threshold or enabled state at any time.
- **Reset it:** uninstall and reinstall the extension to return to default values.
- **Stop using it:** uninstall the extension, which removes all stored values.
- **Disable temporarily:** use the in-options toggle, or disable the extension from `chrome://extensions`.

EU and California residents have additional rights under GDPR and CCPA respectively. Because we do not collect data, most of these rights (access, deletion, portability, opting out of sale) have nothing to act on, but you may still contact us with any question or request.

---

## Changes to This Policy

If the extension's behavior changes in a way that affects what data is handled, this policy will be updated and the "Last updated" date at the top will reflect the change.

Substantive changes will be noted in the extension's Chrome Web Store listing release notes so that users can review them before updating.

---

## Contact

For privacy questions, data deletion requests, or anything else covered by this policy:

**Email:** henryhcheung1@gmail.com

The extension's source code is available for inspection on request. Email the address above to receive a copy.
