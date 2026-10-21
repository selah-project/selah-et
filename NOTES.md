# MÄRKMED — projekti Selah eestikeelne tõlge (selah-et)

See fail hoiab **salme, mida on puudutanud käsi või otsus** — et lugeja näeks, kas salmi tegi masin, käsi
või otsus, ja miks. See hoiab ka küsimusi, mis ootavad veel eesti keelt kõneleva inimese kõrva.
*(Kirjetes on nimetatud heebrea vorm, seepärast jäävad mõned sõnad heebrea keelde.)*

---

## §1 · Käsitsi parandatud salmid

- **Nimi** — käsitsi · 2026-10-21: *JaHve* (Jr 49:34), *Jaahve* (2Aj 4:16), *Jahe* (3Ms 1:11) → **Jahve**.
- **Nimetüved** — ühtlustatud · 2026-10-21: *Binyamin* → **Binjamin**, *Babylon* → **Babülon**, *Elyon* →
  **Eljon**, *Tsiyon* → **Tsijon**, *Jabēš* → **Jabeš** (eesti keeles ei ole tähte *y* ega läti tähti).
- **Kirillitsa ja kreeka tähed** 7 sõnas — käsitsi · 2026-10-21 (2Sm 14:32 *Gešur*, 1Ms 27:40 *ike*,
  1Sm 25:25, 3Ms 17:5 *tapavad*, Jos 8:4, Jos 14:7 *Barnea*, Jos 18:21 *Binjamin*).
- **Heebrea ja katkised sulud voolus** — käsitsi · 2026-10-21: 1Ms 19:23, Jr 51:24, Ps 120:6, Ii 9:30,
  2Aj 4:11, 4Ms 4:14, Esr 4:17.
- **Õpetussõnad 11:31** — käsitsi · 2026-10-21: *syndaja* → **patustaja**; `הן` → **vaata** (mitte *enne*).
- **Jeremija 2:6** — käsitsi · 2026-10-21: *skinny-maal* → **stepimaal**. **Esra 9:8**: **elu ülalpidamist**.
- **Laegas ja laev — 44 kohta** · 2026-10-21 (`dev/scripts/et_ark_mends.py`): masin oli võtnud inglise sõna
  *ark* ja käänanud seda eesti moodi (*arkk*, *arku*, *arkt*, *arungi* …). `ארון` → **laegas** (*laeka ·
  laegast · laekasse*), Noa `תבה` → **laev** (*laeva*), kääne loetud igas lauses. 1Sm 7:2, Hs 17:12
  (*tõrksale kojale*), Js 41:29 ja 1Kn 6:19 (*devir*) kirjutati käsitsi ümber; Jr 51:3 *arksamb* → **vibu**.
  *Avatud: vaata §4, küsimus 5.*
- **NFC:** 7 faili teisendati normaalkujule NFC · 2026-10-21.
- **Teine voor — skript** · 2026-10-21 (`dev/scripts/et_second_round_mends.py`): lugemine pärast väravat
  leidis vead, mida värav ei näinud (lugemise punktid 1–27 ja 41–47). Parandatud: Nimi salmi voolus
  (*Jehve*, *Jaave*, *JAHVE*, *Jehoova* jt, Aam 2:4, Js 23:18, 2Kn 1:17); *Jumal* / *Issand* / *Eloim*
  `אלהים` või inimese kohal (*Jumala mees* → **Elohimi mees**); *ülestõusmine* `פשע` kohal → **üleastumine**
  (13 salmi); nimetüved kogu korpuses (*Jaakob* → **Jaakov**, *Taavet* / *Daavid* → **David**, *Iisrael* →
  **Jisrael**, *Aaron* → **Aharon**, *Egiptus* → **Mitsraim**). Värav loeb nüüd ka salmi voolu.
