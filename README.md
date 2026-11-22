# Fiche de Synthèse - Lab 1 : Protocole et Extraction de Données

Ce document résume les éléments définis dans le cadre du **Lab 1**. Il formalise le protocole d'une revue systématique (thème, problématique, PICOS) ainsi que les défis liés à la formulation des questions de recherche et à la justification des données à extraire.

## 1. Cadre Général du Lab

* **Thème :** Machine learning et télédétection pour la détection des maladies et du stress chez l'olivier (*Olea europaea L.*).
* **Problème scientifique :** Les études rapportent des précisions très élevées, mais la validation est souvent faible (répartitions aléatoires, étiquettes visuelles, tests de transfert rares) et l'infection est souvent confondue avec un déficit hydrique.
* **Énoncé du problème :** Dans quelle mesure le ML appliqué à l'imagerie (UAV, aéroportée et satellite) permet-il de détecter les maladies et le stress de l'olivier de manière fiable et transférable, et quelle est la solidité des preuves derrière ces performances ?
* **Objectif général :** Cartographier les plateformes, capteurs, cibles et algorithmes utilisés, et évaluer la rigueur de validation (V0-V5), les données de référence et l'état de préparation au déploiement (DRL1-5).
* **Cadre (PICOS) :**
  * **P (Population) :** Oliviers et vergers (*X. fastidiosa*, *V. dahliae*, maladies foliaires, stress hydrique).
  * **I (Intervention) :** ML/DL appliqué à l'imagerie aérienne et satellite.
  * **C (Comparaison) :** Comparaison descriptive entre plateformes et algorithmes.
  * **O (Outcome/Résultat) :** Performances, niveaux V (validation) et DRL (déploiement).
  * **S (Study/Étude) :** Études empiriques primaires.

## 2. Questions de Recherche (RQs)

* **RQ1 (Population) :** Quelles maladies et conditions de stress sont les plus étudiées, et avec quelles données de référence ?
* **RQ2 (Intervention - Capteurs) :** Quelles modalités de détection et stratégies de fusion sont utilisées, et comment sont-elles liées aux plateformes et aux cibles ?
* **RQ3 (Intervention - Algorithmes) :** Quelles méthodes d'IA sont utilisées (ML classique, DL, modèles fondateurs), et avec quelle explicabilité ?
* **RQ4 (Résultats et Design) :** Quels sont les jeux de données, les plans de validation et les métriques rapportées, et quel est le risque de biais ?
* **RQ5 (Analyse des lacunes) :** Quelles lacunes méthodologiques limitent la transférabilité, l'évaluation et le déploiement ?

---

## 3. Réponses aux Défis du Lab 1

### Défi 1 : Reformulation de la RQ
* **RQ de départ :** Quelles sont les approches d’IA utilisées pour la sécurité ?
* **RQ reformulée :** Quels algorithmes de machine learning et de deep learning sont utilisés pour détecter les vulnérabilités des applications Android dans les articles publiés entre 2020 et 2025, et sur quels jeux de données sont-ils évalués ?

### Défi 2 : Données à extraire et justification

Ce tableau détaille spécifiquement les données qui doivent être extraites des articles pour répondre aux RQs, ainsi que la raison pour laquelle chaque champ est nécessaire au protocole.

| RQ | Champ à extraire | Pourquoi il est nécessaire |
| :--- | :--- | :--- |
| **RQ1** | Cible et stade (précoce ou symptomatique) | Compter les maladies étudiées et distinguer la détection précoce de la symptomatique. |
| **RQ1** | Type de référence (qPCR, visuel, potentiel hydrique) | La fiabilité des labels conditionne celle de la détection. |
| **RQ2** | Plateforme, capteur, modalité, résolution | Permet de croiser plateforme / cible / capteur. |
| **RQ2** | Niveau de fusion | Savoir si la fusion se fait sur les données, les caractéristiques ou les décisions. |
| **RQ3** | Algorithmes et famille | Comparer le ML classique et le deep learning. |
| **RQ3** | Méthode d'explicabilité | Vérifier si le modèle s'appuie sur des signaux physiologiques. |
| **RQ4** | Plan de validation et unité de découpage | Attribuer le niveau V0 à V5 et repérer les fuites de données (*data leakage*). |
| **RQ4** | Métriques et valeurs | Juger si une métrique unique masque un échec d'évaluation. |
| **RQ5** | Données et code publics | Mesurer la reproductibilité de l'étude. |
| **RQ5** | Latence, matériel, coût, lien avec une décision | Attribuer le niveau DRL (déploiement opérationnel). |
