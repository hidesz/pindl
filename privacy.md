# Privacy Policy for pintr-dl

**Last updated: June 10, 2026**

## 1. Overview

**pintr-dl** ("the App") is a free, open-source, self-hosted personal tool that lets a
single user view and download **their own** Pinterest boards and pins through the
official Pinterest API (v5).

The App is **not** a commercial service. It is installed and run by the same person who
owns the Pinterest account it connects to, on hardware that person controls (a personal
computer or a private LAN server). There is no central server operated by the developer,
no multi-user accounts, and no sign-up.

This Privacy Policy explains what information the App accesses, how that information is
used and stored, and the choices available to you. By installing and using the App, you
agree to the practices described here.

## 2. Information We Access

The App accesses the following data **only** from the Pinterest account that you
personally authorize through Pinterest's OAuth 2.0 login flow:

- **Boards** that belong to your authenticated account (board names, IDs, and cover images).
- **Pins** that belong to your authenticated account, including each pin's image URLs and basic metadata (title, description, ID).
- **OAuth tokens** (access token and refresh token) issued to you by Pinterest so the App can make API requests on your behalf.

The App requests the **minimum, read-only scopes** required for this purpose:

- `boards:read`
- `pins:read`

The App **does not** request write access, **cannot** post, edit, or delete anything on
your Pinterest account, and **cannot** access other users' private boards or pins
(Pinterest's API only returns data belonging to the authenticated user).

The App does **not** collect any other personal information such as your name, email
address, location, payment details, contacts, or device identifiers, and it does **not**
use cookies, analytics, advertising, or tracking technologies.

## 3. How We Use the Information

Accessed information is used solely to provide the App's core functionality on your own
device:

- Displaying your boards and pins in a gallery view.
- Proxying and caching pin images so they load reliably and quickly on your local network.
- Downloading selected images individually or as a ZIP archive at your request.
- Re-displaying previously downloaded ZIP archives that you have saved locally.

The information is **never** used for any other purpose, including profiling,
advertising, marketing, or resale.

## 4. Data Storage and Security

All data handled by the App is stored **locally**, on the device or private server where
you run the App. Nothing is transmitted to the developer or to any third party.

- **OAuth tokens** are stored in a local file (`tokens.json`) inside a directory you control. They are used only to authenticate your own API requests and are refreshed automatically by the App when they expire.
- **Cached images** are stored on the local filesystem with a default time-to-live of 30 days and a 5 GB size limit; the oldest cached images are automatically removed (least-recently-used eviction) when the limit is exceeded.
- **Downloaded files and ZIP archives** are saved only where you choose to store them on your own device.

Because the App is self-hosted, the security of the device, server, and network on which
you run it is your responsibility. We recommend running it only on trusted, private
hardware and keeping your Pinterest API credentials confidential.

## 5. Data Sharing and Disclosure

We do **not** sell, rent, share, or otherwise disclose your data to any third party. The
App communicates only with Pinterest's official API endpoints (to retrieve your boards,
pins, and images) and with no other external service.

## 6. Data Retention and Deletion

You are in full control of all stored data because it resides on your own device:

- **Revoke access:** You may revoke the App's access at any time from your Pinterest
  account settings (Settings → Apps / Security). Once revoked, the App can no longer
  access your Pinterest data.
- **Delete tokens:** Deleting the local `tokens.json` file removes the App's stored
  credentials.
- **Delete cached and downloaded data:** Deleting the App's local cache and download
  directories permanently removes all locally stored images and ZIP archives.

The developer retains **no** copy of your data, so there is nothing for the developer to
delete on your behalf.

## 7. Compliance with the Pinterest Platform

The App is designed to comply with the
[Pinterest Developer Guidelines](https://developers.pinterest.com/),
the [Pinterest Developer Terms](https://developers.pinterest.com/terms/), and the
Pinterest Terms of Service. It uses only the official Pinterest API v5, accesses only
data belonging to the authenticated user, and uses the minimum read-only scopes required.
The App does not use any unofficial scraping methods.

## 8. Children's Privacy

The App is not directed to children under the age of 13 (or the minimum age required in
your jurisdiction), and it does not knowingly collect any information from children.

## 9. Changes to This Privacy Policy

We may update this Privacy Policy from time to time. Any changes will be reflected by an
updated "Last updated" date at the top of this document. Continued use of the App after a
change constitutes acceptance of the revised policy.

## 10. Contact

If you have any questions, concerns, or requests regarding this Privacy Policy or
the App, you can contact the developer directly by email:

**Email: hideki1207d@gmail.com**