- **Lugemise parandused — käsitsi** · 2026-10-21 (`dev/scripts/et_reading_mends.py`, 70 salmi, iga koht
  loetud heebrea sõnade vastu; muudetud ainult `translation` ja sama sõna `gloss`):
  - *⟨Jumal⟩* sulgudes → **Elohim** / **Eloah** / **⟨Ta⟩**: 2Sm 7:26 (*Jahve Tsevaot ⟨on⟩ Elohim Jisraeli üle*),
    Ps 27:9, Ps 31:6 (*tõe El*), Ii 22:30, Esr 5:11–12 (*taeva ja maa Eloahi*).
  - Ps 146:9 — *orphanu* → **vaeslast**, *Jumalatute* → **jumalatute**.
  - Inglise ja võõrad sõnad: Ps 23:6 ja 1Ms 12:1 *houses / housest* → **kojas / kojast**; 2Ms 19:3 *housele*
    → **kojale**; 4Ms 35:4 *⟨from⟩* eemaldatud; 2Aj 24:27 → **Kuningate raamatu midrašis**; Hg 2:16 **puurat**,
    Ps 106:9 **Suufi**, Jr 50:25 **Kasdimi**, 2Ms 3:20 **imetegudega**; Õp 29:21 *⟨mānon⟩* → **manon**.
  - Tühjad ja katkised märgid: Js 53:11 (ka *põlgusi* → **süü**), 1Kn 6:27 (*sisemise koja keskele*,
    **⟨olid suunatud⟩**), Õp 22:29 (**Kuningate ees ta seisab, ta ei seisa tundmatute ees**), Õp 4:1
    (**pange tähele**), 3Ms 19:13 (`אתך` on „sinu juures“, mitte sihitise märk: **palgatöölise tasu ärgu
    jäägu ööseks sinu juurde hommikuni**), 3Ms 19:3 (**oma ema ja oma isa**).
  - Nimed ja käänded: Km 1:16 **Moše**, 1Aj 5:36 **Šlomo**, 5Ms 6:5 **Elohimit**, 1Ms 16:5 (**su sülle**,
    **tühiseks**), 2Ms 35:29 **⟨tooma⟩**, 3Ms 7:35 **võidmisosa**.
  - Moonutatud sõnad ja vale tähendus: 1Ms 1:2 (**tühi ja tühjus**), 1Ms 12:3 (**neid, kes sind neavad, nean
    ma**), 1Ms 22:2 (**Võta**), 2Ms 3:1, 2, 7, 12; 2Ms 8:14; 3Ms 19:14–15; 5Ms 6:1, 7; 5Ms 18:14
    (**märgiseletajaid**); Js 53:2, 4, 7 (**nagu utt oma pügajate ees vaikib**); Ps 1:2, 5, 6 (**aga õelate tee
    hukkub**); Ps 23:2, 5; Ii 38:3, 6, 8; Rt 1:6, 20, 21; Ül 2:5, 7, 13, 15, 17; Tn 7:9, 10, 13 (**Päevade
    Vana**; `כבר אנש` → **nagu inimese poeg**); 1Sm 3:1, 3 (**templis**); Hs 37:1 (**oru keskele**); Mi 5:1;
    Õp 8:23; Sk 12:10 (**läbi torganud**, **nagu nutetakse ainsa poja pärast**).

## §2 · Uuesti tõlgitud salmid

- **Maandumine** (2026-10-21 01:23): kogu Tanahh — 23 213 / 23 213 salmi.
- **Loendusvoor** (2026-10-21): 2 098 kohta, kõik korras pärast redelit.
- **Heebrea teksti taastamine** (2026-10-21): muudetud heebrea sõnad (`surface`) toodi tagasi allikast.

## §3 · Mis on õige — ära muuda

- **`isand` / `mu isand`** inimese kohta — Nime ei ole kustutatud (Ps 110:1 *mu isandale*).
- **`jumal` / `jumalad`** väikese tähega rahvaste jumalate ja ebajumalate kohta.
- **`ennustaja`** seisab ainult seal, kus heebrea tekst räägib ennustajatest (`קסם`, `עונן`, `גזרין`,
  `אשף`) — vaarao targad, 5Ms 18:10, 14, Bileam (Jos 13:22), Taanieli õukond (Tn 2:2, 27; 4:4; 5:7, 11),
  Jesaja loendid (Js 3:2; 44:25), Jr 27:9; 29:8, Mi 3:7; 5:11. Värav leiab neid 15; loetud — ükski `נביא` ei
  ole nii tõlgitud.
- **Eesti sõnad, mis näevad välja nagu inglise sõnad:** **king** (jalanõu, 5Ms 29:4), **and** (kingitus,
  3Ms 7:16; Hs 46:5; 48:10, 21; Esr 8:28). Need on eesti sõnad, mitte lekked.
- **`Jumalatute` suure tähega salmi alguses** (Js 10:6, Ps 35:16) — *jumalatu* (jumalakartmatu); lause
  algus, mitte Nimi.
- **Laeka teisikud:** **aru** (mõistus), **arklane** (`ארכי`, 2Sm 15:32 jm) — õiged, värav jätab need
  süütuks.
- **`Ehje ašer ehje`** (2Ms 3:14) — `אהיה אשר אהיה` heebrea kõla järgi; see on valik, mitte viga.

