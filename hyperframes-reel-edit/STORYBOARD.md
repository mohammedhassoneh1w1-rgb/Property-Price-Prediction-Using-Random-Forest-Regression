---
format: 1080x1920
fps: 60
duration: 20.367s (1222 frames)
mode: autonomous
message: "مشروع جديد بأم أذينة — ثمان شقق، الأرضيات دوبلكس، تشطيبات سوبر ديلوكس"
arc: hook-location → claim → structure → finish → humour → CTA
---

# Storyboard — Um Uthaina reel

All times are **output** times (final reel); the source times in brackets come from `timing-map.json`.
World A = presenter A-roll (`assets/rawreel_1080.mp4`, muted; sound from `assets/dialogue.wav` cut to identical ranges).
World B = full-screen warm-paper editorial scenes (sub-compositions).
Graphic share: 629 / 1222 frames = **51.5 %**.

| # | World | Out window | Frames | Drives it |
|---|---|---|---|---|
| A0 | presenter wide | 0.000–0.700 | 0–42 | «مشروع جديد» |
| 1 | B · Location | 0.700–3.183 | 42–191 | «بأم أذينة قريب من الضمان الاجتماعي» |
| A1 | presenter wide @1.08 | 3.183–4.200 | 191–252 | «موقع مميز» |
| 2 | B · Space → Building | 4.200–7.700 | 252–462 | «ومساحات واسعة · العمارة مكونة من ثمان شقق» |
| A2 | presenter seated @1.00 | 7.700–9.167 | 462–550 | «الشقتين الأرضيات» |
| 3 | B · Duplex + Finish | 9.167–11.600 | 550–696 | «دوبلكس بتشطيبات سوبر ديلوكس» |
| A3 | presenter seated @1.08 → 1.16 | 11.600–13.983 | 696–839 | «وأكيد الدراجة هاي مو للبيع» |
| A4 | presenter on stairs @1.00 → 1.08 → 1.14 | 13.983–18.300 | 839–1098 | «وإذا بتدور على فرصة استثنائية ومميزة · نرجع ونحكي لك» |
| 4 | B · CTA card | 18.300–20.367 | 1098–1222 | «ديارة هي خيارك» (+18-frame hold) |

## Frame 0 — Hook on the presenter (A0)

- scene: Wide presenter in front of the new building; fast push-in 1.00→1.12 (0.66 s, expo.out), no bounce
- duration: 0.7s
- transition_in: cut
- status: animated
- voiceover: "مشروع جديد"
- src: index.html#a-r1-open

The caption «مشروع» lands at frame 0 and «جديد» at 0.39 s (the prior word dims to 55 %). The push uses the crop wrapper, with its origin on the face (50 % / 48 %). The hard cut to scene 1 lands exactly on «بأم».

## Frame 1 — Location

- scene: Oversized «أم أذينة»; a schematic street grid draws in, an orange pin drops, and a teal landmark marker «الضمان الاجتماعي» joins it with a dashed «قريب» link
- duration: 2.483s
- transition_in: cut
- status: animated
- voiceover: "بأم أذينة قريب من الضمان الاجتماعي"
- src: compositions/s1-location.html
- rules: svg-path-draw, waterfall-entry (masked word rise), spring-pop-entrance (pin, low overshoot)
- object: schematic map + pin (monochrome ink; orange pin). It is abstract, so no real streets are claimed.

Local beats:
- 0.00 the keyword rises (0.18 s).
- 0.05–0.50 the streets draw.
- 0.22 the pin drops.
- 0.88 «قريب من» appears.
- 1.38 the landmark marker, label and dashed connector draw.
- 1.75–2.48 readable hold, then a hard cut.

## Frame A1 — Credibility return

- scene: Same wide shot, hard crop state 1.08
- duration: 1.017s
- voiceover: "موقع مميز"
- status: animated
- src: index.html#a-r1-claim

Caption «موقع» then «مميز» (warm accent).

## Frame 2 — Space → Building (longest scene)

