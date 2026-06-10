# pintr-dl

**pintr-dl** is a free, open-source, **self-hosted personal tool** that lets a single
user browse and download **their own** Pinterest boards and pins through the official
[Pinterest API (v5)](https://developers.pinterest.com/docs/api/v5/).

It presents your boards and pins in a fast, Pinterest-style masonry gallery that runs
entirely on your own computer or private LAN server, and lets you download images
individually or as a ZIP archive for offline, personal use.

---

## What this app does

- **Connects to your own Pinterest account** using Pinterest's official OAuth 2.0 login
  flow, requesting only the minimum **read-only** scopes.
- **Displays your boards and pins** in a responsive, Pinterest-like masonry grid with
  infinite scroll.
- **Proxies and caches pin images** through the backend so they load reliably and quickly
  on your local network.
- **Downloads images** that you select — one at a time, or many at once as a ZIP archive.
- **Re-displays previously downloaded ZIP archives** as a local offline viewer.

It is a **single-user, personal utility**. There is no central server operated by the
developer, no multi-user accounts, no sign-up, and no data is ever sent to the developer
or any third party. The person who runs the App is the same person who owns the Pinterest
account it connects to.

## Who runs this app

The App is **installed and run by an individual end user** on hardware they control (a
personal computer or a private home/LAN server). It is not a commercial or hosted
service. The developer publishes the source code only; each user deploys and operates
their own private instance.

## How it uses the Pinterest API

- Uses **only** the official **Pinterest API v5** — no scraping or unofficial methods.
- Requests the **minimum, read-only scopes**:
  - `boards:read`
  - `pins:read`
- **Cannot** post, edit, or delete anything on your account, and **cannot** access other
  users' private data — the API only returns data belonging to the authenticated user.
- Accesses only your **boards** (names, IDs, cover images) and your **pins** (image URLs
  and basic metadata such as title, description, and ID).

## Data & privacy

All data is stored **locally** on the device where you run the App. OAuth tokens, cached
images, and downloads never leave your machine, and the developer retains no copy of any
of your data.

See the full **[Privacy Policy](./privacy.md)** for details on what is accessed, how it is
stored, retention/deletion, and your rights.

## Features

| Area | Description |
| --- | --- |
| Boards & pins | Browse all boards and pins from your authorized Pinterest account |
| Gallery view | Pinterest-style masonry grid with infinite scroll |
| Image proxy/cache | Backend proxies and caches images (default 30-day TTL, 5 GB LRU cache) |
| Single download | Download any pin's image as a file |
| Bulk download | Select multiple pins and download them as a streamed ZIP archive |
| ZIP viewer | Re-open and browse previously downloaded ZIP archives offline |

## Tech stack

- **Backend:** Python + [FastAPI](https://fastapi.tiangolo.com/) (Pinterest API v5 client,
  image proxy/cache, ZIP streaming)
- **Frontend:** React + TypeScript (Pinterest-style masonry UI)
- **Deployment:** Docker / Docker Compose for self-hosting

## Getting started

> Detailed setup instructions are provided with the source. In short:

1. Register your own app on the
   [Pinterest Developer Portal](https://developers.pinterest.com/) and obtain a client ID
   and secret.
2. Configure your credentials (client ID/secret and OAuth redirect URI) in the App's
   environment configuration.
3. Run the App with Docker Compose on your own machine or private LAN server.
4. Complete the one-time Pinterest OAuth login in your browser to authorize the App to
   read your boards and pins.

The default development OAuth redirect URI is `http://localhost:8080/auth/callback`.

## Scope & limitations

- **Single user only** — no multi-user accounts or sign-up.
- **Read-only** — the App never modifies your Pinterest account.
- **Images only** — video pins are out of scope for the initial version.
- **Your own data only** — other users' boards/pins cannot be accessed (Pinterest API
  limitation by design).

## Compliance

The App is designed to comply with the
[Pinterest Developer Guidelines](https://developers.pinterest.com/),
the [Pinterest Developer Terms](https://developers.pinterest.com/terms/), and the
Pinterest Terms of Service. It uses only the official Pinterest API v5 with the minimum
read-only scopes and accesses only data belonging to the authenticated user.

## Contact

Questions or issues? Email the developer at **hideki1207d@gmail.com**
## License

This project is released as free, open-source software for personal use.
