# amtgard-rop-skill

A tool that converts the **Amtgard Rules of Play (v8.7)** into an
LLM-friendly structure — one file per ability and class, the reference
sections, applied rules clarifications, and a deterministic magic-user
point-buy validator — so an AI assistant can look things up and help
adjudicate rulings with the exact rule in front of it.

It's a **format and access aid, not a republication**: it takes the
existing rules and reorganizes them for machine retrieval. The official
Rules of Play is always the authority — where this tool and the current
official rulebook ever disagree, the official rulebook governs.

*Unofficial; Not affiliated with or
endorsed by Amtgard International. All rulebook content © Amtgard
International — see [Copyright & Trademark](#copyright--trademark).*

---

## What it does

- **Ability lookup** — one file per ability (180 standard + 16 quest),
  each with Type, School, Range, Incantation, Materials, Effect,
  Limitations, Notes, and which classes grant it. Search by name or by
  effect ("the one that moves people back") via an indexed synopsis list.
- **Class & character building** — one file per class (12 playable +
  Monster + Peasant), with garb/armor/shield/weapon profiles and abilities
  by level. Magic-user files carry the full purchase table (Cost, Max,
  Frequency).
- **Rules adjudication** — combat rules, armor, weapons/equipment, plus a
  magic-mechanics reference (Ability Order, Charge, Enchantments) and a
  States & Special Effects dictionary, so interaction rulings resolve by
  defined terms instead of guesswork.
- **Magic-user point-buy validator** — a deterministic script that checks
  whether a magic-user list is legal under the level-banded point rules
  (5 points per level, rolling down only) and reports the binding
  constraint. No more hand-math errors.
- **Applied clarifications** — the current official clarifications/errata
  are attached as "Known Clarifications" sections on the affected files,
  and they override the printed text where they conflict.

The assistant loads only what each question needs — the foundation is
small and the rest is pulled on demand.

---

## Install — Claude (claude.ai)

1. **Download** `amtgard-rop-assistant.skill` from this repo.
2. In **claude.ai**, open your profile menu → **Settings → Customize →
   Skills** (on some plans this is **Settings → Capabilities → Skills**).
3. Make sure **Code execution and file creation** is turned on — skills
   won't run without it.
4. Click **“+” → Upload skill** and select the `.skill` file. (It's a ZIP
   archive; if the picker only accepts `.zip`, rename the extension.)
5. Toggle the skill **on**. Start a new chat and ask an Amtgard rules
   question — Claude loads it automatically when relevant.

Available on Free, Pro, and Max (upload it yourself under Customize →
Skills). On Team/Enterprise an org owner must enable Skills first. Custom
skills you upload are private to your account.

## Install — OpenAI (ChatGPT)

> **⚠️ Install from a web browser, not the mobile app.** ChatGPT's skill
> upload screen only exists in the **web** interface. The phone app has no
> "upload skill" option — but once you've installed it in the browser, the
> skill **works in the mobile app** just fine. This trips people up; do
> the install on desktop/web first.

1. **Download** `amtgard-rop-skill.skill` from this repo.
2. In **ChatGPT on the web**, click your **profile icon → Skills**.
3. Choose **New skill → Upload from your computer** and select the
   `.skill` file (rename to `.zip` if the picker requires it).
4. ChatGPT scans the upload; once it's available, **enable** it.
5. Now use it anywhere, including the **ChatGPT mobile app**.

Skills on ChatGPT are currently a beta on **Business, Enterprise, Edu, and
Teachers** plans (and are supported in Codex and the API). If you don't see
a **Skills** entry under your profile, your plan/workspace doesn't have the
feature enabled yet.

> Skills follow the open [Agent Skills](https://agentskills.io) standard,
> which is why the same `.skill` works across compatible assistants.

---

## Usage

Once installed, just ask naturally — the assistant detects the topic and
loads the skill. Examples:

- "What does Flame Blade do, and what's the incantation?"
- "Build me a 6th-level Wizard for sword-and-board with as many Shoves as possible."
- "Does Poison get through armor? What about against an Invulnerable player?"
- "What's the skill that moves people back?"
- "How does Ability Order resolve Brutal Strike hitting a Frozen player?"

For magic-user costing questions, the assistant runs the bundled validator
rather than doing the arithmetic by hand.

---

## Copyright & Trademark

**All rulebook content belongs to Amtgard International. This project
claims no rights over it.**

Every rule, ability, class entry, incantation, clarification, and any other
text drawn from the Amtgard Rules of Play, the Dor Un Avathar, or related
Amtgard publications is **© Amtgard International, all rights reserved.** It
is reorganized here for the convenience of Amtgard players and is **not**
licensed, relicensed, sold, or placed in the public domain by this project.
No ownership of any rulebook content is claimed.

**"Amtgard," "Amtgard Rules of Play," and "Dor Un Avathar" are trademarks
of Amtgard International,** used here only descriptively to identify the
game this tool supports.

This project is **unofficial** and is **not affiliated with, sponsored by,
or endorsed by Amtgard International** or any of its kingdoms. It is a free,
non-commercial, fan-made play aid. The official rulebook is always the
authority; where this tool and the current official Rules of Play ever
disagree, **the official rulebook governs.**

If you represent Amtgard International and would like any content changed or
removed, please open an issue or contact the maintainer and it will be
handled promptly.

---

## License

The **original code and tooling** in this repository — the build pipeline,
the magic-user point-buy validator, and the skill scaffolding — are
released under the **MIT License** (see [`LICENSE`](LICENSE)). The MIT
license applies **only** to that original work, and **not** to any Amtgard
rulebook content, which remains © Amtgard International as described above.
