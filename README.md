# Portfolio – FATIMA EZZAHRAE EL ANSARI
Ingénieure en Électronique Embarquée et Systèmes Intelligents
Projets en systèmes automobiles (ADAS), robotique et conception de circuits intégrés —Cadence Virtuoso, MATLAB/Simulink

## 🏭 Modélisation et Maintenance Prédictive du Broyeur Vertical BK4 – Stage de Fin d'Études (Holcim Maroc)

Le broyeur vertical BK4 joue un rôle essentiel dans la continuité de la production au sein de la cimenterie de Fès :
toute défaillance de cet équipement peut entraîner un arrêt de la ligne de production et des pertes financières
importantes. C'est dans ce contexte que j'ai réalisé mon projet de fin d'études chez Holcim Maroc, avec pour
objectif de comprendre le fonctionnement global du broyeur et de développer un outil d'aide à la maintenance
prédictive.

**🔧 Modélisation du système**

Chaque sous-système du broyeur — le moteur, le réducteur, le séparateur et le système hydraulique — a été modélisé
sous MATLAB/Simulink, afin de reproduire fidèlement le fonctionnement réel du broyeur BK4.

**📡 Capteurs virtuels**

En l'absence d'accès à une base de données de capteurs réels, des capteurs virtuels ont été implémentés via des
blocs MATLAB Function, permettant de calculer les grandeurs critiques du broyeur : température, vibrations et
position des galets.

**🧠 Génération des données et modèle d'intelligence artificielle**

À partir des seuils d'alarme et d'arrêt fournis par l'usine, trois états de fonctionnement ont été générés : sain,
défaut faible et défaut grave, exportés sous forme de fichiers CSV. Ces données ont ensuite servi à entraîner un
modèle d'intelligence artificielle (Random Forest), combinant une comparaison directe aux seuils et une analyse
de tendance de l'évolution des grandeurs critiques, afin de prédire l'état de fonctionnement du broyeur.

**🖥️ Interface de prédiction**

Une interface de prédiction a été conçue pour restituer, en temps réel, l'état du broyeur et l'évolution de ses
grandeurs critiques (température, vibrations), facilitant ainsi la détection précoce d'anomalies.

🛠️ Outils utilisés : MATLAB | Simulink | MATLAB Function | Python | Random Forest | Machine Learning


<img width="945" height="496" alt="ACC" src="https://github.com/user-attachments/assets/b8d747ac-2615-480e-b244-c46c7ce8bbff" />
<img width="945" height="492" alt="ACC1" src="https://github.com/user-attachments/assets/5a74d6d8-24f4-417c-b26b-16cd4bc7818d" />

## 🚗 Adaptive Cruise Control (ACC) – MATLAB/Simulink & Stateflow

Dans le cadre d'un projet de modélisation des systèmes automobiles, j'ai réalisé la conception d'un système
Adaptive Cruise Control (ACC) permettant d'adapter automatiquement la vitesse du véhicule en fonction de la
présence d'un véhicule précédent et de la distance de sécurité.

La logique de fonctionnement a été implémentée avec Stateflow à travers trois états principaux : **Cruise**,
**Follow** et **Braking**.

- **Cruise** : en l'absence de véhicule détecté, le système maintient la vitesse cible définie par le conducteur.
- **Follow** : lorsqu'un véhicule est détecté, le système ajuste la vitesse afin de respecter la distance de sécurité.
- **Braking** : lorsque la distance devient critique, le système déclenche un freinage d'urgence accompagné d'une alerte.

Les transitions entre les différents états sont définies à partir de conditions telles que la détection d'un
véhicule, la vitesse du véhicule ego et la distance mesurée. Cette approche permet de représenter clairement le
comportement dynamique et décisionnel de l'ACC avant son intégration dans le modèle Simulink.

Une fois la logique validée en simulation, un test **HIL (Hardware-in-the-Loop)** a été réalisé sur carte
**Pixhawk 2.4.8**,  afin de vérifier le comportement du code généré directement sur la cible embarquée. L'état actif du système (Cruise / Follow / Braking) est restitué par la
configuration d'une LED sur la carte.

🛠️ Outils utilisés : MATLAB | Simulink | Stateflow | Model-Based Design | Test HIL (Pixhawk 2.4.8)

![Machine à états ACC](ACC.png)
![Configuration LED - Test HIL Pixhawk](ACC1.png)

## 🚁 Simulation d'un Quadrirotor (MATLAB/Simulink)
Modélisation et contrôle d’un quadrirotor avec régulateurs PID et simulation de ses performances.

## 🚦 Système de Feux Tricolores – Stateflow
Modélisation et validation d’un système de feux de circulation en temps réel via les tests MIL, SIL, PIL et HIL.



## 🔌 Conception de circuits intégrés – Cadence Virtuoso 180nm
Simulation de circuits au niveau transistor, incluant amplificateurs opérationnels, miroirs de courant et portes
logiques numériques (NAND, XOR, inverseurs) avec la technologie Cadence 180nm, vérification DRC/LVS.

## 🔋 Système de gestion de batterie (BMS) – Véhicule électrique
Modélisation et analyse dynamique d'une batterie lithium-ion.

## 🤖 Robot suiveur de ligne STM32
Robot autonome, suivi de ligne et détection d'obstacles en temps réel.
