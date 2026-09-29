# Véhicule autonome de service

> Projet pluriannuel mené en équipe à Télécom Saint-Étienne (2026–2028).  
> **English version below.**

## 🇫🇷 Objectif

Développer un véhicule autonome capable de transporter du petit matériel entre différentes salles d'un établissement, avec navigation autonome et prise en compte des obstacles.

Le projet associe informatique, électronique, capteurs et robotique embarquée. Il est développé progressivement sur plusieurs années : les fonctions décrites comme perspectives ne sont pas présentées comme déjà implémentées.

## Principe

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
Perception → localisation/cartographie
        │
        ▼
Planification / déplacement
```

## Matériel retenu pour la plateforme actuelle

- Raspberry Pi ;
- châssis 4 roues Baron ROB0025 avec moteurs/encodeurs ;
- 2 × drivers moteurs Cytron MDD3A ;
- LiDAR LD19 ;
- IMU DFRobot Fermion BMI323 ;
- écran et périphériques Raspberry Pi.

## Développement par étapes

### Première phase

Les premiers travaux ont porté sur le déplacement du véhicule et le suivi de ligne. Une caméra a été testée, mais son utilisation s'est révélée plus complexe et moins prioritaire que les besoins de navigation/localisation.

### Phase actuelle

L'orientation actuelle privilégie :
- cartographie de l'environnement ;
- localisation/navigation avec LiDAR ;
- suivi d'une personne comme cas de test ;
- supervision du robot ;
- mode manuel encadré par des prérequis de sécurité et une visualisation de l'état du véhicule ;
- collecte de métriques.

### Perspectives

À terme, le projet vise une chaîne plus complète avec commande depuis une application, choix de destination, planification de trajet, évitement d'obstacles et supervision web.

## Contexte équipe

Le projet est réalisé en groupe et s'étend de mars 2026 à juin 2028. Ce dépôt documente donc le système et son évolution sans attribuer à une seule personne le travail collectif.

## État du dépôt

**Work in progress / Projet en cours.**

Le projet est **en cours de développement**. Ce README distingue volontairement les éléments testés/choisis des fonctionnalités prévues afin de ne pas présenter la roadmap comme un résultat déjà obtenu.

---

# 🇬🇧 Autonomous Service Vehicle

Multi-year team project at Télécom Saint-Étienne (2026–2028) focused on building an autonomous vehicle for transporting small equipment between rooms.

The platform combines a Raspberry Pi, four-wheel chassis with encoders, Cytron motor drivers, an LD19 LiDAR and a BMI323 IMU.

Development is incremental. Early work focused on vehicle motion and line following. The current direction prioritizes LiDAR-based mapping/navigation, person-following experiments, supervision and system metrics.

Future work includes destination requests through an application, path planning, obstacle avoidance and web-based supervision.

This is a **work in progress**. Planned features are deliberately separated from implemented/tested elements.
