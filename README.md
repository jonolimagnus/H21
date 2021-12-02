# FORR3CG Haust 2021 - Lokaverkefni (25%)

Áður en lengra er haldið skalt þú stofna nýtt **private** repo á github og bjóða *gestskoli* inn sem collaberator. Farðu svo inn á Innu og skila slóðinni að repo-inu í annaðhvort **Lokaverkefni** skilahólfið.

## Almennar reglur varðandi verkefnið

- Verkefnið er einstaklingsverkefni. Ef tveir eða fleiri nemendur skila sömu lausnunum er gefið 0 (núll) fyrir þær lausnir.
- Ef kóði er tekinn af netinu (eða öðrum álíka stöðum) skal taka það fram, benda á hvaðan hann kemur og skrifa skýringar (e. comment) við hverja línu kóðans, sé það ekki gert verður gefið 0 (núll) fyrir verkefnið. Almennt eru ekki gefin stig fyrir kóða sem tekinn er af netinu en hann getur samt gefið örfá stig ef hann er t.d. til að bæta útlit forritsins.
- Ekki er heimilt að nota tilbúnar lausnir fyrir listann. Notið ekki auto og allir bendar (e. pointer) skulu vera hráir (e. raw).
- Allur kóði skal skrifaður í C++. Skipta á hverjum klasa í cpp og h skrár.
  
### Skýrsla

Halda skal utan um verkefnið á github. Þar á að vera allur kóði ásamt dagbók og skýrslu. Í dagbókinni á að halda utan um hvað er gert og hvenær (ef eitthvað er ekki í dagbókinni þá er það ekki í verkefninu). Skýrslan er svo stutt samantekt á dagbókinni á samt útskýringum á hvernig forritið ykkar vinnur. Þar eiga líka að vera leiðbeiningar fyrir viðmótið sem þið skrifið. Skilið einnig stuttu myndbandi (screen record) þar sem virkni forritsins er sýnd. Sniðmát fyrir skýrslu má finna [hér](skyrsluform.md)

Vanti skýrsluna eða stóran hluta hennar hefur það mjög neikvæð áhrif á einkunnina fyrir verkefnið.

## Íhlutalisti

Þú átt að skrifa forrit sem heldur utan um íhluti. Íhlutirnir sem þarf að halda utan um eru [LED](https://is.wikipedia.org/wiki/Ljóstvistur) perur, [viðnám](https://is.wikipedia.org/wiki/Rafmótstaða) og [þéttar](https://is.wikipedia.org/wiki/Rafþéttir). Fyrir LED perurnar þarf að skrá **lit** (*strengur*), fyrir viðnámin þarf að skrá **ohm**a (Ω) fjölda (*heiltala*) og fyrir þéttana þarf að skrá **rýmd** (*kommutala*) í farödum (F). Fyrir alla íhlutina þarf svo að skrá **númer** (*heiltala*) og **stærð** í mm. (*heiltala*).

Allir íhlutirnir eru svo geymdir í lista.

### Grunnkröfur

Verkefnið er 100 stig. Fullkomin lausn á grunnkröfum gefur 60 - 80 stig eftir því hvaða leið er valin fyrir listann.

- Gerður klasa fyrir hverja gerð íhlutar og svo einn yfirklasi sem heldur utan um gögn sem eru sameiginleg í hinum klösunum.
- Gerðu getters og setters fyrir allar gagnabreytur klasanna.
- Klasarnir þurfa að geta prentað sjálfa sig á snyrtilega á skjáinn.
  - Algeng gildi fyrir rýmd þétta eru í mF eða µF. Í þessu forriti verður rýmdin skráð án margfaldara en þegar rýmdin er skrifuð út á hún að vera með eðlilegum margfaldara. Dæmi: skráð gildi 0.001, ætti að skrifa út 1mF og skráð gildi 0.00001, ætti að skrifa út 10µF.
- Útfærðu þinn eigin listaklasa sem heldur utan um allt sem er í íhlutalistanum, veldu eina ef eftirfarandi aðferðum:
  - Kviklegt fylki (e. dynamic array), gefur engin aukastig ofan á grunnkröfur.
  - Tengdur listi (e. linked list), gefur 10 aukastig ofan á grunnkröfur.
  - Tætitafla (e. hash table, hash map, dictionary), gefur 20 aukastig ofan á grunnkröfur.
    - Hér er nóg að reikna hash gildið út frá númerinu.
- Gerðu notendaviðmót þar sem hægt er að gera eftirfarandi:
  - Það þarf að vera hægt að setja íhlut í listann.
  - Það þarf að vera hægt að sækja íhlut úr listanum.
  - Það þarf að vera hægt að eyða íhlut úr listanum.
  - Það þarf að vera hægt að uppfæra íhluti í listanum, hér er nóg að geta uppfært eina gerð af íhlut.
  - það þarf að vera hægt að prenta á skjá lista með öllum íhlutunum.
  - Hafðu notendaviðmótið sem svipuðu sniði og sýnt var í kennslustund 1. desember (sjá dæmi [hér](https://gist.github.com/gestskoli/b65e4d7d064c50ef09daf263a800c4ab)).

### Dæmi um aukakröfur

- Skráavinnsla, hægt er að skrifa listann í skrár og lesa í listann úr skrá. (15 stig)
  - Hér er þægilegast að hver klasi kunni að skrifa sig í skrá og lista klasinn geti lesið skrárnar.
- Gögnin eru röðuð í listanum. (5 stig)
  - Innifelur að útfæra þarf samanburðarvirkjana.
- Litir í viðmóti, hér má nota tilbúna lausn t.d. [rlutil](https://github.com/tapio/rlutil). (5 stig)
- Annað sem ykkur dettur í hug í samráði við kennara.

## Skil verkefnisins

Skil verkefnisins eru í tvennu lagi:

- Hlutaskil, 30% af lokaeinkunn. Hér á að skila öllum íhluta klösunum þ.e.a.s. klösunum fyrir LED, viðnám, þétti og svo yfirklasanum. Skilist fyrir miðnætti mánudaginn 6. desember (ekki verður hægt að fá framlengdan frest). Einkunn fyrir þennan hluta verður gefin fyrir miðvikudaginn 8. desember. **Ef engu er skilað í þessum hluta eru 30% farin af lokaeinkunn.**
- Lokaskil, 70% af lokaeinkunn. Skilist fyrir klukkan 14:00 sunnudaginn 12. desember. Ekki verður hægt að fá framlengingu á þessum tíma.

## Prófunargögn

Hafið þessi gögn harðkóðuð í forritinu sem þið skilið.

Íhlutur | Nr. | Stærð | Litur/Ω/F
--- | --- | --- | ---
LED | 700 | 5 | Hvítt
LED | 701 | 5 | Gult
LED | 702 | 5 | Grænt
LED | 703 | 3 | Blátt
Viðnám | 704 | 3 | 220
Viðnám | 705 | 1 | 1000
Viðnám | 706 | 3 | 5000
Þéttir | 707 | 2 | 0.000001
Þéttir | 708 | 2 | 0.0025
Þéttir | 709 | 6 | 0.1

### Prófunargögn í svigum

```c++

LED(700, 5, "Hvítt");
LED(701, 5, "Gult");
LED(702, 5, "Grænt");
LED(703, 3, "Blátt");
Vidnam(704, 3, 220);
Vidnam(705, 1, 1000);
Vidnam(706, 3, 5000);
Thettir(707, 2, 0.000001);
Thettir(708, 2, 0.0025);
Thettir(709, 6, 0.1);

```
