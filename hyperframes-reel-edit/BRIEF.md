---
workflow: general-video
flow: automation
storyboard: no
message: "New project in Um Uthaina: 8 apartments, duplex ground floors, super-deluxe finishing — Diyara is your choice"
destination: instagram-reels
aspect: 1080x1920
language: ar
length: 20s
angle: footage-remix
---

## Intent

Premium Arabic 9:16 reel edited from one raw real-estate clip (`rawreel.mp4`).
It alternates between two worlds: a restrained presenter A-roll with motivated
crop states and small word-timed captions, and full-screen warm-paper editorial
interludes. Each interlude has one monochrome symbolic object, oversized Arabic
kinetic type, a progressive build and hard cuts. Personal, unbranded visual
treatment: no logo, watermark or invented identity.

## Assets

- rawreel.mp4 — the only source (464×832, 60 fps, 68.43 s). Presenter on camera
  at 0–15.6 s and 61.6–68.4 s; silent property walkthrough at 15.6–61.6 s. It is
  never modified.
- assets/rawreel_1080.mp4 — derived lanczos upscale/cover-crop to 1080×1920 at
  60 fps (picture only; same timebase as rawreel).
- assets/dialogue.wav — derived dialogue: rawreel audio, 70 Hz high-pass, −2.2 dB,
  peak limiter. The edited programme measures −14.0 LUFS / −2.4 dBTP.
- assets/fonts/cairo-*.woff2 — Cairo (OFL-1.1) from @fontsource/cairo 5.3.0. No
  Arabic display font was pre-installed (only DejaVu Sans / FreeSerif), so it was
  vendored locally. There are no render-time fetches.
- assets/vendor/gsap.min.js — GSAP 3.14.2 vendored locally (no CDN at render).

## Customizations

- Silence removal plus hard cuts. The 46 s silent walkthrough is removed from the
  timeline, but its real footage is reused (monochrome) inside the editorial
  scenes as truthful evidence of the property.
- Opening push-in 1.00→1.12 with the first caption arriving during the push.
- Warm paper palette: paper #E9E0D3, ink #1B1D1E, burnt orange #E66A21, teal
  #2A8791, rare gold #D8A44A.
- Voice only: no music bed and no SFX.

## Notes

- The source is a property-tour reel, not a pure talking head; the edit adapts
  the requested style to that reality.
- The map in scene 1 is schematic (no real streets). Only the spoken landmark
  name is shown.
- "ديارة" is spoken in the CTA and appears to be a proper name; its spelling is
  unverified.
