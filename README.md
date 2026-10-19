# Letterlab — hakstrook

Een digitale structureerstrook. Het woord staat in vakjes, één vakje per
klank. De lesgever vouwt letters weg, leest zoemend mee met de wijzer, laat
het woord in klanken hakken, en wisselt telkens één letter (raam - raak -
rik - tik). Als **Lingo-bord** is het een inleiding op de les: van het
woord van de vorige les, letter per letter, naar het nieuwe kernwoord.

Stappenplan technisch lezen: stap 1 (kernwoord op de structureerstrook),
4 (analyse: wegvouwen en verklanken), 11G (blanco strook: waar hoor je de
klank?) en 12 (hakken en plakken).

## Mogelijkheden in de link

| In de link | Betekenis |
|---|---|
| `woord=raam` | Het woord (verplicht). |
| `woord=raam\|raak\|rik\|tik` | Wisselrijtje: met de pijlen naar het volgende woord. De nieuwe letter kleurt even roze. |
| `woord=b-a-nk` | Zelf de vakjes bepalen met streepjes. Anders: sch, oe, aa, ee, oo, uu, ie, ei, ij, ui, eu, ou, au, ng en ch in één vakje. |
| `woordbeeld=ja` | Het hele woord ook als woordstrook boven de hakstrook. |
| `beeld=raam` | Afbeelding uit `assets/afbeeldingen/` (centrale repository). |
| `weg=3` | Vakje 3 staat bij het begin weggevouwen (meerdere: `weg=1,3`). |
| `leeg=ja` | Blanco strook: de cursist tikt het vakje aan waar hij de klank hoort (kruisje). |
| `klank=nee` | Geen geluidsknoppen: de lesgever spreekt zelf. |
| `tempo=traag` | Zoemtempo: `traag`, `standaard` (zonder iets) of `snel`. |
| `bord=ja` | Lingo-bord: de woorden van het rijtje komen onder elkaar. In elk nieuw woord staat eerst een **?** op de plaats van de letter die verandert. |
| `nieuw=r` | Bij het Lingo-bord: de nieuwe letter van de les krijgt in het laatste woord het label *nieuw*. |

## Bediening

| Knop | Toets | Wat |
|---|---|---|
| tik op een vakje | 1 tot 9 | letter weg- of terugvouwen (blanco strook: kruisje) |
| Zoem | Z | de wijzer schuift aan een vast tempo onder het woord; de lesgever leest zoemend mee (zonder geluid) |
| Hak | H | de klanken één voor één, met een pauze |
| luidspreker | W | het hele woord (met weggevouwen letters: wat overblijft) |
| herstel | R | alle letters terug |
| pijlen | pijl links/rechts, spatie | vorig of volgend woord; op het Lingo-bord eerst het **?**, dan de letter (met haar klank) |
| volledig scherm | F | |

Het zoemtempo (seconden per vakje) staat bovenaan in het script bij
`ZOEM_TEMPI`, de pauze bij hakken bij `HAK_GAP_MS`.

## Lingo-bord als inleiding

Voorbeeld: `hakstrook/?woord=daan|naan|naam|raam&bord=ja&nieuw=r`

1. Het woord van de vorige les staat klaar: *daan*. Lees het samen.
2. Volgende: een nieuwe rij verschijnt met een **?** vooraan. *Welke letter
   moet hier staan? Welk woord maken we?*
3. Volgende (of tik op het vraagteken): de letter verschijnt en klinkt. Lees
   het nieuwe woord zoemend.
4. Zo verder tot het kernwoord, waarin de nieuwe letter het label *nieuw*
   krijgt.

Ook een letter erbij kan: `ik|kik|kim`. De lesreeks-maker stelt zo'n bord
vanzelf voor (van het vorige kernwoord naar het nieuwe, alleen met gekende
letters).

## Geluid

Zoem heeft geen geluid: de lesgever leest zelf. Hak, de luidspreker en het
tonen van een letter op het Lingo-bord gebruiken de opnames. Klanken uit `assets/audio/klanken/` (centrale repository), daarna de
klankmap van het klik-klakboekje. De stilte vooraan en achteraan elke
opname wordt overgeslagen. Het hele woord komt
uit `assets/audio/woorden/<eerste letter>/` of `nonsens/`. Is er geen
opname, dan spreekt de browserstem.

Let op: bij weggevouwen letters (bv. `raa`) is er meestal geen opname van
wat overblijft. Dan klinkt de browserstem. Liefst zegt de lesgever het
zelf.

## Publiceren (eenmalig)

1. Maak bij **ligolimino** een openbare repository `hakstrook`.
2. Kies **uploading an existing file** en sleep de **inhoud** van deze map
   erin (niet de map zelf). Kies **Commit changes**.
3. **Settings → Pages**: branch `main`, map `/ (root)`, **Save**.
4. Na enkele minuten: `https://ligolimino.github.io/hakstrook/`.

Open je die link zonder iets erachter, dan zie je een uitlegpagina met een
formulier om zelf een link te maken.

## Zelfstandig en onderhoudsvrij

- Alleen gewone bestanden: geen installatie, geen bouwstap, geen databank.
- Het lettertype Andika staat in de repository zelf.
- De volledige oefening staat in de link. Een link blijft werken zolang de
  repository online staat.
- In Genially is de achtergrond doorzichtig, zodat de dia zichtbaar blijft.

## Na een wijziging

Telefoons kunnen een oude versie bewaren. Wacht even of herlaad de pagina.

## Licentie lettertype

Andika valt onder de SIL Open Font License, zie
`assets/fonts/OFL-LICENSE.txt`.
