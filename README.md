# amtgard-rop-skill

A tool that converts the **Amtgard Rules of Play (v8.7)** into an
LLM-friendly structure — one file per ability and class, the reference
sections, applied clarifications, and a deterministic magic-user point-buy
validator — so a language model can look things up and help adjudicate
rulings accurately, with the exact rule in front of it.

It is a **format and access aid**, not a republication: it takes the
existing rules and reorganizes them for machine retrieval. The official
Rules of Play remains the authority — where this tool and the current
official rulebook ever disagree, **the official rulebook governs.**

Built by a member of the **Celestial Kingdom** as a free, non-commercial
play aid for the Amtgard community.

---

## ⚖️ Copyright & Trademark Notice

**All rulebook content belongs to Amtgard International. This project
claims no rights over it.**

Every rule, ability, class entry, incantation, clarification, and any
other text drawn from the Amtgard Rules of Play, the Dor Un Avathar, or
related Amtgard publications is **© Amtgard International, all rights
reserved.** It is reorganized here for the convenience of Amtgard players
and is **not** licensed, relicensed, sold, or placed in the public domain
by this project. No ownership of any rulebook content is claimed.

**"Amtgard," "Amtgard Rules of Play," and "Dor Un Avathar" are trademarks
of Amtgard International,** used here only descriptively to identify the
game this tool supports.

This project is **unofficial** and is **not affiliated with, sponsored by,
or endorsed by Amtgard International** or any kingdom. It is a free,
non-commercial fan project.

If you represent Amtgard International and want anything changed or
removed, open an issue or contact the maintainer and it will be handled
promptly.

---

## License

The **original code and tooling** in this repository — the build pipeline,
the point-buy validator, and the skill scaffolding — are MIT-licensed (see
`LICENSE`). This applies **only** to that original work, **not** to any
Amtgard rulebook content, which remains © Amtgard International as
described above.
