# Véhicule autonome de service

> Projet pluriannuel en équipe à Télécom Saint-Étienne (2026–2028) — **Work in progress**.  
> **English version below.**

## 🇫🇷 Objectif

Développer progressivement un véhicule capable de transporter du petit matériel entre différentes salles. Le projet combine Raspberry Pi, motorisation, encodeurs et capteurs ; les fonctions d'autonomie avancées appartiennent aux phases suivantes du projet.

## État actuel

### Réalisé / testé

- première phase de déplacement et **suivi de ligne** ;
- essai d'une caméra pour cette première approche ;
- définition de la plateforme matérielle et sélection des composants pour la suite du projet.

### En développement

- intégration de la nouvelle plateforme Raspberry Pi ;
- exploitation des encodeurs, du LiDAR LD19 et de l'IMU BMI323 ;
- préparation des briques nécessaires à la localisation/cartographie.

### Prévu

Les éléments suivants sont des **objectifs de roadmap et ne sont pas présentés comme fonctionnels aujourd'hui** :
- cartographie et localisation complètes ;
- navigation autonome et évitement d'obstacles ;
- suivi de personne comme scénario expérimental ;
- mode manuel avec visualisation de l'état du robot ;
- collecte de métriques et supervision ;
- application de commande et supervision web.

## Plateforme matérielle retenue

- Raspberry Pi ;
- châssis 4 roues Baron ROB0025 avec moteurs et encodeurs ;
- 2 × drivers moteurs Cytron MDD3A ;
- LiDAR LD19 ;
- IMU DFRobot Fermion BMI323 ;
- écran et périphériques Raspberry Pi.

## Architecture cible

```text
Commande / destination
        │
        ▼
 Raspberry Pi
 contrôle embarqué
        │
   ┌────┴────┐
   ▼         ▼
Capteurs   Moteurs
LiDAR      + encodeurs
IMU
        │
        ▼
Localisation / cartographie
        │
        ▼
Navigation / déplacement
```

Ce schéma représente l'**architecture visée**, pas l'état fonctionnel actuel.

## Contexte

Projet pédagogique réalisé en groupe et planifié de mars 2026 à juin 2028. Le dépôt documente l'évolution du système sans attribuer à une seule personne le travail collectif.

À ce stade, le dépôt est principalement documentaire : le code des futures fonctions de navigation n'y est pas présenté comme disponible.

---

# 🇬🇧 Autonomous Service Vehicle

Multi-year team project at Télécom Saint-Étienne (2026–2028) — **work in progress**.

### Implemented / tested

Early vehicle-motion and line-following work, including an initial camera experiment, plus selection of the hardware platform for the next phase.

### In progress

Integration of the Raspberry Pi platform, motor encoders, LD19 LiDAR and BMI323 IMU, and preparation of the building blocks required for localization and mapping.

### Planned

Full mapping/localization, autonomous navigation, obstacle avoidance, person-following experiments, manual supervision, metrics and a web control interface are **roadmap items, not completed features**.

**Target hardware:** Raspberry Pi · Baron ROB0025 chassis · 2× Cytron MDD3A · LD19 LiDAR · BMI323 IMU

This repository currently focuses on project documentation and roadmap clarity rather than claiming unavailable navigation source code.