- scene: The real living-room footage (monochrome) sits in a paper frame while dimension arrows extend to its edges («واسعة»). The frame then shrinks into one unit of an 8-unit building elevation; the other 7 units assemble one by one, and «ثمان شقق» takes over
- duration: 3.5s
- transition_in: cut
- status: animated
- voiceover: "ومساحات واسعة · العمارة مكونة من ثمان شقق"
- src: compositions/s2-building.html
- rules: card-morph-anchor (shared-element handoff via uniform scale), svg-path-draw (dimension line, building outline), waterfall-entry (units stagger ≤ 0.4 s)
- footage: rawreel src 23.75–27.25 (wide living room, doors, marble), mono-clean treatment

Local beats:
- 0.03 «مساحات» appears.
- 0.74 «واسعة» rises in orange; the dimension line draws outward.
- 1.357 the card morphs into a cell and «العمارة مكونة من» appears.
- 1.97–2.70 the units assemble.
- 2.817 «ثمان» appears, then «شقق» at 3.117.
- The scene holds to 3.5.
- The source shot change (standing → seated) is hidden under this scene.

## Frame A2 — Seated presenter

- scene: First reveal of the seated medium shot, base crop 1.00
- duration: 1.467s
- voiceover: "الشقتين الأرضيات"
- status: animated
- src: index.html#a-r2

Caption «الشقتين» then «الأرضيات» (cool accent).

## Frame 3 — Duplex + Super-deluxe finishing

- scene: The section drawing of a two-level unit draws in, and an orange stair zig-zag links the levels («دوبلكس»). A real finish card (chandelier/marble hall, monochrome) slides in for «بتشطيبات», then an orange «سوبر ديلوكس» seal stamps onto it
- duration: 2.433s
- transition_in: cut
- status: animated
- voiceover: "دوبلكس بتشطيبات سوبر ديلوكس"
- src: compositions/s3-duplex.html
- rules: svg-path-draw (section + stair), waterfall-entry (keyword), press-release-spring (stamp settle, short)
- footage: rawreel src 18.78–20.45 (chandelier + marble stair hall), mono-clean treatment

Local beats:
- 0.12 «دوبلكس» rises; the section draws 0.12–0.62.
- 0.717 «بتشطيبات» appears and the finish card slides in.
- 1.767 the stamp «سوبر ديلوكس» lands and «دوبلكس» settles to ink.
- 2.18–2.43 hold.
- Two micro-silence trims (0.20 s, 0.18 s) are hidden under this scene.

## Frame A3 — Humour beat

- scene: Seated shot at 1.08; hard punch to 1.16 on «مو» for the joke
- duration: 2.383s
- voiceover: "وأكيد الدراجة هاي مو للبيع"
- status: animated
- src: index.html#a-r2c

Caption groups: «وأكيد» · «الدراجة هاي» · «مو للبيع» («مو» in warm accent).

## Frame A4 — CTA setup on the presenter

- scene: Presenter walking down the curved white stair. Base 1.00, hard punch 1.08 on «استثنائية», hard punch 1.14 on «نرجع»
- duration: 4.317s
- voiceover: "وإذا بتدور على فرصة استثنائية ومميزة · نرجع ونحكي لك"
- status: animated
- src: index.html#a-r3

The presenter stays visible through the whole CTA setup. Caption groups: «وإذا بتدور» · «على فرصة» · «استثنائية ومميزة» (warm on «استثنائية») · «نرجع ونحكي لك».

## Frame 4 — CTA card

- scene: A house outline draws in and «ديارة» appears; «هي» follows; «خيارك» lands oversized in orange while a check mark draws inside the house. The completed card holds 18 frames
- duration: 2.067s
- transition_in: cut
- status: animated
- voiceover: "ديارة هي خيارك"
- src: compositions/s4-cta.html
- rules: svg-path-draw, waterfall-entry

The card does not end on black and does not reset. It carries no invented instruction line; the only supporting line is the spoken «فرصة استثنائية ومميزة».
