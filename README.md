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

| File | Use | Volume | Source |
|---|---|---|---|
| `music/quirky-synth-placeholder.mp3` | fun science / animals bed, 112 BPM, 40 s, loopable | 0.12 (0.20 when a louder bed is wanted) | synthesized (placeholder; replace with a real track) |
| `sfx/ui/whoosh.wav` | every scene cut, 0.28 s before the cut | 0.32 | SoundWeaver `transition-smooth-whoosh` |
| `sfx/ui/click.wav` | labels / stickers pop | 0.35 | SoundWeaver `pop-bubble` |
| `sfx/ui/ding.wav` | reveal, payoff, CTA | 0.4 | SoundWeaver `notification-ding` |
| `sfx/ui/clank.wav` | stamp / block lands | 0.5 | SoundWeaver `switch-hard-off` |
| `sfx/ui/glitch.wav` | switch-off, error, "meh" | 0.4 | SoundWeaver `error-sharp-alert` |
| `sfx/ui/tick.wav` | number counters (4–5 ticks, 0.3 s apart) | 0.6 | SoundWeaver `tap-ui-tick` |
| `sfx/ui/celebrate.wav` | confetti on the CTA | 0.35 | SoundWeaver `success-celebrate` |
| `sfx/placeholder/boing.wav` | joke / punch line | 0.35 | synthesized |
| `sfx/placeholder/riser.wav` | starts 1.7 s before a big reveal (peak at 1.7 s) | 0.45 | synthesized |
| `sfx/placeholder/heart.wav` | emotional / "this is you" moment, 0.3 s before the line | 0.5 | synthesized |
| `sfx/placeholder/scribble.wav` | arrows / drawing | 0.5 | synthesized |
| `sfx/placeholder/bark.wav` | dog bark (weak placeholder) | 0.35 | synthesized |

## Wanted (upload with these names)
| Save as | What | Search |
|---|---|---|
| `sfx/bark.mp3` | one short friendly dog bark, 0.3–0.6 s | https://pixabay.com/sound-effects/search/dog%20bark%20single/ |
| `sfx/boing.mp3` | cartoon boing | https://pixabay.com/sound-effects/search/cartoon%20boing/ |
| `sfx/riser.mp3` | ~2 s riser | https://pixabay.com/sound-effects/search/riser/ |
| `sfx/heart.mp3` | soft heartbeat | https://pixabay.com/sound-effects/search/heartbeat/ |
| `sfx/whoosh.mp3` | longer cinematic whoosh | https://pixabay.com/sound-effects/search/whoosh/ |
| `music/quirky-1.mp3` | playful ukulele/pizzicato, 105–120 BPM, no vocals | YouTube Audio Library → Funny / Happy |
| `music/suspense-1.mp3` | mysterious pulse, no vocals | https://pixabay.com/music/search/suspense%20pulse/ |
| `music/emotional-1.mp3` | soft piano/pad, no vocals | https://pixabay.com/music/search/emotional%20ambient/ |
| `music/space-1.mp3` | ambient space bed, no vocals | https://pixabay.com/music/search/space%20ambient/ |
