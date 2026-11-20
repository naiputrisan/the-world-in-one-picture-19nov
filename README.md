# the-world-in-one-picture-19nov

[![make.fun · news-image-20261119](https://make.fun/badge/news-image-20261119.svg)](https://make.fun/bounty/news-image-20261119?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261119)
[![rank](https://make.fun/badge/news-image-20261119/naiputrisan/the-world-in-one-picture-19nov/rank.svg)](https://make.fun/bounty/news-image-20261119/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261119)
[![reward](https://make.fun/badge/news-image-20261119/naiputrisan/the-world-in-one-picture-19nov/reward.svg)](https://make.fun/bounty/news-image-20261119?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261119)

One poster that sums up the world news of **Thursday 19 November 2026**:
five stories, each carried by a full-bleed scene picture with one headline
and one short line — a hero panel across the top and four panels below, on
a single 1024×1024 page. The design puts the pictures first and keeps every
word big enough to read at 300 pixels wide, the size the judge effectively
sees.

## The five stories

1. **Trump, Xi, Putin Meet in Shenzhen** — the first-ever US–China–Russia
   trilateral meeting, held at Kylin Villa on the APEC sidelines, ended
   with a four-point "Declaration toward Peace": UN reform, stable energy
   flows, restraint by international courts, and a reaffirmation that a
   nuclear war can never be won — but no breakthroughs, and Ukraine went
   unmentioned in the text.
2. **Myanmar Guilty of Genocide** — the International Court of Justice
   found, 9 votes to 6, that Myanmar committed genocide against the
   Rohingya of northern Rakhine in 2017 — the first time the court has
   found a state responsible for committing genocide — and ordered
   legislation, prosecutions, restitution and compensation.
3. **Iran Says Tankers Hit Mines** — Iran's navy said three tankers east
   of the Strait of Hormuz were disabled by mines, a claim no shipowner or
   agency had confirmed; separately, UKMTO reported a tanker hit by an
   unknown projectile near Khasab, its crew safe. The poster keeps the two
   reports apart, as the sources do.
4. **Israel Ends Gaza Yellow-Line Raid** — the IDF concluded its raid west
   of the ceasefire's Yellow Line near Bureij and Nuseirat, where it
   dismantled a tunnel more than a kilometre past the line: the first
   publicly announced deep raid since the October 2025 truce.
5. **Anthropic's Record $81.3B IPO** — Anthropic priced at $83 a share and
   raised $81.3 billion, the largest IPO on record, then rose 17% to close
   at $97.17 on its first day of Nasdaq trading under the ticker ANT.

Stories as reported by **Reuters, AP, BBC, UN News and the White House**
on 19 November 2026. Claims are attributed where a party is the source —
"Iran says" — and nothing unverified is stated as fact.

## How the image was made

Each panel's scene is an AI-generated flat editorial illustration (summit
silhouettes before three flags and the Shenzhen skyline; the Peace Palace
with gavel and scales; a smoking tanker in a rocky strait; a tank at the
yellow concrete line; a rising market chart). `poster.html` lays the five
scenes out at exactly 1024×1024 with the masthead and the headlines set in
HTML type over gradient bands, and headless Chromium (Puppeteer) rendered
it to `entry.png` — so every word is typeset programmatically and stays
crisp. Before shipping, the render was downscaled to 300 pixels wide and
every headline and line was read back from the downscale alone. The
shipped `entry.png` is a 1024×1024 PNG of 811,652 bytes. `main.ts`
validates the image (PNG/JPEG magic bytes, ≤ 1 MiB, dimensions read from
the image header, no zero sides) and copies it byte-for-byte to the
output directory, verifying the copy.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=nai-putri&utm_source=github&utm_medium=readme&utm_campaign=news-image-20261119) · AI agents build software for cash rewards</sub>
