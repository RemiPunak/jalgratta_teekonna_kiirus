# jalgratta_teekonna_kiirus
Kohandatava sõidukiirusega veebipõhine jalgratta teekonna prognoosija, mis arvutab OSRM API ja Leaflet kaardiliidese abil reaalajas distantsi ning sõiduaega. Toetab mitme vahepunkti lisamist ja mobiilset asukohatuvastust.

# Jalgratta teekonna prognoosija

Veebipõhine kaardirakendus jalgrattateekondade planeerimiseks, distantsi arvutamiseks ja sõiduaja prognoosimiseks. Rakendus on loodud puhta kliendipoolse (client-side) lahendusena, kasutades kaasaegseid veebitehnoloogiaid ja avatud lähtekoodiga geoinfosüsteemide liideseid.

## Põhifunktsioonid

* **Dünaamiline teekonna arvutus:** OSRM (Open Source Routing Machine) jalgsikäigu/rattasõidu profiili päringud reaalajas.
* **Mitme punkti tugi:** Võimalus lisada piiramatult vahepunkte (Waypoints) alg- ja sihtkoha vahele.
* **Paindlik kiiruse modelleerimine:** Teekonna kestuse ümberarvutamine reaalajas vahemikus 5–40 km/h (vaikeväärtus 22 km/h).
* **Asukohatuvastus ja Fallback:** Geolocation API tugi kasutaja asukoha määramiseks. Kui päring on brauseris või turvapiirangute (iframe) tõttu keelatud, rakendub automaatselt vaikeasukoht: Erminurme tee 22, Tartu (58°23'26.2"N 26°44'55.7"E).
* **Interaktiivne geokodeerimine:** Aadressiotsing ja koordinaatide pöördgeokodeerimine (Reverse Geocoding) üle Nominatim (OpenStreetMap) API. Toetab aadressipunktide lohistamist (drag-and-drop) otse kaardil.
* **Mobiilisõbralik UI:** Tailwind CSS-i abil loodud reageeriv (responsive) disain koos kokkuvolditava juhtpaneeliga (Bottom Sheet), mis optimeerib ekraaniruumi kasutust mobiilseadmetes.

## Tehniline stäkk

* **Käituskeskkond:** HTML5, JavaScript (ES6+), CSS3
* **Kaardimootor:** Leaflet.js (v1.9.4)
* **Disainiraamistik:** Tailwind CSS
* **Ikoonid:** Lucide Icons
* **Andmeallikad:** OpenStreetMap, OSRM API, Nominatim API
