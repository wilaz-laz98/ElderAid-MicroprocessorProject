# Real time clock

L'HW-084 est un module RTC (Real Time Clock) basé sur le DS3231, une horloge temps réel très précise. Il est conçu pour conserver l'heure et la date de manière fiable, même en cas de coupure d'alimentation, grâce à une pile de sauvegarde.

## Caractéristiques principales du HW-084 (DS3231) :
 
**1.	Circuit intégré DS3231 :**
o	RTC avec oscillateur à quartz intégré, ce qui le rend extrêmement précis.
o	Précision : ± 2 ppm (parties par million), soit une dérive d'environ 1 minute par an.

**2.	Alimentation :**
o	Fonctionne entre 3.3V et 5V.
o	Une pile bouton CR2032 assure le maintien de l'heure en cas de coupure d'alimentation.

**3.	Communication I2C :**
o	Adresse I2C par défaut : 0x68.
o	Permet une communication simple avec les microcontrôleurs comme Arduino, ESP32, Raspberry Pi, etc.

**4.	Mémoire EEPROM :**
o	Certaines versions incluent une EEPROM 24C32 (32 Ko), qui peut stocker des données non volatiles.

**5.	Détection de température :**
o	Le DS3231 intègre un capteur de température interne avec une résolution de 0.25°C.

**6.	Sortie d'alarme :**
o	Le module permet de configurer des alarmes (alarme 1 et alarme 2) à des heures précises.
o	Sortie SQW : Génère des signaux carrés à des fréquences programmables (1Hz, 4kHz, etc.).

## Applications du module RTC HW-084 :

**1.	Horloges numériques :** Affichage de l'heure et de la date.
**2.	Enregistreurs de données (datalogger) :** Ajouter un horodatage précis aux mesures.
**3.	Automatisation :** Programmer des événements à des heures précises (alarmes, timers).
**4.	Projets IoT :** Maintenir l'heure sans accès à Internet.
**5.	Équipements portables :** Garder l'heure grâce à la batterie de sauvegarde.

## Avantages du HW-084 :
**•	Haute précision grâce au DS3231.**
**•	Facilité d'intégration grâce au bus I2C.**
**•	Autonomie avec la pile CR2032.**
**•	Polyvalence grâce à ses alarmes et sa sortie SQW.**

