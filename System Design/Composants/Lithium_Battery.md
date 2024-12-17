# Lithium Battery Charging Board

Le module Lithium Battery Charging Board (souvent appelé TP4056) est un circuit de charge compact pour batteries lithium-ion, telles que les 18650. Ce module est très utilisé dans les projets DIY pour charger des batteries rechargeables grâce à une interface Micro-USB.
________________________________________
**Caractéristiques principales du module TP4056 :**
1.	Circuit intégré principal :
o	TP4056, un contrôleur de charge linéaire pour batteries lithium-ion.
o	Supporte une charge en CC (Courant Constant) / CV (Tension Constante).
2.	Alimentation d'entrée :
o	Micro-USB : Permet d'alimenter le module depuis un chargeur USB standard.
o	Tension d'entrée : 4.5V à 5.5V (classique pour les ports USB).
3.	Batterie supportée :
o	Batteries lithium-ion rechargeables de 3.7V nominale (par exemple, 18650).
o	Tension de charge maximale : 4.2V (pleinement chargée).
4.	Courant de charge :
o	Le courant de charge maximal par défaut est 1A.
o	Résistance programmée pour ajuster le courant de charge.
5.	Protection intégrée :
o	Protection contre les surtensions.
o	Protection contre les décharges profondes.
o	Protection contre les courts-circuits.
6.	Indicateurs LED :
o	LED rouge : La batterie est en cours de charge.
o	LED verte : La batterie est complètement chargée.
7.	Broches supplémentaires :
o	BAT+ et BAT- : Connexion aux bornes positive et négative de la batterie.
o	OUT+ et OUT- : Sortie pour alimenter un autre circuit tout en chargeant.
________________________________________
**Précautions d'utilisation :**
1.	Utilisez des batteries en bon état :
o	Les batteries lithium-ion peuvent être dangereuses si elles sont endommagées ou mal utilisées.
2.	Respectez la polarité :
o	Connecter les bornes BAT+ et BAT- correctement pour éviter les courts-circuits.
3.	Ventilation :
o	Le module peut chauffer pendant la charge. Assurez-vous d'une bonne ventilation.
4.	Courant de charge :
o	Par défaut, le courant est fixé à 1A. Si vous utilisez des batteries plus petites (par exemple 500mAh), ajustez le courant en changeant la résistance RPROG sur le module.
________________________________________
**Exemple d'application avec ESP32 :**
Vous pouvez utiliser ce module pour alimenter un ESP32 avec une batterie 18650. Voici les étapes :
1.	Charge de la batterie :
o	Utilisez le module TP4056 pour charger la batterie lithium-ion.
2.	Connexion à l'ESP32 :
o	Connectez la sortie OUT+ (positive) et OUT- (négative) du TP4056 à l'entrée Vin (ou 5V) et GND de l'ESP32.
3.	Régulation de tension :
o	L'ESP32 peut fonctionner avec une tension de 3.3V, donc vous pouvez utiliser un régulateur de tension si nécessaire.
________________________________________
**Avantages du module TP4056 :**
1.	Compact et économique.
2.	Interface Micro-USB facile d'utilisation.
3.	Protection intégrée pour une charge sûre.
4.	Compatible avec de nombreuses batteries lithium-ion (18650, 14500, etc.).

