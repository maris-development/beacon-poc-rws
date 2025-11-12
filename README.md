# beacon-poc-rws

## IHM_beacon.ipynb
In de voorgaande PoC zijn meerdere Nederlands mariene databronnen onderzocht en de onderstaande zes bronnen zijn uiteindelijk gekozen als input voor de IHM-specifieke Beacon instantie die via de IHM_beacon.ipynb notebook en de nieuwe GUI (Beacon studio - https://beacon-ihm.maris.nl/studio/) te bevragen en visualiseren zijn:
- WADAR BETA
- Aquadesk
- RWS CTD collectie
- VIS monitoring
- Vogel monitoring
- WOT data WMR

De IHM Beacon instantie is hier beschreven: https://beacon-ihm.maris.nl/swagger/. Deze is zo veel mogelijk geactualiseerd, compleet gemaakt en wordt operationeel beheerd. Ter voorbereiding van het ontwikkelen van de Beacon GUI zijn er voor de WADAR, RWS-CTD en Aquadesk, “easy” tables aangemaakt met de belangrijkste (meta)data kolommen en ook aggregaties en mappings toegepast om de collecties zo goed en simpel mogelijk doorzoekbaar te maken voor de gebruiker. 

In de IHM_beacon.ipynb notebook staat er voor iedere bovenstaande collectie een voorbeeld, hoe deze te bevragen zijn. 

## WADAR_mapping.ipynb & Aquadesk_mapping.ipynb
In de eerste PoC zijn er voor verschillende databronnen Beacon instanties opgezet, waarbij Beacon naast de data ook alle metadata inleest, en in staat is om te ondersteunen via mappings naar vocabulaire zoals voor parameters, soortnaam, eenheid, etc. Tijdens de evaluatie van het project is vanuit IHM de volgende wens geformuleerd: “Als Beacon de data EN metadata van een bepaalde data collectie helemaal kan inlezen en semantisch kan harmoniseren en kan exporteren naar een aantal dataformats, zou Beacon dan ook kunnen ondersteunen in het publiceren van Nederlandse observatiedata met metadata (en later eventueel andere data) volgens de internationale standaarden zoals in gebruik in EMODnet?”

Er is gekozen om een onderzoek te doen naar de haalbaarheid voor Aquadesk als representatieve dataset voor mariene biodiversiteitsdata. Daarnaast is er ook gekeken naar WADAR data, beschikbaar gemaakt via de Beta WaterWebservices dat mariene physische en chemische datasets bevat. Mocht de haalbaarheid bewezen worden, dan kan dit ook uitgebreid worden naar project data van b.v. MONS en WOZEP.

De materie is complex en heeft verschillende uitdagingen m.b.t. inlezen van de benodigde metadata, creëren van verschillende syntactische en semantische mappings, aggregatieniveau van uitlevering, en het schrijven van de output files in de juiste formats. Daarom is er in deze eerste fase gestart met een haalbaarheidsstudie voor Aquadesk en WADAR data met een kleine demonstratie via de twee notebooks WADAR_mapping.ipynb & Aquadesk_mapping.ipynb van het genereren van output passend bij de benodigde formats voor chemisch/fysische data volgens SeaDataNet (WADAR), en voor biodiversiteitsdata volgens OBIS-ENV (Aquadesk), voor slechts enkele datasets, en nog zonder de gehele semantische (vocab naar vocab) mapping voor de gehele databron te maken.

Conclusie: Na een eerste analyse door MARIS voor de bronnen WADAR en Aquadesk is de conclusie dat dit inderdaad mogelijk is, maar dat er nog verdere stappen nodig zijn naar operationalisatie.
