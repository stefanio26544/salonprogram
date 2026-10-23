# IO Signature 3D — review

**Film:** 14 s, 1920×1080, 30 fps, fără sunet. `renders/io-atelier-signature-3d.mp4`

## Ce face
| t (s) | Moment |
| --- | --- |
| 0 – 1.7 | I-ul din aur iese din întuneric, pe o suprafață neagră lucioasă |
| 1.0 – 2.05 | O-ul e lăsat orizontal, înfilat pe I, și cade cu gravitație constantă |
| 2.05 – 2.8 | Lovește suprafața, două sărituri (restituție 0.28) |
| 2.8 – 3.7 | Oscilează pe margine ca o monedă care se liniștește (precesie accelerată) |
| 3.7 – 7.9 | Urcă pe I într-o spirală lentă de 1½ ture, din orizontal în vertical; camera devine frontală |
| 7.9 – 8.5 | Legănare fină, amortizată, în poziția din logo |
| 8.4 – 11 | Reflexia se stinge, semnul urcă, apar ATELIER și „by Ioana” |
| 11 – 14 | Liniște |

## Tehnic
- Three.js r169 (vendor/), desenat din timpul cadrului (`hf-seek`), complet determinist.
- Aur: bare cu secțiune super-elipsă (margini rotunjite), PBR metal, mediu de studio cu softbox-uri, umbre reale (inelul își aruncă umbra pe I).
- Motion blur real: 8 sub-cadre pe cadru, obturator 180°. Randarea durează ~33 min.
- Centrul inelului e mereu pe axa tijei; unghiul e limitat de suprafață și de serifa de sus, deci inelul nu trece niciodată prin metal.
- Suprafața: reflexie oglindită care se stinge cu distanța + umbră de contact (ShadowMaterial).

## Avertismente păstrate
- `dead_stretch` 0–4.75 s: fals — verificarea nu vede mișcarea din canvas-ul 3D.
- `console_warning` (GPU stall ReadPixels): normal pentru randarea software.
- `nested_structure_needs_subcomposition`, `composition_file_too_large`: un singur cadru, intenționat.

Sunetul nu există; nu a fost verificat nimic auditiv.
