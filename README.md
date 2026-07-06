# Car-Racing-Game - Pukekohe GP

A single-file, mobile-first web adaptation of the card-driven racing board game, themed
around the purple No. 17 car and a fan-made Pukekohe circuit (73 spaces, 4 corners).
Built for personal play — please keep the repo **private**; the tabletop game it adapts
is a commercial design and this project uses original visuals only.

## Play it

Open `index.html` in any modern browser — no build, no dependencies, works offline.
On your phone, add it to the home screen for a full-screen app feel.

## How a round works

You drive the purple **No. 17** against 1–8 AI rivals (Legends-style logic).

1. **Shift gears** — one step free; jumping two costs 1 Heat.
2. **Play cards** — exactly your gear number. Heat can't be played; a hand
   clogged with Heat is *cluttered*: you coast, dump what you can, drop to 1st.
3. **Reveal & move** — Stress (＋) flips your deck for a random speed.
4. **Adrenaline** — last car gets +1 speed and +1 cooldown.
5. **React** — Cooldown (gear 1: ×3, gear 2: ×1) returns Heat to the engine;
   **Boost** pays 1 Heat for a bonus flip that counts toward corner checks.
6. **Slipstream** — in another car's tow, take 2 free spaces (never across the
   final finish line).
7. **Check corners** — exceed a limit and the engine pays the difference in
   Heat; can't pay and you **spin out** (lose engine Heat, gain Stress, 1st gear).
8. **Discard** (optional) and **replenish** to 7 cards.

First across the line after the set laps wins. Manage the engine — there's no
prize for finishing in a pristine car, but a cooked one never finishes at all.

## Tweak it

Everything lives in one file. Near the top of the `<script>`:

- `TRACK` — spaces, corner positions/limits, Heat/Stress counts, legends line.
- `LEGEND_CARDS` — the AI pace deck (top speed + diamond value).
- `BOT_POOL` — rival names and colours.
