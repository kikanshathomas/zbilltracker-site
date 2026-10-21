# Changelog

All notable changes to the Zombie Bill Tracker website (zbilltracker.com) are
documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased] - 2026-10-20

### Added

- `readme.md` describing the site, its page set, how changes ship and how to
  verify the live site. Repository document only; not part of the site.
- Privacy policy: a description of the on-device crash log, including what it
  records, that it is part of the phone's own backup and of the optional
  Documents backup file, and that it leaves the phone only through that backup
  or a user-initiated "Export diagnostics".
- Privacy policy: the Run at startup, Keep awake and Vibration permissions
  requested by the Android app, with the reason for each.
- Privacy policy: an explanation of the Documents backup file that versions
  before 1.1.0 created automatically, the one-time notice shown after updating,
  and the fact that the app never deletes the file.
- Privacy policy: a full description of the website's GoatCounter visit
  counting, covering what is recorded, what is not, the hosts the browser
  contacts, and a link to GoatCounter's privacy policy.
- Privacy policy: a note that the iPhone and iPad version is planned and that
  the Apple, App Store and iCloud sections apply only once it is released.

### Changed

- The changelog file is now named `changelog.md` (lowercase), following the
  company file naming rule.
- Privacy policy effective date is now October 20, 2026.
- Privacy policy: the Google backup is described as current and Apple or
  iCloud backup as future; section 11 is now titled
  "Apple (planned iPhone version)".
- Privacy policy: the statement that the app does not request internet access,
  and the permissions list, now apply specifically to the Android app.
- Privacy policy: device backup now states that the backup holds everything
  the app stores and is also used for Android device-to-device transfer.
- "No tracking" and "no analytics" statements on the homepage, download page
  and privacy policy (descriptions, cards, statistics, FAQ and footers) now
  refer to the app, since the website counts visits.
- Homepage offline FAQ, in both the visible text and the structured data, now
  explains that data leaves the phone only through the phone's own backup or a
  file the user exports.
- Homepage privacy FAQ now refers to backup to the user's Google account only.
- The homepage and download page no longer state a price; they describe the
  app as a one-time purchase, with Google Play as the source of the current
  price. The price offer was removed from the homepage structured data.
- Sitemap last-modified dates for the homepage, download page and privacy
  policy are now 2026-10-20.
- Icon, store badge and social share images were recompressed losslessly
  (pixel-identical), reducing their combined size from 1,373,968 to 901,104
  bytes (about 34 percent).

### Fixed

- Privacy policy no longer says bill data is "never sent anywhere"; it now says
  bill data is never sent to GoatCounter or to Ubersoft, consistent with the
  device backup disclosure.

### Removed

- Unused styles and the initials-avatar script for the former HTML phone
  mock-ups on the homepage (about 9.6 KB). There is no visible change.
- The "Internet: declared by the app framework" permission entry from the
  privacy policy.

### Security

- GoatCounter is now loaded from the versioned script
  `https://gc.zgo.at/count.v4.js` over HTTPS with Subresource Integrity
  (SHA-384) and `crossorigin="anonymous"` on all pages, instead of the
  unversioned, protocol-relative `//gc.zgo.at/count.js`.
