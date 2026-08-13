# DAGELIJKSE UPDATE-PROMPT — MACRO → MICRO DASHBOARD

Kopieer het blok hieronder integraal in een nieuw gesprek. Voeg de bestanden toe die onder BIJLAGEN staan. Wat je niet hebt, laat je gewoon weg — de prompt vertelt Claude hoe daarmee om te gaan.

---

## HET BLOK — kopieer vanaf hier

**OPDRACHT**

Werk mijn Macro → Micro dashboard bij naar de stand van vandaag. Lever één compleet HTML-bestand terug, dezelfde structuur en dezelfde lichte layout als het bijgevoegde bestand. Wijzig alleen het DATABLOK bovenin het script, niet de architectuur.

**BIJLAGEN**

1. Het dashboard-HTML van gisteren
2. DEGIRO Account Statement (CSV) — Activiteit → Rapporten → Account Statement
3. Actuele niveaus van de zes instrumenten uit TradingView: MGC1!, MNQ1!, SIL1!, MCL1!, GER40, UK100 — laatste slotkoers en dagverandering
4. EDGAR-uitdraai Form 4 sinds de vorige update (indien beschikbaar)
5. Nieuwe Google Alerts of nieuwsberichten die ik zelf heb doorgestuurd
6. Eventueel: een nieuwe Part van de Connections Map

**STAP 1 — CONTROLEER EERST, WERK DAARNA BIJ**

Toets vóór elke wijziging deze vijf dragende beweringen aan een live bron. Zoek daadwerkelijk; ga niet af op wat in het bestand staat.

- De status van de Straat van Hormuz en het olieniveau (WTI én Brent)
- De renteverwachting voor de eerstvolgende FOMC — welke maand prijst de markt nu in
- De laatste CPI- en payroll-uitkomst, inclusief de revisies op eerdere maanden
- De stand van de zes instrumenten en, indien in mijn bezit, de tien posities
- Elke tariefmaatregel met een datum binnen dertig dagen

Rapporteer per bewering: BEVESTIGD, GECORRIGEERD of ONOPGELOST, met de bron en de datum van controle. Verwerk correcties door in de rest van het dashboard — een omgekeerd teken in de macro moet doorwerken in de heatmaps en de scenariomatrix.

**STAP 2 — INSIDERTRANSACTIES**

Scheid strikt op transactiecode en behandel ze niet gelijk:

| Code | Betekenis | Weegt mee |
|---|---|---|
| P | Open-markt aankoop, discretionair | JA — sterkste signaal |
| S zonder plan | Discretionaire verkoop | JA — als signaal |
| S onder 10b5-1 | Vooraf ingepland | NEE — noteer plandatum |
| A | Toekenning | NEE |
| F / M | Belastinginhouding of optie-afwikkeling | NEE |

Zet bij elke transactie de **leeftijd in dagen** naast de datum. Markeer alles ouder dan 150 dagen als verlopen. Voeg één regel toe met de marktbrede koop-verkoopverhouding als context, zodat een leeg beeld niet als datagat wordt gelezen.

**STAP 3 — PORTEFEUILLE**

Lees de CSV uit voor aantal, koers, kostprijs en valuta. Bereken zelf: waarde in euro, weging, gewogen driverblootstelling per kolom van de heatmap, en de verandering ten opzichte van de vorige update. Vermeld de EUR/USD die je gebruikt en waar die vandaan komt.

**STAP 4 — KALENDER**

Schuif het venster op. Verwijder wat is afgehandeld, maar bewaar de uitkomst als één regel. Controleer of er nieuwe gedateerde gebeurtenissen bij zijn gekomen: expiraties, Fed-data, macrocijfers, beleidsmaatregelen, kwartaalcijfers. Markeer per datum of hij BEVESTIGD is bij de bron of GESCHAT uit een patroon.

**HARDE REGELS**

1. Vul nooit een getal in dat niet uit een genoemde bron komt. Ontbreekt een bron, dan blijft het veld leeg en gemarkeerd.
2. Elk getal draagt een bronklasse-badge. Analistendoelen zijn de zwakste klasse en worden nooit als niveau gepresenteerd zonder dat erbij te zeggen.
3. Een niveau zonder antwoord op alle drie de vragen — wie handelde hier, zitten ze er nog, wat verwijdert ze — krijgt het label GEEN DEKKING en wordt niet weggelaten.
4. Tijdstempels staan per bron apart in de kopregel. Is de portefeuille van vandaag en de marktfeed van gisteren, dan staat dat er zo.
5. Bij een nieuwe Part van de Connections Map verwerk je alleen het scorebord en de verschillen — niet het hele document opnieuw samenvatten.
6. Meld actief wat je níét hebt kunnen verifiëren. Een gat dat benoemd is, is bruikbaar; een gat dat is opgevuld met een aanname is gevaarlijk.

**LEVERING**

Het complete HTML-bestand, plus in de chat een korte samenvatting van maximaal tien regels met: wat er is gecorrigeerd, wat er nieuw is, en wat er vandaag als eerste aandacht vraagt.

## — tot hier

---

## KORTE VERSIE

Voor dagen waarop er weinig is gebeurd:

> Werk het bijgevoegde dashboard bij naar vandaag. Controleer eerst Hormuz/olie, de renteverwachting en de laatste CPI- en payrolluitkomst aan live bronnen en meld per punt BEVESTIGD of GECORRIGEERD. Verwerk daarna de bijgevoegde DEGIRO-CSV en de TradingView-niveaus. Scheid insidertransacties strikt op code — alleen P telt als koopsignaal, F en A tellen niet, S onder 10b5-1 draagt geen informatie. Vul niets in zonder bron; laat ontbrekende velden leeg en gemarkeerd. Lever één compleet HTML-bestand plus tien regels samenvatting.

---

## WAT JE MEELEVERT, EN WAAROM HET UITMAAKT

| Bijlage | Zonder | Met |
|---|---|---|
| DEGIRO CSV | Kostprijs wordt afgeleid uit W/V ÷ W/V%, zonder transactiekosten of aankoopdata | Exacte kostprijs, aankoopdatum, kosten, dividend |
| TradingView-niveaus | Macroprijzen lopen dagen achter op de analyse eromheen | Cones en niveaus kloppen weer bij de prijs |
| EDGAR Form 4 | Insiderlaag veroudert stil; alleen namen met nieuwsdekking worden gevonden | Volledige dekking, inclusief small caps zonder pers |
| Optie-impliciete beweging | Elk event wordt als even onverwacht behandeld | Onderscheid tussen "belangrijk" en "al ingeprijsd" |
