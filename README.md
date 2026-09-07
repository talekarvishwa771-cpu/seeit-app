```
​🕵️ seeit
​Hide any file inside a photo. No one will ever know it's there.
A steganography CLI tool that hides any file inside a cover image — the photo still opens perfectly fine, everywhere.
​⚠️ Note: This repo ships a protected build. The seeit.py here is obfuscated — this is a distribution copy for everyday use, not the original source.
​📸 What is this?
​Image viewers stop reading a JPG at its "end of image" marker. seeit hides your file after that marker — the photo opens completely normally in any gallery app, WhatsApp preview, or browser, while your real file rides along invisibly, waiting to be pulled back out.
  ____                ___  _   
 / ___|  ___    ___  |_ _|| |__
 \___ \ / _ \  / _ \  | | | ___
  ___) |  __/ |  __/  | | | |__
 |____/ \___   \___  |___| \___

     hide any file inside a photo


```

## ✨ Features

| | |
|---|---|
| 🖼️ **Any file, any size** | Hide docs, zips, videos — even 500MB+ files, streamed so it won't eat your phone's RAM |
| 🧭 **Guided menu** | Run it with no flags and just pick options — nothing to memorize |
| 🔐 **Password protection** | AES-256-GCM encryption, chunked, so it stays fast even on huge files |
| 📦 **Polyglot mode** | Hide a `.zip` and the result opens *directly* in RAR/7-Zip via "Open as archive" — no seeit needed to peek inside |
| ✅ **Integrity checks** | Every extraction is verified — you'll always know if something got corrupted |

## 📋 Requirements

- Python 3
- `cryptography` (only needed if you use password protection)

## 🚀 Install

```bash
git clone https://github.com/talekarvishwa771-cpu/seeit-app.git
cd seeit-app
pip install cryptography
python3 seeit.py
```

## 🕹️ Usage

**Guided menu** — just run it, no arguments needed:

```bash
python3 seeit.py
```

**Or go straight to the command you want:**

| Command | What it does |
|---|---|
| `hide -c cover.jpg -f secret.zip -o out.jpg` | Hide a file inside a photo |
| `hide -c cover.jpg -f secret.zip -o out.jpg -p` | ...with a password |
| `hide -c cover.jpg -f secret.zip -o out.jpg -z` | ...as a polyglot (zip files only) |
| `unhide -i out.jpg -o recovered.zip` | Extract the hidden file |
| `list -i out.jpg` | Quick check — hidden filename & size |
| `info -i out.jpg` | Full diagnostic info |

## ⚡ Heads up

> Apps like **WhatsApp, Instagram, and Messenger** recompress images sent as "photos" — this **destroys** the hidden data.
> Always send the file as a **Document/File**, or use email, cloud storage, or a direct transfer instead.

---

<div align="center">

**Created by void.725**

⭐ If this was useful, consider starring the repo!

</div>
```
