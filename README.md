# 🚀 Projet de Contrôle GPIO STM32

Ce projet met en œuvre un driver GPIO bas niveau pour les microcontrôleurs STM32, permettant la configuration
et le contrôle des broches GPIO des différents ports (A à K) de la carte STM32F407 Discovery. 🛠️Il illustre 
les principes fondamentaux de la programmation embarquée à travers la manipulation directe des registres matériels
et l’utilisation d’opérations bit à bit (masquage, décalage, écriture sélective).

# 📁 Structure du projet

main.c : Programme principal qui initialise et contrôle les broches GPIO.

gpio.c : Implémentation des fonctions d’initialisation, de lecture et d’écriture sur les ports GPIO.

gpio.h : Fichier d’en-tête contenant les déclarations des fonctions et les définitions de macros nécessaires.

# 📂 Détails des fichiers
🔹 main.c
Point d’entrée du projet.
Ce fichier contient la fonction main() qui gère l’initialisation des GPIO et leur comportement selon le scénario défini (activation de LED, lecture d’un bouton, etc.).

🔹 gpio.c
Implémente les principales fonctions du driver GPIO :

`GPIO_ClockEnable(unsigned int *gpio_x)`: Active l’horloge du port GPIO spécifié.

GPIO_DeInit(unsigned int *gpio_x) : Réinitialise le port GPIO.

GPIO_Init(unsigned int *gpio_x, char Mode, char typeOutput, short int pin) : Configure le mode et le type de sortie d’une broche.

GPIO_ReadInputDataBit(unsigned int *gpio_x, unsigned short int GPIO_Pin) : Lit l’état logique d’une broche donnée.

GPIO_ReadInputData(unsigned int *gpio_x) : Lit l’ensemble des bits d’un port GPIO.

GPIO_WriteBit(unsigned int *gpio_x, unsigned short int GPIO_Pin, char BitVal) : Modifie l’état d’une broche (mise à 1 ou à 0).

GPIO_Write(unsigned int *gpio_x, unsigned short int PortVal) : Écrit une valeur sur tout le port GPIO.

🔹 gpio.h
Contient les prototypes des fonctions et les définitions de macros nécessaires à la configuration et à la manipulation des GPIO.

# 🧭 Utilisation
1. Cloner le dépôt sur votre machine locale :

2. Ouvrir le projet dans votre environnement de développement (ex. IAR Embedded Workbench ou STM32CubeIDE).

3. Compiler et téléverser le code sur la carte STM32F407 Discovery.

4. Observer le comportement des GPIO (par exemple, allumage de LED ou lecture d’un bouton poussoir).

# ⚙️ Technologies utilisées
🧩 Langage C embarqué

⚡ STM32F407 Discovery Board

💻 IAR Embedded Workbench

🔍 Opérations bit à bit (masquage, décalage, écriture)

# 🤝 Contribution
Les contributions sont les bienvenues !
N’hésitez pas à ouvrir une issue ou à proposer une pull request pour améliorer le projet.

# 📜 Licence
Ce projet est distribué sous licence MIT.
Consultez le fichier LICENSE pour plus d’informations.

# 📧 Contact
Pour toute question, suggestion ou collaboration, vous pouvez me contacter via :

Email : baker.essid98@gmail.com

LinkedIn : [Baker Essid](https://www.linkedin.com/in/baker-essid-b27b311b9/overlay/about-this-profile/?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base%3Bgh8EYV5MTL%2BDU11rWtcMPA%3D%3D)

Je répondrai avec plaisir à vos messages et discussions autour du projet.


