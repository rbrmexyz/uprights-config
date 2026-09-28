# Uprights settings

The Uprights app reads `config.json` from https://rbrmexyz.github.io/uprights-config/config.json
every time it opens. Edit it here on GitHub and players get the change on their next launch —
no new build needed. Leave a number out and the app uses its built-in default.

## Tuning

| Setting | What it does | Now |
|---|---|---|
| `windPush` | How hard each mph shoves the ball | 0.32 |
| `windGripUp` | Share of the wind felt while the ball rises | 0.45 |
| `windGripDownMax` | Share felt at full speed coming down | 2.0 |
| `windMaxStart` | Strongest wind (mph) on the first kick | 12 |
| `windMaxAdd` | Extra mph once difficulty tops out | 24 |
| `windMinFraction` | Every kick gets at least this share of the max (0–1) | 0.5 |
| `rampMakes` | Makes in a row until difficulty tops out | 10 |
| `yardLineMaxStart` | Furthest spot early on (yard line; add 17 for the attempt) | 12 |
| `yardLineMaxAdd` | Extra yards of range at full difficulty | 26 |
| `sweetSpot` | Clean-contact zone as a share of the ball's width (0–0.9) | 0.14 |
| `aimSensitivity` | How much the swipe angle turns the kick | 0.5 |
| `idealMargin` | Ideal flick = just clears the bar × this | 1.1 |
| `overcookShank` | How much an overswing knocks the strike off-centre | 1.6 |
| `overcookSpray` | Extra aim spray from an overswing | 0.1 |
| `flickBase` | Launch speed (m/s) of the gentlest flick | 8 |
| `flickGain` | How much faster the ball goes per unit of flick speed — raise it if long kicks feel out of reach | 7 |
| `maxSpeed` | Hardest possible kick (m/s); 31 reaches ~75 yards in still air | 31 |

## Sponsors

Put artwork in `sponsors/` and list it by full URL, e.g.
`https://rbrmexyz.github.io/uprights-config/sponsors/pizza.png`.

| Slot | Size | Notes |
|---|---|---|
| `wall` | 256×44, up to 4 | Field wall boards, repeated around the stadium |
| `ribbon` | 1024×48 | LED ribbon between the tiers; scrolls |
| `board` | 1068×64 | Strip along the bottom of the video board |
| `pad` | 512×128 logo, or 1024×920 full wrap | Goal post pad, fully wrapped. A wide logo runs up the pad on its own background colour; a near-square image is used as the whole wrap |
| `net` | 1024×410, transparent PNG | Printed on the kicking net behind the posts — seen on every kick |
| `ball` | 512×128, transparent PNG | Printed along one panel of the ball, beside the laces |
| `tee` | 512×128 | Wraps the kicking tee in the logo's background colour |

Any slot you leave out shows plain stadium (dark boards, bare net, plain ball). Nothing fills in with house ads.

```json
"sponsors": {
  "wall": ["https://rbrmexyz.github.io/uprights-config/sponsors/pizza.png"],
  "board": "https://rbrmexyz.github.io/uprights-config/sponsors/pizza-strip.png"
}
```

Changes take up to ~10 minutes to reach GitHub Pages. JSON is picky: check commas and quotes,
because a broken file is ignored and the app keeps its last good settings.
