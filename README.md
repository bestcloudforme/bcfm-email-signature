# bcfm-email-signature

Static image assets for the **Bestcloudfor.me** email signature.

The signature HTML references these files through [jsDelivr](https://www.jsdelivr.com/), so they load in Gmail, Outlook and Apple Mail without any extra hosting.

> **Do not delete, rename or overwrite files in this repo.** Every signature that has already been sent points here. If an image changes, every sent email changes with it.

## Usage

Reference images with a pinned version tag:

```
https://cdn.jsdelivr.net/gh/bcfmelman/bcfm-email-signature@v1/<file>.png
```

Example:

```html
<img src="https://cdn.jsdelivr.net/gh/bcfmelman/bcfm-email-signature@v1/logo_cloud.png" width="64" height="36" alt="">
```

Always use a tag (`@v1`), never `@main`. Pinned URLs keep existing signatures stable even if the repo changes.

## Assets

| File | Used for | Display size |
| --- | --- | --- |
| `logo_cloud.png` | BCFM cloud mark | 64×36 |
| `logo_text.png` | BESTCLOUDFOR.ME wordmark | 160×16 |
| `icon-mail.png` | Email | 14×14 |
| `icon-phone.png` | Phone | 14×14 |
| `icon-li_contact.png` | Personal LinkedIn link | 14×14 |
| `icon-li_social.png` | Company LinkedIn | 22×22 |
| `icon-yt.png` | Company YouTube | 22×22 |
| `icon-ig.png` | Company Instagram | 22×22 |
| `icon-x.png` | Company X | 22×22 |
| `icon-b_web.png` | Website button | 21×14 |
| `icon-b_medium.png` | Medium Blog button | 14×14 |
| `icon-b_spotify.png` | Devopsology Podcast button | 14×14 |

All images are exported at 2× for sharp rendering on high-DPI screens. Backgrounds are transparent.

## Adding the signature to Gmail

1. Open your signature HTML file in Chrome.
2. Select all (`Cmd+A` / `Ctrl+A`) and copy the rendered signature, not the source code.
3. In Gmail, go to **Settings → See all settings → General → Signature**.
4. Create a new signature, paste, and click **Save Changes** at the bottom of the page.
5. Set it as the default for new emails and replies, then send yourself a test email.

## Updating assets

1. Add the new or changed files. Do not touch existing ones.
2. Create a new release with the next tag (`v2`, `v3`, …).
3. Update the signature HTML to point to the new tag.

Older tags stay as they are, so signatures in emails that were already sent keep working.

## What not to commit

Only image assets belong here. Do not commit signature HTML files, since they contain personal phone numbers and email addresses.
