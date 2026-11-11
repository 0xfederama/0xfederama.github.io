---
title: Privacy policy
---

*Last updated: 2026-11-11*

This policy covers **Collections**, a personal, non-commercial, self-hosted project run by me, Federico Ramacciotti, as an individual, and this website (federama.dev).

## Collections

Collections is a private app for organizing lists of items (books, films, etc.). It runs on my own Raspberry Pi at home and is reachable at collections.federama.dev only by people I have invited. It uses two Google OAuth apps.

### "Collections": Sign in with Google

Signing in to collections.federama.dev goes through Cloudflare Access with "Sign in with Google", using the scopes `openid`, `email` and `profile`. Cloudflare Access only checks whether your email address is on my allow list.

The app receives your email address, plus your name and profile picture if Google provides them, and stores them on my server to identify you and to show who owns or shares a list. No passwords are stored. Cloudflare processes the login as part of Cloudflare Access; see [Cloudflare's privacy policy](https://www.cloudflare.com/privacypolicy/).

### "Collections Backup": Google Drive

This app is used only by the server's backup job (rclone) with my own Google account, with the `drive.file` scope, which means it can only see files it created itself. Every night it uploads an encrypted backup of the app's data (the database plus uploaded images, encrypted before leaving the server) to my own Google Drive. It never reads, lists or changes any other Drive files.

### How Google user data is used

Google user data is used only to provide the features described above. It is not sold, not shared with third parties (except Cloudflare and Google as part of the login and storage described above), not used for advertising, and not used to train AI or machine-learning models.

The use of information received from Google APIs adheres to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the Limited Use requirements.

### Retention and deletion

Account data is kept while you have access to Collections. You can ask me to delete your account and data at any time by writing to [vgfede@gmail.com](mailto:vgfede@gmail.com). Backups rotate and expire: local copies within about a month, Google Drive copies once they are older than the last 30 backups.

You can also revoke the app's access to your Google account at any time at [myaccount.google.com/permissions](https://myaccount.google.com/permissions).

## This website

federama.dev does not use analytics and does not set its own cookies. Its pages load a script and stylesheet from latest.cactus.chat (a comment widget included by the site theme), so that service receives the standard request data your browser sends, such as your IP address.

## Contact

Questions about this policy: [vgfede@gmail.com](mailto:vgfede@gmail.com).
