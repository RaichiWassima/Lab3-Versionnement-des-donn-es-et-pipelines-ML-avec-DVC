# Lab 3 — Versionnement des données et pipelines ML avec DVC

## Contexte académique
**Université :** Université Chouaib Doukkali  
**École :** École Nationale des Sciences Appliquées d’El Jadida  
**Département :** Télécommunications, Réseaux et Informatique  
**Module :** MLOps  

**Filière :** SDIA  
**Niveau :** 2ᵉ Année  
**Année universitaire :** 2025/2026  

**Réalisé par :** Wassima RAICHI

---

## Objectif du lab
Ce lab a pour objectif de mettre en place le **versionnement des données, des modèles et des pipelines de Machine Learning à l’aide de DVC**, en complément de Git, afin d’assurer la **reproductibilité**, la **traçabilité** et la **collaboration** dans un contexte MLOps.

---

## Technologies utilisées
- Git (versionnement du code)
- DVC (versionnement des données et pipelines)
- Python
- CSV datasets
- Local DVC remote


---

## Étapes réalisées

### Étape 1 — Initialisation de DVC
Initialisation de DVC dans le projet afin d’intégrer le versionnement des données et artefacts ML en complément de Git.

---

### Étape 2 — Versionnement des données brutes
Le dataset brut `data/raw.csv` a été ajouté au suivi DVC, tandis que Git ne conserve que le fichier de métadonnées `raw.csv.dvc`, garantissant un dépôt Git léger.

---

### Étape 3 — Configuration d’un remote DVC
Un remote DVC local (`dvc_storage`) a été configuré pour stocker les données et modèles volumineux en dehors du dépôt Git.

---

### Étape 4 — Push des données vers le remote
Les données versionnées ont été envoyées vers le remote DVC afin de les rendre persistantes et partageables.

---

### Étape 5 — Simulation d’une collaboration
Le dataset a été supprimé localement puis restauré à l’identique via `dvc pull`, démontrant la capacité de DVC à gérer le partage et la reproductibilité des données.

---

### Étape 6 — Création d’un pipeline reproductible
Un pipeline complet (préparation, entraînement, évaluation) a été défini dans `dvc.yaml`, formalisant les dépendances, sorties et commandes du workflow ML.

---

### Étape 7 — Reproduction automatique du pipeline
Après modification d’une étape, `dvc repro` a permis de relancer uniquement les étapes impactées et de générer le fichier `dvc.lock`, garantissant une reproductibilité totale du pipeline.

---

## ✅ Résultats obtenus
- Versionnement fiable des données et modèles
- Pipeline ML entièrement reproductible
- Séparation claire entre code (Git) et données (DVC)
- Simulation réaliste d’un environnement collaboratif MLOps

---

## Conclusion
Ce lab démontre l’importance de DVC dans un pipeline MLOps moderne, en permettant un **contrôle précis des données**, une **reproductibilité complète des expériences**, et une **collaboration efficace** entre les différents acteurs d’un projet de Machine Learning.

