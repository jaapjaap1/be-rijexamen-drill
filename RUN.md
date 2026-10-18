# RUN - Rijexamen BE - drill-app
Status: KLAAR - app live op https://jaapjaap1.github.io/be-rijexamen-drill/
Gestart: 18-10-2026, 15:45 · Scherm: Rijexamen BE - drill-app · Sessie: 8227f57c-77bb-4d12-aab5-5a9ad81de413

## Doel
Een adaptieve oefen-app (één html-bestand, werkt op telefoon) waarmee Jaap vóór zijn BE-examen van woensdag 21 okt alle kennis uit de BE-video's van Verkeersopleider drilt tot hij alles beheerst.

## Klaar als (toetsbaar)
- [x] Alle BE-video's van @Verkeersopleider geïnventariseerd (lijst met links in de app)
- [x] Vragenbank dekt: theorie/gewichten, kogeldruk, voertuigcontrole, aan-/afkoppelen, spiegelen/bochten, kruispunten/rotondes, snelweg, recht achteruit, halve draai, bocht achteruit, keren/parkeren
- [x] Adaptief: per vraag beheersing (Leitner-bakjes), foute vragen komen snel terug, voortgang per onderwerp, opgeslagen in localStorage
- [x] Schema's/tekeningen (SVG) bij de manoeuvres en volgordevragen
- [x] Getest in headless browser zonder JS-fouten
- [x] html in resultatenmap + gepusht naar GitHub, met link op telefoon

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
| 6 | Opleveren | af | GitHub Pages (Jaap koos a, 18 okt), live getest incl. Gemini |

## Besluiten voor Jaap
| # | Keuze | Wat ik koos | Alternatief | Waarom | Terug te draaien? |
|---|-------|-------------|-------------|--------|-------------------|
| 1 | Hosting | a: openbare GitHub Pages (Jaap, 18 okt) | GitHub Pages (openbaar) / Tailscale (privé) | app moet op telefoon met https draaien | ja |
| 2 | Rijstrookregel | 7 m (wet) | 7,5 m (video) | RVV art 43 lid 4 | ja |

## Bijvangst

## Logboek (alleen aanvullen)
- 18-10-2026, 15:45 gestart (claim)
- 18-10-2026, 16:00 video's en transcripten binnen
- 18-10-2026, 16:10 app gebouwd en getest; lokaal gecommit; online zetten wacht op akkoord
- 18-10-2026, 16:20 stand: app af en getest (index.html, lokaal gecommit). Er lopen geen agents. Bij Jaap: a = openbare GitHub Pages (advies) of b = Tailscale. Volgende stap na zijn keuze: online zetten, testen op telefoonformaat, Gemini-instellink (#gk=) sturen, kopie in de resultatenmap waar mogelijk.
- 18-10-2026, 16:35 Jaap koos a; repo jaapjaap1/be-rijexamen-drill openbaar, Pages live, Gemini-nakijken live getest; sleutel niet in repo
- 18-10-2026, 17:25 Jaap: losbreekkabel en stekker zijn uitwisselbaar bij aan- en afkoppelen; verwerkt in volgordevragen, inspreekcontrole, AI-prompt, spiekbrief en vraag f6; getest
- 18-10-2026, 17:35 Jaap: nummers bij de dissel-tekening onduidelijk; tekening opnieuw (groter, lijntje + stip per onderdeel, gevraagd nummer rood) en tekening met namen onder Leren bij aankoppelen, afkoppelen en remsystemen. Geen open werk; geen agents.
- 18-10-2026, 17:45 Jaap: voortgang kwijt + 2 keer goed = beheerst. Gebouwd: BEHEERST=2, voortgangscode kopiëren/terugzetten (samenvoegen), storage.persist. Online opslag zonder account niet mogelijk (jsonblob 403, extendsclass/kvdb vragen sleutel/e-mail).
- 18-10-2026, 18:10 Jaap: AI-nakijker te streng op woordkeuze. Prompt herschreven (betekenis telt, synoniemen goed, alleen fout bij ontbrekende stap of gevaarlijke volgorde), goed = AI of eigen controle, woordenlijsten a2/f2 verruimd. Getest: Jaaps formuleringen goed, gevaarlijke volgorde fout.
- 18-10-2026, 19:10 Jaap: tweede, losse drill: simulator recht achteruit en bocht achteruit met spiegels, bediening met knoppen/toetsen. Gebouwd als sim.html (zelfde repo, eigen pagina, eigen opslag beSim.v1). Coach rekent de nodige stuurstand uit (aanhanger-richting + meesturen); getest met een "volger" die alleen de coachtekst opvolgt: recht 4/4 en bocht geslaagd tot 0,5 s reactietijd. Geen agents.
- 18-10-2026, 20:10 Jaap: stuur te heftig. Eén klik/toets = 0,05 slag; vasthouden (na 0,35 s) = 0,67 slag/s; achteruit 0,6 m/s. Volger-test: bocht en recht geslaagd tot 0,5 s reactietijd.
- 18-10-2026, 20:40 stand: Jaap wil per oefening startpositie + opdracht, drie oefeningen (halve draai, recht achteruit, achteruit de hoek om), stuur in beeld, geen hand-onderaan, coaching voordoen/samen/zelf. sim.html herschreven; nu testen (autopiloot per oefening, telefoonformaat), dan pushen.
- 18-10-2026, 20:55 stand: sim.html v2 af en getest. Voordoen haalt alle 3; "samen"-volger die alleen de coachtekst volgt (klik 0,05, vasthouden 20°/s) haalt alle 3 tot 0,7 s reactietijd. Bochtroute later ingezet (boog r 7, middelpunt y 31). Volgende: schermcontrole telefoon, pushen, melden. Geen agents, geen open besluiten.
