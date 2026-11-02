# sound-music-for-content

Sound effects and music beds for kishar's 2D motion-design Shorts (the `motion-shorts` skill).
Claude clones this repo at the start of every video and checks it **before** SoundWeaver.

## Folders

| Folder | What goes here |
|---|---|
| `music/` | Music beds, **no vocals**, at least as long as the video (≥ 35 s). Name them by mood: `quirky-*.mp3`, `suspense-*.mp3`, `space-*.mp3`, `emotional-*.mp3`, `pluck-*.mp3` |
| `sfx/` | Real sound effects you downloaded (bark, boing, riser, heartbeat, splash…) |
| `sfx/ui/` | Short UI sounds copied from the SoundWeaver plugin |
| `sfx/placeholder/` | Sounds synthesized in code. Use only until a real file exists in `sfx/` with the same name |

**Rule for Claude:** if `sfx/<name>` exists, use it; otherwise fall back to `sfx/ui/<name>`, then `sfx/placeholder/<name>`, then SoundWeaver. If nothing fits, write a `sound-requests.md` sheet.

## Adding a sound (from phone/tablet)
1. Download a free file (Pixabay, YouTube Audio Library, or freesound **CC0**; no commercial or meme audio).
2. In this repo open `music/` or `sfx/` → **Add file → Upload files** → commit.
3. Add one row to the table below (name, use, volume).

## Sound list

**Prep notes** = what to do before using the file (all SFX get peak-normalized to −1 dBFS first, then the volume below).

### Music (beds: no vocals)
| File | Mood / use | Length | Volume | Prep notes |
|---|---|---|---|---|
| `music/quirky-1.mp3` | fun science, body, animals | 30.0 s | 0.12 (0.20 for a louder bed) | shorter than most videos: loop with `acrossfade=d=2` to video length |
| `music/space-ambient-1.mp3` | space / scale | 33.6 s | 0.12 | loop for videos > 33 s |
| `music/suspense-pulse-1.mp3` | mystery / hidden systems | 34.1 s | 0.14 (it's quieter, −21 LUFS) | loop for videos > 34 s |
| `music/emotional-ambient-1.mp3` | love / history / tender stories | 14.6 s | 0.12 | loop ×3 with crossfades |
| `music/pluck-loop-1.mp3` | light everyday objects | 7.7 s | 0.12 | short loop: repeat with 0.5 s crossfades |
| `music/plunk-sting.mp3` | 2 s sting after a joke / punch line | 2.0 s | 0.3 | use once per video |
| `music/quirky-synth-placeholder.mp3` | fallback bed | 40 s | 0.12 | synthesized; only if nothing else fits |

### Sound effects
| File | Use | Volume | Prep notes |
|---|---|---|---|
| `sfx/whoosh.mp3` | every scene cut, starts 0.28 s before the cut | 0.32 | peak at 0.14 s |
| `sfx/click.mp3` | labels / stickers pop | 0.35 | **the click is at 1.0 s**: trim `atrim=0.98:1.2` + 0.1 s fade |
| `sfx/ding.mp3` | reveal, payoff, CTA | 0.4 | long tail: fade out from 0.9 s to 1.5 s |
| `sfx/clank.mp3` | stamp / block lands | 0.5 | hit at 0.2 s (start it 0.15 s early) |
| `sfx/glitch.mp3` | switch-off, error, "meh" | 0.4 | 1.3 s |
| `sfx/tick.mp3` | number counters (4–5 ticks, 0.3 s apart) | 0.6 | very short and quiet: normalize (+11 dB) |
| `sfx/boing.mp3` | joke / punch line | 0.35 | 1.6 s |
| `sfx/scribble.mp3` | arrows / drawing | 0.5 | **very quiet (−41 LUFS)**: normalize (+27 dB) |
| `sfx/riser.mp3` | build before a big reveal | 0.45 | **peaks at 2.0 s**: start it 2.0 s before the reveal word, cut at 2.15 s with a short fade |
| `sfx/heart.mp3` | emotional / "this is you" moment, 0.3 s before the line | 0.5 | has 4 lub-dubs: use one with `atrim=0.12:0.67`, or keep all for a long beat |
| `sfx/ui/*.wav` | SoundWeaver backups (whoosh, click, ding, clank, glitch, tick, celebrate) | as above | `celebrate.wav` = confetti on the CTA, 0.35 |
| `sfx/placeholder/*.wav` | synthesized stand-ins (boing, riser, heart, scribble, bark) | as above | only when no real file exists |

## Wanted (upload with these names)
| Save as | What | Search |
|---|---|---|
| `sfx/bark.mp3` | one short friendly dog bark, 0.3–0.6 s | https://pixabay.com/sound-effects/search/dog%20bark%20single/ |
| `sfx/whine.mp3` | small dog whine / "huh?", 0.3–0.5 s | https://pixabay.com/sound-effects/search/dog%20whine/ |
| `sfx/pop.mp3` | bubbly pop for stickers (a second click option) | https://pixabay.com/sound-effects/search/pop/ |
| `sfx/stamp.mp3` | rubber-stamp thud | https://pixabay.com/sound-effects/search/stamp/ |
| `music/quirky-2.mp3` | another playful bed, ≥ 45 s, no vocals | YouTube Audio Library → Funny / Happy |

Tip: name files `kind-number.mp3` (no spaces) so they sort and match automatically.