## §4 · Küsimused, mis ootavad eesti keelt kõnelevat inimest

1. **`Jahve`** ja käänded — kas *Jahvet* · *Jahvele* · *Jahvest*, või parem käänamatu *Jahve*?
2. **`ruahh` · `mašiahh`** — *hh* `ח` jaoks; või *h*?
3. **Nimed** (*Avraham, Jitshak, Jaakov, Moše* või *Aabraham, Iisak, Jaakob, Mooses*) — heebrea kõla või
   nimed, mida lugeja tunneb?
4. **Loomad** — *kaljumäger* `שפן` jaoks; *metskits* `יחמור` jaoks; *leping* `ברית` jaoks.
5. **Laegas / laev — kääne 44 kohal.** Masin oli need kohad täitnud inglise sõnaga *ark*; käsi pani asemele
   *laegas* ja *laev* ning luges käände igas lauses (näiteks *paned laekasse* 2Ms 25:16, *kaane laeka peale*
   2Ms 40:20, *vaadanud Jahve laekasse* 1Sm 6:19). Kääne on käe valik, mitte eesti kõrva oma. Palun loe need
   44 salmi (loend `dev/scripts/et_ark_mends.py`) ja ütle, kas kääne on õige.
6. **`nefeš` / `nefesh`** — `נפש` on jäänud tõlkimata 148 failis (näiteks Ps 23:3 *Minu nefesh*). Reeglid
   (D2) seda sõna ei nimeta. Kas see on hoitud sõna nagu *ruahh* (siis üks kirjapilt — *nefeš*), või tuleb
   kirjutada *hing*?
7. Kõik sõnad — neile on vaja eesti lugejaid.

## Avatud küsimused — mis on veel alles

Lugemine pärast väravat (2026-10-21, pärast 361a8f2b) leidis 74 punkti: näidis üle 150 salmi kõigist kolmest
osast ja kogu korpuse otsing klasside kaupa. Punktid 1–27 ja 41–47 parandas teise vooru skript
(`dev/scripts/et_second_round_mends.py`), ülejäänud parandati käsitsi (`dev/scripts/et_reading_mends.py`) —
vaata §1. **Alles on:**

1. **Kõikuvad kirjapildid, mida reeglid ei nimeta (punkt 49)** — vali üks: *Siion* 110 / *Tsijon* 9 (käsi
   valis *Tsijon*); *Joosep* / *Joosua* / *Josef*; *Saul* / *Šaul*; *Taaniel* / *Daniel*; *Šemuuel* /
   *Šmuel* / *Samuel*; *Iiob* / *Ijov*; *Juuda* / *Jehuda*; *Javeš* / *Jaaveš* / *Jabeš*; Rt 1-s *Naomi* /
   *Noomi* / *Naemi*, *Beit-Lehem* / *Beet-Lehem* / *Beit-Lechem* (ka Mi 5:1), *Ruut* / *Rut*, *Moabi* /
   *Moobi* (Rt 1:22), *Eliimelek*; *Para'o* / *Paroosi* (2Ms 7:22). **Ei ole muudetud.**
2. **Õp 29:21 `מנון`** — haruldane sõna, tähendus ebaselge; nüüd kirjutatud **manon** (heebrea kõla). Kas
   eesti sõna (*poeg*? *tänamatu*?) või jääb nii?
3. **Valikud, mida käsi tegi ja mida eesti kõrv peaks kinnitama:** *Päevade Vana* (`עתיק יומין`, Tn 7:9, 13);
   *nagu inimese poeg* (`כבר אנש`, Tn 7:13); *templis* `היכל` kohal (1Sm 3:3) või *heikhal*; *päev hingab*
   (`שיפוח היום`, Ül 2:17); *kohtuseadused* `משפטים` kohal (5Ms 6:1); *kordad* `ושננתם` kohal (5Ms 6:7).
4. **3Ms 19:13** — sõna `לא` gloss on veel *ära*, salm ütleb nüüd *ärgu*; väike, jäetud.
5. **Salmifailide `notes` väljad** (masina põhjendused) on sageli inglise keeles ja kasutavad kohati sõna
   *Jumal* (näiteks 1Ms 1:1 *Jumala loomise alguses*). Need ei ole salmi voolus ega väravas; kas need
   jäävad, tõlgitakse või eemaldatakse avaldamisel?
6. **Näidis on näidis:** samu klasse (moonutatud sõnad, vale kääne, kõikuvad nimed) on kindlasti ka mujal.
   Iga eesti lugeja salm kaalub rohkem kui see loend.
