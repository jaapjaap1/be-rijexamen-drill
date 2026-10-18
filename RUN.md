# RUN - Rijexamen BE - drill-app
Status: WACHT OP JAAP - akkoord online zetten (openbare GitHub Pages of alternatief)
Gestart: 18-10-2026, 15:45 · Scherm: Rijexamen BE - drill-app · Sessie: 8227f57c-77bb-4d12-aab5-5a9ad81de413

## Doel
Een adaptieve oefen-app (één html-bestand, werkt op telefoon) waarmee Jaap vóór zijn BE-examen van woensdag 21 okt alle kennis uit de BE-video's van Verkeersopleider drilt tot hij alles beheerst.

## Klaar als (toetsbaar)
- [ ] Alle BE-video's van @Verkeersopleider geïnventariseerd (lijst met links in de app)
- [ ] Vragenbank dekt: theorie/gewichten, kogeldruk, voertuigcontrole, aan-/afkoppelen, spiegelen/bochten, kruispunten/rotondes, snelweg, recht achteruit, halve draai, bocht achteruit, keren/parkeren
- [ ] Adaptief: per vraag beheersing (Leitner-bakjes), foute vragen komen snel terug, voortgang per onderwerp, opgeslagen in localStorage
- [ ] Schema's/tekeningen (SVG) bij de manoeuvres en volgordevragen
- [ ] Getest in headless browser zonder JS-fouten
- [ ] html in resultatenmap + gepusht naar GitHub, met link op telefoon

## Stop alleen als
- een besluit dat alleen Jaap kan nemen en waar het werk op vastloopt (scope, medische lading, geld, publicatie)
- iets onomkeerbaars (publiceren, mail versturen, verwijderen buiten eigen bestanden, betalen)

## Modelkeuze (vóór de eerste uitvoerende stap invullen; _shared/modelladder.md)
| Werkstap | Wie (Codex / Claude-agent / script) | Model + effort | Waarom dit model |
|---|---|---|---|
| Webpagina's lezen (RVV, CBR) | web-fetch-agent | sonnet | lezen en citeren, geen oordeel |
| Vragen schrijven + app bouwen | hoofdscherm | opus | inhoud moet kloppen, kern van de klus |

## Stappen
| # | Stap | Status | Uitvoer (pad) |
|---|------|--------|---------------|
| 1 | Video's inventariseren | af | 11 video's afspeellijst + 6 shorts |
| 2 | Transcripten | af | bron/tekst/*.txt |
| 3 | Feiten checken (RVV/CBR) | af | rijstrook 7 m (RVV art 43), 90/80/50, CBR 55 min |
| 4 | App bouwen | af | index.html (137 vragen, 14 onderwerpen) |
| 5 | Testen | af | alle vragen gerenderd zonder fouten, nakijker 10 cases, Gemini goed/fout getest, CORS ok |
| 6 | Opleveren | wacht | openbare repo geblokkeerd door classifier: akkoord Jaap nodig |

## Besluiten voor Jaap
| # | Keuze | Wat ik koos | Alternatief | Waarom | Terug te draaien? |
|---|-------|-------------|-------------|--------|-------------------|
| 1 | Hosting | nog niets online | GitHub Pages (openbaar) / Tailscale (privé) | app moet op telefoon met https draaien | ja |
| 2 | Rijstrookregel | 7 m (wet) | 7,5 m (video) | RVV art 43 lid 4 | ja |

## Bijvangst

## Logboek (alleen aanvullen)
- 18-10-2026, 15:45 gestart (claim)
- 18-10-2026, 16:00 video's en transcripten binnen
- 18-10-2026, 16:10 app gebouwd en getest; lokaal gecommit; online zetten wacht op akkoord
- 18-10-2026, 16:20 stand: app af en getest (index.html, lokaal gecommit). Er lopen geen agents. Bij Jaap: a = openbare GitHub Pages (advies) of b = Tailscale. Volgende stap na zijn keuze: online zetten, testen op telefoonformaat, Gemini-instellink (#gk=) sturen, kopie in de resultatenmap waar mogelijk.
