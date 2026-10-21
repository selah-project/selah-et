# PÄRITOLU — kuidas see tõlge tehti

*Eesti keel. Heebrea Pühakiri, salm salmi järel. Alustatud 2026-10-20 19:01; kogu Tanahh maandus
2026-10-21 01:23; loendusvoor ja käsitsi parandused lõpetatud 2026-10-21 03:08 (USA idaranniku aeg,
EDT = UTC−4).*

See on kirje sellest, kuidas see tõlge tehti ja mida tuleb veel parandada. Masintõlge ei vääri usaldust,
kui sa ei näe, kuidas see tehti. Seepärast ütleb see fail kõik — **ka meie vead.**

---

## Kuidas töö käis

Iga salm tõlgiti oma heebrea tekstist (OSHB / Westminster Leningrad Codex) reeglite järgi, mis on
kirjutatud eesti keeles (`docs/methodology/translation-discipline/et.md` projektis Selah). Masin:
**glm-5.3** (Zhipu) kõigis 23 213 failis; välja `tier` väärtus on **glm-5.2** — rada, mille kaudu kõned
käisid. 21 078 failil on täielik `provenance` plokk (süsteemi- ja kasutajaviiba SHA-256, viibafail, koodi
versioon); 2 135 faili, mis kirjutati ümber loendusvoorus, kannavad ainult `model`, `tier` ja `timestamp`.

Iga kuni nelja salmi rühma jaoks sai masin: heebrea teksti (märkidega ja ainult tähtedega); iga sõna koos
selle sõnaraamatuvormi, Strongi numbri ja Strongi tähendusega; naabersalmid; reeglid eesti keeles; ja
**seitse ingliskeelset tõlget võrdluseks** (Wycliffe, Geneva 1599, King James, Young's Literal, American
Standard, JPS 1917, Berean Standard) koos naabruses olevate King Jamesi salmidega. *(Need võrdlused jäeti
meelega ja on avalikult märgitud; „puhta ruumi“ käik — ainult heebrea tekst ja sõnaraamat — tuleb hiljem
eraldi muudatusena.)*

Igal salmil on kaks kuju: **eesti sõna iga heebrea sõna jaoks** ja **kogu salm** eesti keeles. Mõlemad on
hoitud.

## Proov enne algust

Kakskümmend sõna tõlgiti eesti keelde ja tagasi inglise keelde: tagasi tuli **20 / 20**. Loomade proov
salmis (exp 1200): **37 / 46** — vead (`הערב` → *kadakas* ronga asemel, `לשפנים` → *kahanik*, `השפן` →
*kärp*, `ומריא` → *pull*) läksid reeglitesse. Reeglitel oli **Nimede ja võtmesõnade tabel** ja **loomade
tabel** esimesest salmist peale — üks sõna ühes kohas, alati.

## Mida kontrolliti

Värav (`dev/scripts/et_gate.clj`), kõigis 23 213 failis:

- **Nimi:** `Jahve` **6 007 / 6 007** kohal.
- `ISSAND`, `Issand`, `Igavene`, `Jehoova`, `YHWH` Nime kohal; `Jumal` üksi `יהוה` kohal: **0**.
- `Kristus`, `Jeesus`, `Messias`: **0**.
- Soome, läti ja kirillitsa tähed: **0**. Inglise sõnad (*the*, *of*, *which*, *with*): **0**. Inglise
  sõnad või `⟨ה⟩` sulgudes: **0**.
- Heebrea sõnad salmi voolus: **0**. Tekst mitte NFC-kujul: **0**.
- `ennustaja`: **15** — need on salmid ennustajatest (`קסם`, `עונן`, `גזרין`, `אשף`), loetud ja õiged;
  ükski ei ole `נביא`.

Värav lasti uuesti pärast käsitsi parandusi (361a8f2b): Nimi **6 007 / 6 007**, kõik teised klassid **0**,
`ennustaja` **15** (samad õiged salmid).

**Aga värav ei näe kõike.** Nime kontroll loeb ainult paljast `יהוה` kohta **sõna** (`gloss`) tasemel —
mitte eesliitega kohti (`ליהוה`, `ביהוה`) ega salmi voolu. Lugemine pärast väravat leidis voolus
**21 salmi**, kus Nimi on valesti kirjutatud või kadunud (*Jehve*, *Jaave*, *JAHVE*, *Jahevile*, *Jähvile*,
*Jehovale*, *Jehoovat*; Aam 2:4 *Nõnda ütleb Jehuda*), *Jumal* `אלהים` kohal (*Jumala mees* jm), *ülestõusmine*
`פשע` (üleastumise) kohal, inglise ja võõraid sõnu (*houses*, *⟨from⟩*, *orphanu*), kiriklikke nimekujusid
(*Jaakob* 168 salmis) ja moonutatud sõnu. Need parandati teises voorus
(`dev/scripts/et_second_round_mends.py`) ja käsitsi (`dev/scripts/et_reading_mends.py`, 70 salmi); värav loeb
nüüd ka salmi voolu. Mis on alles, on loetud `NOTES.md` lõpus („Avatud küsimused“).

## Mida parandati

- **Heebrea tekst:** muudetud heebrea sõnad taastati allikast (surface restore).
- **Loendusvoor** (2 098 kohta, kõik korras pärast redelit): võõrad tähed, inglise sõnad, märgid, heebrea
  sõnad voolus.
- **Käsitsi** (361a8f2b, `dev/scripts/et_post_round_mends.py`): Nimi ×3 (*JaHve*, *Jaahve*, *Jahe* →
  *Jahve*); nimetüved reeglite järgi (*Binjamin*, *Tsijon*, *Eljon*, *Babülon*, *Jabeš*); kirillitsa ja kreeka
  tähed 7 sõnas; heebrea ja katkised sulud voolus (1Ms 19:23, Jr 51:24, Ps 120:6, Ii 9:30, 2Aj 4:11,
  4Ms 4:14, Esr 4:17); *syndaja* → *patustaja* ja `הן` *vaata* (Õp 11:31); *skinny-maal* → *stepimaal*
  (Jr 2:6); NFC 7 failis.
- **Laegas** (`dev/scripts/et_ark_mends.py`): masin oli võtnud inglise sõna *ark* eesti keelde ja käänanud
  seda 44 kohal (*ark · arki · arku · arkk · arkt · arkn · arkast · arukk · arukis · arundi · arungi · arut*)
  — `ארון` jaoks ja Noa `תבה` jaoks. Parandatud käsitsi: **laegas** (*laeka · laegast · laekasse*) ja **laev**,
  kääne loetud igas lauses. 1Sm 7:2, Hs 17:12, Js 41:29, 1Kn 6:19 kirjutati ümber, sest press ei pidanud;
  Jr 51:3 *arksamb* → *vibu*.

## Masin ja inimene

**Iga sõna salmifailides tegi masin**, välja arvatud käsitsi parandused, mis on nimetatud `NOTES.md` §1.
Enamikku salme ei ole lugenud ükski inimene. **Ükski eesti keelt kõnelev inimene ei ole seda tõlget veel
lugenud.** See on endiselt kõige avatum küsimus.

Kogu töö ajalugu: `NOTES.md` ja git'i ajalugu.
