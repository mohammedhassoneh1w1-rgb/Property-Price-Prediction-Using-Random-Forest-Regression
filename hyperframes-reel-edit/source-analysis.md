# Source analysis — rawreel.mp4

## Metadata (ffprobe)

| Field | Value |
|---|---|
| Duration | 68.433 s (4106 frames) |
| Video | H.264, yuv420p, **464×832** (≈9:16.15), **60/1 fps** CFR |
| Audio | AAC, 44.1 kHz, 2 ch |
| Size / bitrate | 8.31 MB / 971 kb/s (WhatsApp-compressed) |
| Delivery canvas | 1080×1920 @ 60 fps (native rate kept). The picture is a 2.33× lanczos upscale, so expect softness — this is a source limit. |

## Shot inventory (from 1 fps contact sheet `analysis/contact_1fps.jpg`)

| Source time | Content | Face/subject position (x, y of frame) |
|---|---|---|
| 0.0–5.4 | Presenter standing, **wide**, in front of the new building facade | ≈ (0.50→0.40, 0.50); full body |
| 5.4–6.6 | Shot change (cut inside source) → seated on motorbike | — |
| 6.6–15.6 | Presenter **medium**, seated on a motorbike, street + palms behind, gesturing hands at y≈0.55–0.70 | ≈ (0.50, 0.43) |
| 15.6–17.5 | Building exteriors (silent) | — |
| 17.5–21 | Entrance, chandelier, stair hall | — |
| 21–47 | Living rooms, doors, windows, spiral stairs (marble floors, cove lighting) | — |
| 48–60 | Bathrooms, basement rooms with wood floors, garden yard, glass shower | — |
| 61.0–68.4 | Presenter walking **down a curved white stair**, wide, pointing gesture at the end | head moves (0.64, 0.36) → (0.37, 0.48) |

## Audio / silence analysis (10 ms RMS, `analysis/rms10ms.npy`)

- Speech: **0.00–15.40 s** and **61.76–67.70 s**.
- **15.5–61.6 s is near-silent room tone** (−50 to −65 dBFS, no music) under the walkthrough footage.
- Internal pauses > 220 ms: 5.46–6.69 (1.23 s, also the shot change), 10.18–10.62 (0.44), 11.01–11.40 (0.39), 8.65–9.00 (0.35), 12.86–13.21 (0.35, kept for the joke's timing), 64.44–64.80 (0.36, kept — presenter visible, natural breath).
- Room-tone floor in speech sections ≈ −45 to −50 dBFS. No denoise was needed.

## Retained / removed ranges

See `timing-map.json`. Removed: 5.417–6.550, 10.300–10.500, 11.117–11.300, 15.500–61.617, 68.000–68.433. Total cut 20.367 s (1222 frames).

## Transcript (verified, Jordanian Arabic)

> مشروع جديد بأم أذينة، قريب من الضمان الاجتماعي. موقع مميز ومساحات واسعة. العمارة مكونة من ثمان شقق، الشقتين الأرضيات دوبلكس، بتشطيبات سوبر ديلوكس. وأكيد الدراجة هاي مو للبيع. … وإذا بتدور على فرصة استثنائية ومميزة، نرجع ونحكي لك: ديارة هي خيارك.

Method: HuggingFace was blocked by the session's network policy, so the Whisper large-v3 int8 ONNX export (k2-fsa/sherpa-onnx GitHub release) ran through a hand-written decoder:

- Each pause-delimited chunk and sub-chunk was decoded separately.
- Word boundaries were anchored to measured energy dips and interpolated inside short (≤1.4 s) chunks.
- Ambiguous words were resolved by teacher-forced log-probability comparison:
  - مو للبيع −2.3 vs مش للبيع −7.4
  - ديارة −0.17 vs ديارا −4.0
- The full-file decode hallucinated "ترجمة نانسي قنقر" over the silent section, which confirms there is no speech there.

Expected word-timing accuracy is about ±60–120 ms, adequate for 1–4-word caption groups.

## Semantic beats

1. **Hook / location** — new project in Um Uthaina, near the Social Security Corporation.
2. **Quality claim** — distinctive location, spacious areas.
3. **Building composition** — 8 apartments; the two ground-floor units are duplex.
4. **Finishing** — super-deluxe finishing.
5. **Humour / credibility** — "and of course this motorbike is not for sale".
6. **CTA** — "if you're looking for an exceptional opportunity, we tell you again: Diyara is your choice."
