# Brand conformance

**DOC NO. RL-310-A · REV. A**

This project follows the [Riposte Laboratories design system](https://github.com/armeehn/riposte-brand)
— published at [ripostelabs.xyz/brand](https://ripostelabs.xyz/brand/).

---

## Conforms

| Surface | Status |
|---|---|
| README | Sentence-case headings, tables over prose, concrete claims with real units |
| Voice | Plainspoken. "Everything runs in the browser — images never leave the machine they were opened on" is the register exactly |
| Output artefact | Cut sheets are dimensioned print documents — the brand's native form |

## Deliberately diverges

Nothing yet. The divergences below are **debt**, not decisions.

| Divergence | Detail |
|---|---|
| `public/css/style.css` uses a generic dark-app palette | `#16181c` background, `#4a8ae8` blue accent, `#414753` / `#3a3f48` chrome. None of these are brand colours. |
| Sans-serif UI type | No JetBrains Mono anywhere in the app shell |
| Rounded corners and soft shadows | Both are forbidden by the guide. Radius is 0 and depth is a hard `4px 4px 0` offset |

## Queued

- [ ] **Restyle `public/css/style.css` onto `riposte-brand.css`.** This is the highest-value
      brand work in the repo — Cutsheet is a *print layout tool*, so a design system built
      around dimensioned engineering documents is a natural fit rather than a costume.
      The mapping is direct:
      - Toolbar and panels → `.spec` cards with `bone-dim` headers
      - Sheet preview → bone field with 2px ink rules
      - Bleed / margin / cut-line indicators → the accent rotation, pink → marigold → teal
      - Primary action → `.cta` with the hard-offset hover
      - Blue `#4a8ae8` → the working accent, `--accent`
- [ ] **Check cut-line contrast against the artwork**, not just against the UI. Cut lines are
      guides over user images; they need to read on both light and dark artwork. This is the
      one place a bright accent at 2.27:1 is genuinely fine — it is a hairline over a photo,
      not text — but it should be a deliberate call, not an accident.
- [ ] Add `footer.colophon` to `public/index.html`.
- [ ] `docs/` screenshots regenerated after the restyle.

**Do the restyle as its own PR.** The app is working and tested; a stylesheet swap should be
reviewable on its own and screenshot-diffed against `tests/browser-render.html`.

## Quick reference

```
ink      #1d1a17      pink     #f0477d   (bone text; display only, 3.16:1)
bone     #f6f1e7      marigold #fe9a0d   (INK text; 8.12:1, safe for prose)
bone-dim #eae4d6      teal     #12b795   (bone text; fills only, 2.27:1)

deep, for accent fills that carry a sentence:
pink-deep #d81150   marigold-deep #a15e01   teal-deep #0c7a63

font     JetBrains Mono 400 / 700 / 800
spacing  4 8 12 16 24 34 48 64 72     radius 0     rules 2px solid / 1px dashed
print    rules never below 1.5pt; 15mm margins; 3mm bleed
```

Full guide: <https://github.com/armeehn/riposte-brand> ·
Print rules: [`docs/08-print.md`](https://github.com/armeehn/riposte-brand/blob/main/docs/08-print.md)

---

<table>
<tr>
<td><b>DOC NO. RL-310-A</b><br>REV. A · EST. 2026</td>
<td align="right"><b>PARRY ♻ RIPOSTE ♻ RECYCLE ♻ REPEAT</b><br>Riposte Laboratories Inc.</td>
</tr>
</table>
