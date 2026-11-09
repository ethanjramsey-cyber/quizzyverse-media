# Quizzyverse media licences

All videos in `videos/` were rendered with `/home/box/tiktok-empire/scripts/render.py`
(PIXEL). Backgrounds are procedural (Pillow/numpy). There are **no third-party
watermarks, stock photos, stock video clips, or third-party music/SFX samples**.

## Fonts

Font files live under `/usr/share/fonts/truetype/sand-box/google/`. Licence text
was read from each font’s OpenType `name` table (`nameID` 13 = Licence,
`nameID` 14 = Licence URL) on 2026-11-09.

| Family | Files used | Licence | Licence URL (from font metadata) |
|--------|------------|---------|----------------------------------|
| Orbitron | `Orbitron/Orbitron-VariableFont_wght.ttf` | SIL Open Font License 1.1 | http://scripts.sil.org/OFL |
| Montserrat | `Montserrat/Montserrat-VariableFont_wght.ttf` | SIL Open Font License 1.1 | https://openfontlicense.org |
| Poppins | `Poppins/Poppins-ExtraBold.ttf`, `Poppins/Poppins-Bold.ttf` | SIL Open Font License 1.1 | https://scripts.sil.org/OFL |
| Press Start 2P | `Press Start 2P/PressStart2P-Regular.ttf` | SIL Open Font License 1.1 | http://scripts.sil.org/OFL |
| Bungee | `Bungee/Bungee-Regular.ttf` | SIL Open Font License 1.1 | https://openfontlicense.org |
| Inter | `Inter/Inter-VariableFont_opsz,wght.ttf` (AI-disclosure label) | SIL Open Font License 1.1 | https://openfontlicense.org |

SIL OFL 1.1 allows commercial use, redistribution, and modification (with the
usual Reserved Font Name conditions). No separate `OFL.txt` was bundled next to
these sand-box font files; the licence statement above comes from the fonts’
own name tables.

## Audio / music

All music beds and SFX (pad, arpeggio, ticks, ding, whoosh) are **synthesised
in-house** by `synth_audio()` in `/home/box/tiktok-empire/scripts/render.py`
using numpy (no third-party samples or loops).

## Per-video assets

| Filename | Template | Fonts | Audio source | Licence notes |
|----------|----------|-------|--------------|---------------|
| `W1D1-1_neon_space.mp4` | neon_space | Orbitron, Montserrat, Inter | `scripts/render.py` `synth_audio` | OFL 1.1 fonts; original synthesised audio |
| `W1D1-2_clean_classroom.mp4` | clean_classroom | Poppins ExtraBold/Bold, Inter | `scripts/render.py` `synth_audio` | OFL 1.1 fonts; original synthesised audio |
| `W1D1-3_retro_arcade.mp4` | retro_arcade | Press Start 2P, Bungee, Inter | `scripts/render.py` `synth_audio` | OFL 1.1 fonts; original synthesised audio |
| `W1D2-1_clean_classroom.mp4` | clean_classroom | Poppins ExtraBold/Bold, Inter | `scripts/render.py` `synth_audio` | OFL 1.1 fonts; original synthesised audio |
| `W1D2-2_retro_arcade.mp4` | retro_arcade | Press Start 2P, Bungee, Inter | `scripts/render.py` `synth_audio` | OFL 1.1 fonts; original synthesised audio |
| `W1D2-3_neon_space.mp4` | neon_space | Orbitron, Montserrat, Inter | `scripts/render.py` `synth_audio` | OFL 1.1 fonts; original synthesised audio |
| `W1D3-1_retro_arcade.mp4` | retro_arcade | Press Start 2P, Bungee, Inter | `scripts/render.py` `synth_audio` | OFL 1.1 fonts; original synthesised audio |
| `W1D3-2_neon_space.mp4` | neon_space | Orbitron, Montserrat, Inter | `scripts/render.py` `synth_audio` | OFL 1.1 fonts; original synthesised audio |
| `W1D3-3_clean_classroom.mp4` | clean_classroom | Poppins ExtraBold/Bold, Inter | `scripts/render.py` `synth_audio` | OFL 1.1 fonts; original synthesised audio |

Provenance for each file: identical byte-size copies of the Week 1 day 1–3
renders in `/home/box/tiktok-empire/output/`, committed in media-repo commit
`9724505` (“Week 1 days 1-3 videos”), produced by `scripts/render.py`.

## Related (not in this repo)

The separate reusable quiz template under `/home/box/tiktok-empire/templates/`
uses Montserrat Alternates (SIL OFL 1.1; same google sand-box tree) with DejaVu
Sans Bold as fallback (Bitstream Vera-derived free licence; see
`/usr/share/doc/fonts-dejavu-core/copyright`), and synthesises audio in
`templates/audio_gen.py`. Those assets are not shipped in `videos/` today.
