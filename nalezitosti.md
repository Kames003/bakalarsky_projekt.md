## FrontEnd 
Technológia: Flutter (Dart) alebo React Native (JavaScript/TypeScript)

## Mapové podkaldy 
: Mapbox, Leaflet (s OpenStreetMap), prípadne Locus API (pre GPX)

## Preferovany je MapBox : 
Podporuje offline režim, vrstvy, štýly, 3D vizualizácie.
Výborný na navigáciu, trasy, vizualizáciu CHKO zón.

!!! TO MENTION IMPORTANT 

## UI / UX návrh dizajnu - ešte pred začatim vypracovanie by som ho priniesol 
Alebo ina graficka knižnica pre vizualizcia a rozloženie na štyl Figma

## BackEnd - api + ds 
Python FastAPI 
databaza : PostGreSQL + POSTGIS - pre geolokačne data + uživatelske profily , redis pre cache 

## Geolokacia pa chko zony 
import SHP suborov do PostGIS - rozširenie postgreSQL pre geodata 
obsahuje hranice zon, CHKO na štyle nachadza sa poloha v pasme CHKO 
= vypočitanie intersekcie pozicie pouzivatelov s chko vrstvami 

## AI komponentny / volitelne 

### symptómy a rozpoznávanie zranení:

NLP model (napr. spaCy, HuggingFace transformers)
NLP (Natural Language Processing) → rozpoznávanie textu (napr. opis symptómov).
spaCy: rýchla, jednoduchá knižnica pre analýzu textu.
HuggingFace: ponúka predtrénované AI modely, ktoré vieš použiť na klasifikáciu symptómov.

Computer Vision (mobilná AI cez TensorFlow Lite)
eventualne by bol schopny spracovať zranenia krvacanie zvierata nakolko je schopny spracovavať obraz z kamery 

## ChatBot pre prvu pomoc 
Rasa alebo DialogFlow 


## Hardware rozšírenie (v budúcnosti)
### Mikrokontroléry: ESP32 alebo Raspberry Pi Pico W (Bluetooth + WiFi)

Senzory: Pulzný oxymeter (MAX30102), gyroskop (MPU6050) pre detekciu pádu

Komunikácia: Bluetooth LE alebo LoRa pre odosielanie dát do mobilu

### Dizajn hardverovej časti ak to aktuatorom nazyvať smiem by som si navrhol a vytlačil 

## ESP32
Malý a lacný mikrokontrolér s Wi-Fi a Bluetooth.

Vhodný na nositeľné zariadenia (napr. náramok pre sledovanie tepu).

Vie komunikovať s mobilom → napr. odoslať SOS ak tep prudko klesne.

## Pulzný oxymeter: MAX30102
Meria tep a saturáciu kyslíka v krvi.

Možno ho pripojiť na ESP32 a odosielať hodnoty do aplikácie.

## Gyroskop / akcelerometer: MPU6050
Detekuje pohyb, pád, otras.

detekcia pádu cyklistu.

## Komunikácia: Bluetooth LE alebo LoRa
Bluetooth Low Energy (BLE): krátky dosah, vhodné pre wearables (náramky, hodinky).

## Legenda pre vysvetlenie implementačnej strategie 

MVP - Minimum Viable Product
Post-MVP – Počiatočné rozšírenia po MVP
Rozšírenia (Extensions / Bonus Features)
 
## Priorita	Funkcia	Status
1.	Lokalizácia v CHKO + pravidlá	✅ MVP
1.	SOS tlačidlo + GPS	✅ MVP
2.	Záznam a export trasy	✅ MVP
2.	Edukácia o CHKO a faune/flóre	✅ MVP
3.	AI pre prvú pomoc	🔄 Post-MVP
3.	Monitorovanie vitálnych funkcií	🔄 Post-MVP
4.	Detekcia pádu + alarm	🔄 Post-MVP
4.	Zdieľaná poloha skupiny	🔄 Post-MVP
5.	Výzvy, kurzy, výbava, komunitné funkcie	🔄 Rozšírenie
