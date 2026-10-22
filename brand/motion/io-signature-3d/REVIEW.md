# IO Signature 3D — review

**Film:** 11 s, 1920×1080, 30 fps, fără sunet. `renders/io-atelier-signature-3d.mp4`

## Ce face
| t (s) | Moment |
| --- | --- |
| 0 – 1.7 | I-ul din aur iese din întuneric |
| 0.8 – 4.7 | Inelul O vine orizontal de sus, se înfilează pe I, alunecă în jos rotindu-se în jurul tijei (~2¾ ture, frânate) și se ridică spre vertical cât îi permite spațiul de sub serifă |
| 4.7 – 5.6 | Așezarea: recul amortizat, inelul ajunge în poziția din logo (jos în fața I-ului, sus în spatele lui) |
| 5.9 – 7.1 | Semnul urcă; 6.5 – 8.2 ATELIER și „by Ioana” |
| 8.2 – 11 | Liniște, reflexiile se mișcă lent pe metal |

## Tehnic
- Three.js r169 (vendor/), desenat din timpul cadrului (`hf-seek`), complet determinist.
- Aur: bare cu secțiune super-elipsă (margini rotunjite), PBR metal, mediu de studio cu softbox-uri, umbre reale (inelul își aruncă umbra pe I).
- Motion blur real: 10 sub-cadre pe cadru, obturator 180°. Randarea durează ~21 min.
- Centrul inelului e mereu pe axa tijei, iar unghiul e limitat de serifă, deci inelul nu trece niciodată prin metal.

## Avertismente păstrate
- `dead_stretch` 0–4.75 s: fals — verificarea nu vede mișcarea din canvas-ul 3D.
- `console_warning` (GPU stall ReadPixels): normal pentru randarea software.
- `nested_structure_needs_subcomposition`, `composition_file_too_large`: un singur cadru, intenționat.

Sunetul nu există; nu a fost verificat nimic auditiv.
