# IO Signature — review

**Film:** 9 s, 1080×1920 (TikTok / Reels), 30 fps, fără sunet. `renders/io-atelier-signature.mp4`

## Ce face
| t (s) | Moment |
| --- | --- |
| 0 – 0.3 | Negru cerneală, cameră ușor apropiată (1.06 → 1.0 până la 4.2 s) |
| 0.3 – 2.6 | O linie fină de lumină aurie desenează conturul monogramei; o scânteie conduce cercul |
| 2.4 – 3.6 | Aprinderea: aurul periat umple conturul pe diagonală, un halou cald, o sclipire de lumină |
| 3.7 – 4.8 | Monograma urcă și face loc semnăturii |
| 4.4 – 5.4 | ATELIER, literă cu literă, din ceață |
| 5.25 – 6.1 | Liniile fine se deschid din centru, apare „by Ioana” |
| 6.7 – 7.4 | O ultimă sclipire pe metal, apoi liniște 1.5 s |

## Decizii
- Pornit de la monograma aurie (I prin O, inelul trece peste I jos) — versiunea cea mai matură din cele trei animații existente.
- Scos tot ce citea „template”: lumina UV violet, bokeh-ul, benzile negre de cinema, pensula ilustrată. Luxul vine din reținere: o singură sursă de lumină, un singur gest.
- Fonturi complete (Figtree, Pinyon Script — ambele licență OFL) în `assets/fonts/`, nu subseturi.
- Totul determinist (praf cu seed fix, fără bucle).

## Măsurat / doar privit
- `check`: 0 erori; 1 avertisment păstrat intenționat (`nested_structure_needs_subcomposition`) — e un singur cadru de 9 s, o sub-compoziție nu aduce nimic.
- Cadrele cheie verificate pe snapshot și pe fișierul randat.
- **Sunet: nu există.** Nu aveam o sursă de muzică/efecte; sunetul vechi (`io-uv-spectacular/assets/sound.wav`) e sincronizat pe alt film.

## Cel mai slab moment
Haloul de la 2.9–3.4 s e puternic; dacă pare prea „strălucitor”, scade opacitatea lui `#halo` de la 1 la 0.7.

## Variabile (editabile în HyperFrames Studio)
`signature`, `ground`, `ground-glow`, `signature-color`.
