---
title: Laurent Mengal - Notes projet
projet: Immo Advens / My Rent Copilot
date: 2026-07-13
tags: [projet, immo, notes]
---

# Notes projet — Immo Advens / My Rent Copilot

## Concurrent repéré : Property Copilot (propertycopilot.io)

SaaS canadien (Vancouver, lancement juin 2026). Même positionnement que le projet de Laurent, mais marché canadien. Tunnel complet annonce → bail signé en 5 étapes : annonce unique (lien/QR à poster sur Kijiji, FB Marketplace, rentals.ca) → KYC + screening Equifax → dashboard de tri → baux numériques + suivi loyer (coming soon) → reporting du loyer à Equifax (coming soon).

Modèle éco : 1re propriété gratuite, $10/mois (2-3), $25/mois (4-10), custom au-delà ; gratuit pour les locataires ; screening à $25/rapport (= revenu principal, pas l'abonnement). Cible double : bailleurs, property managers, agents immo ET locataires.

Pourquoi c'est pertinent : valide le marché de Laurent, réutilise le mot « copilot » qu'il envisage comme nom, et matche son idée d'élargir à la vente ET la location. À la fois validation et quasi-concurrent (autre pays).

## Les 3 termes clés (résumé)

- **KYC** : vérification d'identité du candidat (pièce d'identité + selfie/liveness). Prouve qu'il est bien qui il dit être. Universel et facilement mockable pour une démo.
- **Screening** : enquête solvabilité + antécédents (score de crédit Equifax/TransUnion + background). Repose sur un système de crédit centralisé US/Canada.
- **Reporting crédit** : la plateforme déclare les loyers payés aux bureaux de crédit, ce qui fait monter le score du locataire. Feature très nord-américaine.

## Angle mort à signaler à Laurent (différences BE/CA)

Le système de score de crédit individuel centralisé (Equifax) n'existe pas en Belgique comme au Canada. Conséquence : sur les 3 briques de Property Copilot, seul le **KYC est transposable tel quel**. Le **screening** et le **reporting crédit** reposent sur ce scoring et sont à repenser complètement pour le marché belge (RGPD strict + Centrale des crédits BNB peu accessible aux bailleurs → plutôt preuves de revenus, contrat de travail, garant). À creuser avant de promettre ces features.

## Rappel scope MVP

Property Copilot = produit fini avec des années de dev. Le projet de Laurent = MVP-démo cliquable pour investisseurs pré-seed. Ne pas confondre. Les modules « vente + location » et l'IA avancée → roadmap V2, pas la démo. Garder un doc « idées V2 » séparé pour absorber le scope creep sans retarder la livraison.

## Naming

Le nom « copilot » plaît à Laurent, mais **propertycopilot.io existe déjà et est actif** (au Canada). À vérifier côté marque/domaine avant de s'engager sur un nom en « ...copilot ».
