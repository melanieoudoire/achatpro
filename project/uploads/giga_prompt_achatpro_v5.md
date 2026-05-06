# 🎯 GIGA-PROMPT — Suite Achats IA "AchatPro"

> **Mode d'emploi** : copie-colle l'intégralité de ce prompt dans une nouvelle conversation Claude (avec artifacts activés). Claude générera une maquette React interactive complète. Tu pourras ensuite itérer en disant *"développe maintenant le module Contrats"*, *"ajoute des données sur le dashboard"*, etc.

> **🌐 Partage public** : la maquette générée est conçue pour être **partageable par simple lien** à n'importe qui (jury, collègues, direction) sans installation ni compte. Trois options s'offrent à toi (détaillées plus bas) :
> 1. **Lien Claude natif** — clique sur "Publish" dans l'artifact, partage le lien (le plus simple).
> 2. **Déploiement Vercel** — URL propre type `achatpro.vercel.app` (recommandé pour la soutenance).
> 3. **Netlify Drop** — drag & drop du dossier build, lien instantané.

---

## 🧭 RÔLE & MISSION

Tu es **un expert UX/UI senior et architecte produit SaaS B2B**. Tu vas concevoir et coder la **maquette interactive complète** d'une plateforme nommée **"AchatPro"** : un copilote IA pour la fonction Achats d'entreprise.

Ton livrable doit être :
- **Une application React mono-fichier** (artifact unique, navigation par sidebar, état local)
- **Visuellement premium, élégante, naturelle** (ambiance vert sauge / beige / crème, niveau Notion / Linear mais plus organique)
- **Démontrable lors d'une soutenance** (parcours fluide, données mock crédibles, micro-animations)
- **Évolutive en interne** (architecture claire, composants réutilisables)

## 📋 CONTEXTE PROJET

- **Auteure & utilisatrice de démo** : **Mélanie Oudoire** (acheteuse) — son nom doit apparaître partout dans la maquette : profil sidebar, salutations ("Bonjour Mélanie"), signatures d'emails, auteure de prompts personnalisés, etc.
- **Utilisateurs cibles** : équipe Achats (acheteurs, responsables, direction).
- **Promesse produit** : *"Toute la fonction Achats, augmentée par l'IA, de A à Z, en un seul endroit."*
- **Différenciateurs clés** :
  1. Couvre **TOUT** le processus Achats (pas un silo, une suite intégrée).
  2. Les **prompts experts métier** sont **visibles, éditables et versionnés** (transparence + personnalisation).
  3. Esthétique inattendue (vert sauge / nature) → mémorable face à la concurrence corporate-bleu.

---

## 🎨 DIRECTION ARTISTIQUE — IMPORTANT

### Palette (à respecter strictement)
- **Fond principal** : `#F5F1EA` (blanc cassé / lin)
- **Cartes principales** : `#FAF7F2` (crème) avec ombre très douce
- **Cartes secondaires** : `#E8DFD3` (beige sable)
- **Vert sauge clair** : `#A8B89B` (couleur signature, fonds de section, badges)
- **Vert sauge foncé** : `#7A8B6F` (boutons primaires, accents)
- **Vert profond** : `#3D4A3D` (titres, textes forts)
- **Texte courant** : `#5A5A52` (gris-vert chaud)
- **Doré subtil** : `#C9A961` (highlights, badges premium, étoiles)
- **Rouge terre** : `#B85C3E` (alertes, risques) — **utilisé avec parcimonie**
- **Mode sombre optionnel** : fond `#2A2D26`, cartes `#363A33`, accents inchangés

### Typographie
- **Titres** : `'Playfair Display', 'DM Serif Display', serif` (élégant, légèrement classique)
- **Corps & UI** : `'Inter', 'DM Sans', sans-serif`
- **Tailles** : titres généreux (32-48px sur les pages), corps 14-16px, micro-texte 12-13px.

### Style visuel
- **Border-radius** généreux : 16px sur cartes, 12px sur boutons, 24px sur sections hero.
- **Ombres** : très douces (`0 2px 12px rgba(60, 70, 60, 0.06)`), jamais agressives.
- **Espacement** : généreux, beaucoup de white space.
- **Boutons** : arrondis, vert sauge foncé pour primaire, contour vert pour secondaire, ghost pour tertiaire.
- **Iconographie** : line-art fine (Lucide React), traits ~1.5px.
- **Illustrations** : touches botaniques discrètes (feuilles SVG en filigrane dans certains coins/sections hero), jamais envahissantes.
- **Micro-animations** : fade-in subtils, hover doux (translateY -2px, ombre légèrement accentuée).
- **Graphiques** : palette dérivée de la charte (vert sauge → vert profond → doré → terre), jamais les couleurs Recharts par défaut.

### Inspirations à mixer
Notion (clarté), Linear (densité d'info maîtrisée), Stripe Dashboard (data viz), Aesop ou Le Labo (élégance naturelle).

---

## 🏗️ ARCHITECTURE DE L'APPLICATION

### Layout global
- **Sidebar gauche fixe** (240px) :
  - Logo + nom **"AchatPro"** en haut (typo serif, petite icône feuille stylisée)
  - Navigation des modules (groupés par section : *Pilotage*, *Opérations*, *Analyse*, *Conformité*, *Configuration*)
  - Section "🪄 Prompts Library" mise en valeur en bas
  - Profil utilisateur en bas : avatar (initiales **MO**) + nom **"Mélanie Oudoire"** + rôle *"Responsable Achats"*
- **Topbar** (60px) : fil d'Ariane, barre de recherche globale avec placeholder *"Rechercher ou demander à l'IA…"*, cloche notifications, toggle dark/light.
- **Zone principale** : contenu du module actif, padding généreux.
- **Panneau IA latéral droit** (rétractable, 360px) : assistant contextuel toujours accessible (chat + suggestions d'actions liées au module en cours).

### Navigation — Modules à intégrer

**🏠 PILOTAGE**
1. Tableau de bord (accueil) — KPI globaux + alertes IA + raccourcis
2. **Veille & Alertes Marchés** ⭐ NOUVEAU (matières premières, géopolitique, événements monde impactant les achats)
3. **Plan Annuel des Achats (PAA)** 🆕 (vision stratégique année, jalons, budgets prévisionnels)

**🧭 OPÉRATIONS**
4. **Demandes d'Achat (DA)** 🆕 (saisie utilisateurs, validation, transformation en BdC)
5. Processus Achats A→Z (assistant pas-à-pas)
6. Assistant Emails IA
7. **Comparateur d'offres** ⭐ NOUVEAU
8. Sourcing fournisseurs & prospects
9. Workflows d'approbation

**💰 PILOTAGE FINANCIER**
10. **Budget & Engagements** 🆕 (suivi budgétaire temps réel, engagements, prévisions)

**📊 ANALYSE**
11. Dashboards & Reporting (style Power BI)
12. Suivi des dépenses & KPI ⭐ NOUVEAU (Pareto, ABC, KPI)
13. Calculateur TCO
14. Analyse des coûts (Cost Analytics)
15. Évaluation fournisseurs

**📑 CONTRACTUEL**
16. Analyse de contrats
17. Rédaction de contrats
18. **GED Achats** 🆕 (coffre-fort contrats, attestations, certifications, alertes expiration)

**🛡️ RISQUES & CONFORMITÉ**
19. Gestion des risques fournisseurs
20. RSE / ESG / Conformité

**⚙️ CONFIGURATION**
21. Intégrations
22. Base de connaissances
23. 🪄 **Prompts Library** (section signature)

**🔮 ROADMAP** (section visible mais non-cliquable / "Bientôt disponible")
Afficher dans la sidebar tout en bas, dans une section discrète avec un badge *"Phase 2 — Q3 2026"*. Items non-cliquables, juste visibles pour montrer la vision produit :
- Catalogue & e-procurement (PunchOut)
- Module Négociation dédié (BATNA, ZOPA, simulateur)
- Litiges & non-conformités
- Stocks & approvisionnements
- Onboarding fournisseur (KYC/conformité)
- Savings Tracker dédié
- Portail fournisseur (espace externe)
- Application mobile (mode terrain)

---

## 📦 SPÉCIFICATIONS DÉTAILLÉES PAR MODULE

### 1. 🏠 Tableau de bord (page d'accueil) — VERSION ENRICHIE

**Hero d'accueil personnalisé**
- Titre serif : *"Bonjour Mélanie, voici votre journée Achats"* + date du jour formatée en français.
- Sous-titre : météo IA du jour (*"3 alertes critiques · 5 opportunités d'économie · 2 AO à finaliser cette semaine"*).
- Illustration botanique discrète en filigrane à droite.

**Bandeau de KPI principaux** (4 cards)
- Économies réalisées YTD (€ + % vs objectif)
- Contrats actifs (nombre + alerte renouvellements à venir)
- Fournisseurs à risque (nombre + sévérité)
- Tâches en attente (nombre + raccourci)

**🚨 Bloc "Alertes IA" — REFONTE COMPLÈTE (élément central de la page)**

Sous-onglets internes avec compteurs : **Tout (12)** · **💰 Opportunités d'économies (5)** · **📋 Suivi AO (3)** · **📦 Suivi OA / Commandes (4)** · **⚠️ Risques (2)**

Chaque alerte = une **carte enrichie** avec :
- Icône typée + sévérité (info / important / critique / opportunité) en bandeau coloré.
- Titre court accrocheur.
- Description en 2-3 lignes avec **chiffres clés en gras** (montants, pourcentages, dates).
- Source de la détection IA (*"Détecté par : analyse des commandes 2024-2025"*).
- 2-3 **actions cliquables** : *"Voir le détail"*, *"Lancer la négo"*, *"Contacter le fournisseur"*, *"Reporter"*, *"Marquer traitée"*.
- Tag de catégorie + estimation d'impact financier.
- Score de confiance IA (ex: *"Confiance : 87%"*).

**💰 Sous-onglet "Opportunités d'économies" — au moins 5 alertes mockées détaillées :**
1. *"Consolidation possible : 3 fournisseurs de fournitures de bureau livrent vers Lyon. **Économie estimée : 18 400 €/an** en regroupant chez un seul. Confiance 91%."* → Actions : Voir analyse / Lancer consultation / Reporter
2. *"Renégociation contrat Veolia (eau industrielle) : indice de référence ICHT-IME a baissé de 4,2% sur 6 mois mais le prix n'a pas été révisé. **Marge négo : ~12 800 €/an**."* → Actions : Préparer la négo / Voir l'historique
3. *"Décathlon Pro : volume d'achats EPI > 50k€/an, le tarif "Compte Entreprise" est applicable. **Économie : 8% soit ~4 200 €**."* → Actions : Demander le passage / Voir conditions
4. *"Catégorie IT : 14 licences Adobe inactives depuis 90 jours. **Économie immédiate : 9 660 €/an** en résiliant."* → Actions : Voir les utilisateurs / Lancer résiliation
5. *"Maintenance machines Schneider : appel d'offres potentiel — 4 prestataires régionaux non consultés depuis 2022. **Marge estimée : 7-15%**."* → Actions : Lancer un AO / Identifier des prestataires

**📋 Sous-onglet "Suivi AO" (Appels d'Offres) — REFONTE COMPLÈTE :**

Tableau / cards des AO en cours, chacun avec :
- Référence AO + intitulé (ex: *"AO-2026-014 — Prestation nettoyage tertiaire Lyon/Villeurbanne"*).
- **Phase actuelle** dans le cycle visuel : Préparation CDC → Diffusion → Réception offres → Analyse → Soutenance fournisseurs → Choix → Notification → Contractualisation.
- **Date butoir** + jours restants (badge rouge si <5 jours).
- **Nombre de candidats** : invités / ayant répondu / qualifiés.
- **Montant estimé** du marché.
- **Alerte IA contextuelle** : *"⚠️ Seulement 2 réponses sur 6 invités à J-3. Recommandation : relancer aujourd'hui ou prolonger délai de 5 jours."*
- Actions : Voir le dossier / Relancer les fournisseurs / Voir analyse comparative / Notifier le choix.

Mocker 3 AO :
- AO en phase **Réception offres** avec alerte de relance.
- AO en phase **Analyse comparative** avec lien direct vers le Comparateur d'offres.
- AO en phase **Notification** avec checklist de finalisation.

**📦 Sous-onglet "Suivi OA" (Ordres d'Achat / Commandes) — REFONTE COMPLÈTE :**

Tableau / cards des commandes en cours nécessitant attention, chacune avec :
- N° de commande + fournisseur + date émission + date livraison prévue.
- **Statut visuel** : Émise / Confirmée / En production / Expédiée / Reçue partiellement / Reçue / Facturée / Soldée.
- **Alerte IA** spécifique :
  - *"📅 Livraison prévue dans 2 jours non confirmée par le fournisseur — risque de retard."*
  - *"📦 Réception partielle : 80/100 unités reçues, écart à investiguer."*
  - *"💸 Facture reçue 12% au-dessus du BdC — vérifier conditions."*
  - *"🕒 Délai dépassé de 7 jours — pénalités contractuelles applicables (1,2% / semaine)."*
- Actions : Relancer le fournisseur / Saisir une réception / Contester la facture / Appliquer pénalités.

Mocker 4 OA avec ces 4 cas distincts.

**⚠️ Sous-onglet "Risques" — 2 alertes mockées :**
1. *"Fournisseur Lafarge Ciments : dégradation note Ellisphere passée de A à B+ en mars 2026. Dépendance : 28% catégorie BTP."* → Actions : Voir fiche risque / Activer plan B
2. *"Matière première : indice cuivre +14% sur 30 jours — impact estimé sur contrats indexés : +€34k/an."* → Actions : Voir contrats indexés / Renégocier

**Bloc "Recommandations IA du jour"**
3 cartes : *Préparer la QBR Schneider (planifiée jeudi)*, *Benchmarker le fournisseur SECO Tools sur la catégorie outillage*, *Réviser le scoring ESG du portefeuille (CSRD échéance Q2)*.

**Mini-graphique de tendance des dépenses** (sparkline élégante 12 mois).

**Raccourcis vers actions fréquentes**
Cards cliquables : *Nouveau RFQ*, *Comparer des offres*, *Analyser un contrat*, *Calculer un TCO*, *Lancer un sourcing*.

**Citation en pied de page** (italique, vert sauge) : *"L'achat n'est plus une fonction support. C'est un levier stratégique."*

### 2. 🌍 Veille & Alertes Marchés ⭐ NOUVEAU MODULE

**Objectif** : donner à l'acheteuse une **vision temps réel** de l'environnement extérieur qui impacte ses achats — sans avoir à scroller la presse économique.

**Layout général**
- Hero compact : *"Aujourd'hui sur les marchés"* + 3 indicateurs phares en gros (cuivre, brent, fret maritime) avec variation 24h en couleur (vert / rouge terre).
- 4 sous-sections dans des onglets ou empilées : Matières premières · Énergie & Fret · Géopolitique & Réglementaire · Mes alertes personnalisées.

**📈 Section "Matières premières"**
- Grille de cartes par matière : Cuivre, Acier, Aluminium, Plastiques (HDPE, PP), Bois, Coton, Café, Lithium, Pétrole brut, Gaz naturel, Blé.
- Chaque carte : nom + cours actuel (USD/t) + variation 24h / 30j / YTD + mini-sparkline + **bouton "Voir contrats impactés"** (lien vers les contrats indexés sur cette matière).
- Cliquer une carte ouvre un panneau détail : graphique sur 12 mois, **commentaire IA** (*"Le cuivre a bondi de 14% en 30j suite aux annonces de réduction de production au Chili. Vos 4 contrats indexés cuivre subiront une revalorisation au prochain échéancier."*).

**⚡ Section "Énergie & Fret"**
- Indicateurs : Électricité (€/MWh France), Gaz TTF, Pétrole Brent, Fret maritime (Drewry WCI Shanghai-Rotterdam), Fret routier (CNR France).
- Idem cartes + bouton "Impact sur mes coûts logistiques estimé : +X €/mois".

**🌐 Section "Géopolitique & Réglementaire" — événements monde impactant les achats**
- Fil d'actualités curé par IA, chaque item = card avec :
  - **Pictogramme** zone géo (drapeau/continent).
  - **Titre** : ex: *"Nouvelles sanctions UE sur l'aluminium russe (entrée en vigueur 15 juin 2026)"*.
  - **Niveau d'impact** : 🟢 Surveillance / 🟡 À analyser / 🔴 Action requise.
  - **Résumé IA** en 3 lignes.
  - **Catégories impactées** (badges) : Métaux, BTP, Automotive…
  - **Vos fournisseurs concernés** (chips cliquables si match).
  - Source + date + bouton "Voir l'article complet".

Mocker au moins 6 événements variés et réalistes :
- Sanctions / embargos.
- Catastrophes naturelles affectant la supply chain.
- Évolutions réglementaires (CBAM, CSRD, devoir de vigilance).
- Tensions géopolitiques (Mer Rouge, Taïwan, Mexique…).
- Grèves / conflits sociaux logistiques.
- Évolution de taux de change majeurs (USD, CNY).

**🔔 Section "Mes alertes personnalisées"**
- Liste des alertes configurées par Mélanie : *"Cuivre +5% sur 7j"*, *"Toute news fournisseur Lafarge"*, *"Réglementation CSRD"*.
- Bouton **"+ Créer une alerte"** → modal avec choix : matière/indice/zone géo/fournisseur/réglementation, seuil, fréquence (temps réel / quotidien / hebdo).
- Historique des alertes déclenchées dans la semaine.

**Tip premium** : encart en bas *"💡 L'IA détecte un signal faible : 3 articles en 48h mentionnent une potentielle pénurie de magnésium en Europe — voulez-vous être alerté(e) ?"*

---

### 3. 🗓️ Plan Annuel des Achats (PAA) 🆕 NOUVEAU MODULE

**Objectif** : permettre à Mélanie de **piloter stratégiquement l'année** — quels marchés à lancer, à renouveler, à benchmarker, avec quel budget et quelle priorité. C'est le **document directeur** de toute direction Achats mature, attendu en début d'exercice.

**Layout général** : 3 onglets internes → **Vue Roadmap** · **Vue Tableau** · **Vue Synthèse executive**

**🛣️ Onglet 1 — Vue Roadmap (timeline visuelle)**

- **Frise temporelle horizontale** sur 12 mois (janvier → décembre 2026), avec swimlanes par catégorie d'achat (IT, BTP, Prestations, MRO, Énergie, Marketing, Logistique, Mobilier, Véhicules, Frais généraux).
- Chaque **chantier achat** = un **bandeau coloré** sur la timeline avec :
  - Intitulé court (*"Renouvellement contrat-cadre IT poste de travail"*).
  - Type : 🟢 Nouveau / 🔵 Renouvellement / 🟡 Benchmark / 🟠 Renégociation.
  - Phase actuelle (cadrage, sourcing, AO, négo, contractualisation, finalisée).
  - Budget cible.
  - Pilote (initiales avec mini avatar).
  - Statut : ✅ À temps / 🟡 En tension / 🔴 En retard.
- **Jalons clés** marqués par des losanges dorés (date butoir CDC, date diffusion AO, date notification, signature).
- **Drag horizontal** pour décaler une initiative (mode édition).
- **Filtres** en haut : par catégorie, par pilote, par statut, par type.
- **Ligne verticale "aujourd'hui"** rouge terre pour repère temporel.
- Bouton **"+ Nouvelle initiative"** ouvre un formulaire complet.

**📋 Onglet 2 — Vue Tableau (toutes les initiatives)**

- Tableau exhaustif triable / filtrable :
  - Colonnes : Réf · Intitulé · Catégorie · Type · Pilote · Date début · Date fin · Budget cible · Économie attendue · Phase · Statut · Priorité (1-5) · Actions.
- Mocker au moins **15 initiatives** réalistes réparties sur l'année (mix de tailles/catégories) :
  - *"AO-2026-01 — Contrat-cadre IT poste de travail"* (BTP, Renouvellement, Q1, 2,4 M€)
  - *"AO-2026-02 — Prestation nettoyage tertiaire"* (Prestations, Renouvellement, Q1, 480 k€)
  - *"AO-2026-03 — Flotte véhicules de service (LLD)"* (Véhicules, Renouvellement, Q2, 1,2 M€)
  - *"AO-2026-04 — Énergie HTA 2027-2030"* (Énergie, Renouvellement, Q2, 6,8 M€)
  - *"AO-2026-05 — Mobilier ergonomique 3 sites"* (Mobilier, Nouveau, Q2, 320 k€)
  - *"BENCH-2026-06 — Benchmark prestations comptables"* (Prestations, Benchmark, Q3, 280 k€)
  - *"AO-2026-07 — Maintenance multitechnique"* (BTP, Renouvellement, Q3, 950 k€)
  - *"NEGO-2026-08 — Renégociation Veolia eau industrielle"* (Énergie, Renégociation, Q3, 410 k€)
  - *"AO-2026-09 — EPI & vêtements de travail"* (MRO, Renouvellement, Q4, 220 k€)
  - *"AO-2026-10 — Solution e-procurement"* (IT, Nouveau, Q4, 180 k€)
  - *"AO-2026-11 — Refonte agence média"* (Marketing, Renouvellement, Q4, 540 k€)
  - *"NEGO-2026-12 — Renégociation contrats Schneider"* (IT, Renégociation, Q4, 1,8 M€)
  - + 3 initiatives en retard / en tension pour la démo
- Chaque ligne cliquable → fiche détail de l'initiative (description, équipe projet, livrables attendus, jalons, dépendances avec autres initiatives, lien vers le dossier dans Processus A→Z).

**📈 Onglet 3 — Vue Synthèse Exécutive**

Tableau de bord en haut :
- 4 KPI : Nombre d'initiatives · Budget total piloté · Économies prévisionnelles cumulées · Taux d'avancement global.
- **Donut "Répartition par type"** : Renouvellement / Nouveau / Benchmark / Renégociation.
- **Donut "Répartition par catégorie"**.
- **Bar chart trimestriel** : nombre d'initiatives par trimestre (charge de travail visualisée).
- **Bloc IA "Synthèse stratégique"** (texte généré) : *"Votre PAA 2026 totalise 22 initiatives pour 18,3 M€ de spend piloté, avec un objectif de 4,1% d'économies (~750 k€). La concentration Q1-Q2 (62% des initiatives) suggère un risque de surcharge sur les premiers semestres — envisager le glissement de 2-3 chantiers vers Q3."*
- **Bloc "Risques sur le PAA"** : initiatives à risque, dépendances bloquantes, alertes ressources.
- Bouton **"Exporter en PDF / Présenter à la direction"** (génère un livrable type slide deck).

**Tip soutenance** : ce module montre la **dimension stratégique** du métier Achats — ce n'est pas que de l'opérationnel, c'est de la **planification annuelle pluri-millions** avec arbitrages.

---

### 4. 📥 Demandes d'Achat (DA) 🆕 NOUVEAU MODULE — l'amont du processus

**Objectif** : couvrir la **partie amont** du cycle Achats — les utilisateurs métier expriment leurs besoins via une demande d'achat structurée, qui passe par un workflow d'approbation puis bascule en commande. **Sans ce module, AchatPro n'est pas déployable en interne** car le cycle commencerait au milieu.

**Layout** : 2 vues selon le profil → **Vue Demandeur** (utilisateur métier) · **Vue Acheteur** (Mélanie qui traite les DA)

**👤 Vue Demandeur (mode self-service)**

- Hero : *"Exprimer un nouveau besoin"* + bouton CTA **"+ Nouvelle demande d'achat"**.
- Formulaire intelligent en plusieurs étapes (assistant) :
  1. **Type de besoin** : Achat ponctuel / Achat récurrent / Prestation / Investissement / Renouvellement.
  2. **Description du besoin** (texte libre + l'IA suggère une catégorisation automatique).
  3. **Quantité, unité, fréquence**.
  4. **Budget estimé** (si connu) avec **vérification IA temps réel** : *"Votre budget catégorie IT consommé : 78%. Cette demande de 12 k€ porterait à 89%."*
  5. **Date de besoin** (avec alerte si délai trop court par rapport aux délais standards de la catégorie).
  6. **Justification métier** (champ obligatoire pour les demandes > 5 k€).
  7. **Pièces jointes** (cahier des charges, devis indicatif si déjà obtenu).
  8. **Imputation** : centre de coûts, projet, BU.
- **Aide IA en temps réel pendant la saisie** :
  - *"💡 Cette demande ressemble à 'DA-2026-128' validée il y a 2 mois — voulez-vous reprendre ses paramètres ?"*
  - *"💡 Pour cette catégorie, prévoyez 6-8 semaines de délai standard."*
  - *"⚠️ Votre demande dépasse votre seuil de validation directe (5 k€) — un workflow d'approbation à 3 niveaux sera déclenché."*
- **Aperçu du circuit de validation** avant soumission : Demandeur → Manager N+1 → Achats → DAF (selon les règles configurées).
- **"Mes DA"** : liste de toutes les demandes du collaborateur avec statut visuel (📝 Brouillon / 🕐 En attente validation / ✅ Validée / 🛒 Commande émise / 📦 Réception en cours / ✅ Soldée / ❌ Refusée).

**🛒 Vue Acheteur (le pipeline de Mélanie)**

- **Pipeline kanban** des DA en cours :
  - À traiter (nouvellement validées) → En sourcing → En négo → Commande émise → Soldées.
- **Compteurs en haut** : 14 nouvelles aujourd'hui · 8 en retard · 47 en cours · 132 soldées YTD.
- **Cartes DA** dans chaque colonne avec :
  - Numéro, intitulé, demandeur, catégorie, montant, date butoir, jours restants.
  - Badge IA contextuel : *"Similaire à 3 DA récentes — consolidation possible"* / *"Fournisseur référencé existant : Lyreco"* / *"Pas de fournisseur référencé pour cette catégorie".*
- **Vue détail d'une DA** : panneau latéral avec toutes les infos + boutons d'action :
  - *"Commander chez fournisseur référencé"* (raccourci 1-clic).
  - *"Lancer un comparatif d'offres"* (envoie vers le module Comparateur).
  - *"Lancer un AO"* (envoie vers Processus A→Z étape 3).
  - *"Refuser avec motif"* (l'IA propose une réponse polie au demandeur).
  - *"Demander un complément d'info"*.
- **Filtres puissants** : par catégorie, demandeur, BU, montant, statut, urgence, type.
- **Vue "Consolidation"** : l'IA détecte automatiquement les **DA similaires** des 30 derniers jours et propose un regroupement (*"5 DA pour fournitures de bureau totalisant 8 200 € — consolider en 1 commande chez Lyreco ? Économie estimée : 12%"*).

**Tip pédagogique** : c'est le module qui matérialise le **shift left** des Achats — passer de "je traite ce qui arrive" à "je pilote en amont".

---

### 5. 🧭 Processus Achats A→Z — VÉRITABLE ASSISTANT PAS-À-PAS

**Repenser totalement ce module** : ce n'est PAS juste un stepper visuel. C'est un **véritable copilote opérationnel** qui guide Mélanie pas à pas dans le déroulé d'un dossier d'achat, avec aide IA intégrée à chaque étape.

**Layout — Vue d'entrée du module**
- Hero : *"Vos dossiers d'achats en cours"* + bouton CTA **"+ Lancer un nouveau dossier d'achat"** (bouton vert sauge foncé proéminent).
- Liste des dossiers en cours sous forme de cards :
  - Référence + intitulé (*"DA-2026-042 — Renouvellement parc imprimantes siège Paris"*).
  - **Étape actuelle** (1/9) avec mini-stepper visuel.
  - Responsable, montant estimé, date butoir.
  - % de progression + prochaine action attendue.
  - Bouton "Continuer" → ouvre la vue dossier.

**Layout — Vue d'un dossier ouvert** (la vraie valeur du module)

Layout **3 colonnes** :

**Colonne gauche — Stepper vertical des 9 étapes** (chacune cliquable, état visuel : ✅ Faite / 🔄 En cours / ⏳ À venir)
1. Définir le besoin
2. Sourcing fournisseurs
3. Préparer & lancer le RFQ / AO
4. Analyser & comparer les offres
5. Négocier
6. Contractualiser
7. Émettre la commande
8. Réceptionner & contrôler
9. Évaluer le fournisseur

**Colonne centrale — Étape active détaillée**, avec :
- Titre de l'étape + objectif en 1 phrase.
- **Checklist intelligente** générée par l'IA selon le contexte du dossier (ex: pour "Définir le besoin" : *"Avez-vous identifié les utilisateurs finaux ? · Avez-vous chiffré le volume annuel ? · Y a-t-il des contraintes techniques spécifiques ? · Avez-vous validé le budget avec le contrôle de gestion ?"*). Chaque item cochable.
- **Documents associés** à cette étape (cards avec preview, drag & drop pour ajouter).
- **Champs de saisie** structurés selon l'étape (ex: étape 1 → besoin / volume / budget / délai / critères ; étape 3 → liste fournisseurs invités / date limite / critères de notation pondérés).
- **Bouton principal** "Valider cette étape & passer à la suivante" (verrouillé tant que la checklist n'est pas complétée).
- **Boutons secondaires** : "Demander à l'IA" / "Sauvegarder en brouillon" / "Inviter un collègue".

**Colonne droite — Panneau "💡 Aide IA contextuelle"** (toujours visible) :
- Onglet **"Conseils"** : 4-5 tips experts sur l'étape (ex: étape "Négocier" → *"Préparez 3 leviers de négociation distincts. Ne révélez jamais votre BAFO en premier. Demandez toujours une contrepartie pour chaque concession…"*).
- Onglet **"Modèles"** : modèles de documents pertinents pour l'étape (cahier des charges, grille de notation, BAFO, BPU…).
- Onglet **"Pièges à éviter"** : 3-4 erreurs fréquentes documentées.
- Onglet **"Demander à l'IA"** : zone de chat dédiée à cette étape, l'IA connaît tout le contexte du dossier en cours.
- Onglet **"Prompt utilisé"** : lien vers le prompt expert qui pilote cette étape (ouvre la Prompts Library).

**Comportement intelligent**
- Selon la **catégorie d'achat** détectée (IT / prestation / matière première / MRO / véhicules…), l'IA adapte la checklist et les conseils.
- Selon le **montant** détecté, l'IA active les bonnes étapes (ex: < 5k€ → workflow simplifié sans AO formel).
- À l'étape "Analyser les offres", **bouton de raccourci direct** vers le **Comparateur d'offres** (passage automatique des données).
- À l'étape "Négocier", l'IA propose un **brief de négo** pré-rempli.
- À l'étape "Contractualiser", **bouton vers la Rédaction de contrats**.
- À l'étape "Évaluer le fournisseur", **bouton vers le module Évaluation fournisseurs**.

**Ce module est le COLONNE VERTÉBRALE de l'outil — il connecte tous les autres modules entre eux.**

### 6. ✉️ Assistant Emails IA
- Layout deux colonnes : à gauche, scénarios pré-définis (RFQ, Relance, Négociation prix, Refus poli, Mise en demeure, Demande d'avoir, Remerciements…) ; à droite, l'éditeur.
- Sélecteur de **ton** : Ferme / Diplomatique / Urgent / Cordial / Juridique (chips arrondies).
- Sélecteur de **langue** (FR, EN, DE, ES, IT, ZH).
- Mode "miroir" : zone pour coller un email reçu → l'IA propose 3 réponses adaptées.
- Bouton "Vérifier les risques juridiques" qui surligne les phrases engageantes.
- Toutes les signatures d'emails générés se terminent par *"Mélanie Oudoire — Responsable Achats"*.
- Historique des emails générés (sidebar à droite).

---

### 7. 📊 Comparateur d'offres ⭐ NOUVEAU MODULE — soigner particulièrement

**Objectif** : permettre à Mélanie de comparer plusieurs offres reçues pour le même besoin, **côte à côte**, avec **calculs automatiques** et **recommandation IA finale**. Module ultra-démontrable en soutenance.

**Vue d'entrée**
- Liste des comparaisons en cours / archivées sous forme de cards (intitulé du besoin, nombre d'offres, statut, date).
- Bouton CTA **"+ Nouvelle comparaison d'offres"**.

**Création d'une comparaison — Wizard 3 étapes**

**Étape 1 — Définir le besoin de référence**
- Intitulé (ex: *"Renouvellement 25 ordinateurs portables"*).
- Catégorie (chips).
- Critères de notation pondérés (sliders) : Prix · Qualité technique · Délai · Garantie · SAV · RSE / ESG · Conditions de paiement · Localisation. La somme des poids doit faire 100% (l'IA aide à équilibrer).

**Étape 2 — Saisir les offres**
- Bouton "+ Ajouter une offre" (jusqu'à 6).
- Chaque offre = mini-formulaire :
  - Fournisseur (recherche dans la base existante ou nouveau).
  - Upload du document d'offre (PDF / Excel) — l'IA extrait automatiquement les données et **pré-remplit** les champs.
  - Champs structurés : prix unitaire HT, quantité, prix total HT, TVA, frais de port, escompte, conditions de paiement (J0/J30/J60/Lettre de change…), délai de livraison, durée de garantie, conditions SAV, lieu de fabrication, certifications.
  - Champs libres : commentaires de l'acheteuse.

**Étape 3 — Tableau comparatif côte à côte (LE LIVRABLE PHARE)**

Tableau visuel premium (style "carte de menu") :
- **Colonnes = offres** (1 colonne par fournisseur, max 6).
- **Lignes = critères** (toutes les données saisies + critères calculés).
- **Mise en forme intelligente** :
  - Meilleure valeur de chaque ligne **surlignée en vert sauge clair** + petit ✓.
  - Pire valeur en rouge terre clair (subtil).
  - Cellules cliquables → modal de détail.
- Lignes calculées automatiquement par l'IA :
  - **Prix total TTC livré** (calcul : prix HT × qty + transport + TVA − escompte).
  - **Coût mensualisé** (si plan de paiement échelonné).
  - **TCO simplifié** estimé sur la durée de garantie.
  - **Coût ramené à l'unité fonctionnelle** (€/poste, €/mois, €/MWh selon la catégorie).
  - **Économie vs offre la plus chère** (en € et %).
  - **Score pondéré IA** /100 selon les critères de l'étape 1 (calcul transparent au clic : pondération × note de chaque critère).

**🧮 Bouton "Lancer un calcul personnalisé"**
- Ouvre un mini-tableur où l'utilisateur peut écrire ses propres formules en langage naturel (*"calcule le coût total sur 3 ans en intégrant la maintenance annuelle"*) — l'IA construit la formule, exécute, ajoute la ligne au tableau.

**🏆 Recommandation IA finale** (bandeau du bas)
Card mise en valeur avec :
- *"🏆 Recommandation : Offre N°2 — Lenovo via Computacenter"*.
- Justification en 4-5 lignes : *"Bien qu'elle ne soit pas la moins chère (3ème position en prix brut), cette offre obtient le meilleur score pondéré (87/100) grâce à une garantie de 4 ans (vs 2 ans pour la moins chère), un délai de 5 jours, et une note RSE supérieure. Économie réelle estimée sur 4 ans vs offre la moins chère : 2 840 € (TCO)."*
- Boutons : *"Notifier ce fournisseur"* / *"Préparer la négo"* (présélectionne les leviers d'amélioration vs les autres offres) / *"Exporter le rapport"* (PDF de soutenance).

**Vues complémentaires**
- Onglet **"Vue radar"** : graphique radar des 6 offres sur les critères pondérés.
- Onglet **"Vue économique"** : bar chart prix total + TCO + score.
- Onglet **"Historique"** : versions de la comparaison (si Mélanie modifie les pondérations, les versions sont sauvegardées).

**Mocker un cas concret complet** : appel d'offres "25 ordinateurs portables professionnels", 4 offres (Dell, Lenovo via Computacenter, HP, Asus), avec données réalistes prix entre 1 100 € et 1 480 € HT/unité, délais 5-21 jours, garanties 1-4 ans, RSE variables. Recommandation IA gagnante : Lenovo.

### 8. 🔍 Sourcing fournisseurs & prospects
- Barre de recherche puissante avec filtres : secteur, localisation, certifications (ISO 9001, RGE…), CA, effectifs, made in France, RSE.
- Résultats en **cartes fournisseurs** (logo placeholder, nom, score IA /100, badges certifications, CA, localisation, bouton "Voir fiche 360°").
- Onglet "Pipeline" en mode **kanban** : Identifié → Contacté → Qualifié → Référencé → Écarté.
- Vue "Fiche 360°" d'un fournisseur : santé financière, news scrapées, contacts clés, historique, score ESG.
- Alerte "fournisseur en difficulté" en rouge terre si procédure collective détectée.

### 9. ✅ Workflows d'approbation
- Constructeur visuel de circuit en drag & drop (étapes : Demandeur → Manager → Achats → Direction → Validation finale).
- Règles conditionnelles (si montant > X € ET catégorie = Y → ajouter validateur Z).
- Liste des demandes en attente avec statut visuel et SLA.
- Audit trail horodaté.

### 10. 💰 Budget & Engagements 🆕 NOUVEAU MODULE — pilotage financier

**Objectif** : donner à Mélanie et à la DAF une **visibilité temps réel** sur la consommation budgétaire des Achats, les engagements pris (commandes émises non encore facturées), les prévisions atterrissage et les alertes de dépassement. C'est le module qui **réconcilie les Achats avec le Contrôle de Gestion**.

**Layout général** : 4 onglets internes → **Vue d'ensemble** · **Par catégorie** · **Engagements** · **Prévisions & Atterrissage**

**📊 Onglet 1 — Vue d'ensemble**

- **Bandeau "Compteur budgétaire global 2026"** premium :
  - Budget annuel total : **24,5 M€**.
  - Consommé : **14,2 M€** (58%) — barre de progression vert sauge.
  - Engagé non facturé : **3,8 M€** (15%) — superposé en vert sauge clair (hachures).
  - Disponible : **6,5 M€** (27%) — en beige.
  - Indicateur visuel : ✅ Sous contrôle / 🟡 Tension / 🔴 Risque dépassement.
- **3 KPI cards complémentaires** :
  - Taux d'engagement : 73% (consommé + engagé).
  - Burn rate mensuel moyen : 1,52 M€/mois.
  - Atterrissage estimé : 23,8 M€ (97% du budget) — calcul IA basé sur tendance.
- **Graphique combiné mensuel** : barres = budget mensuel cible · ligne pleine = réalisé · ligne pointillée = projection IA jusqu'à fin d'année.
- **Bloc IA "Analyse atterrissage"** : *"À votre rythme actuel, vous atterrirez à 97% du budget annuel, soit 700 k€ d'économies vs prévision. Trois catégories nécessitent une vigilance : Énergie (+8% vs budget), Marketing (+12%), IT (-15%)."*

**🗂️ Onglet 2 — Par catégorie**

- Tableau / cards pour chaque catégorie achats avec :
  - Nom catégorie + icône.
  - Budget annuel · Consommé · Engagé · Disponible · % consommation.
  - **Barre de progression** colorée (vert / jaune / rouge selon le niveau).
  - Variation vs N-1 (en %).
  - Alerte IA si dépassement projeté : *"⚠️ Énergie : à ce rythme, dépassement de 240 k€ projeté en décembre."*
  - Bouton "Voir le détail" (drill-down sur les commandes/factures de la catégorie).
- Mocker au moins **10 catégories** : IT, BTP, Prestations intellectuelles, Énergie, Marketing, Logistique, MRO, Mobilier, Véhicules, Frais généraux.

**📋 Onglet 3 — Engagements (commandes en cours)**

- Liste exhaustive des **commandes émises non encore facturées** (= engagements financiers pris) :
  - N° BdC · Fournisseur · Catégorie · Date émission · Montant HT · Montant TTC · Date livraison prévue · Statut réception · % facturé.
- **Total des engagements en cours** affiché en haut (3,8 M€).
- **Filtres** : par catégorie, par fournisseur, par mois d'émission, par BU.
- **Alerte IA** automatique sur les engagements anciens non soldés : *"📌 12 engagements > 90 jours non facturés (1,2 M€) — vérifier le statut avec les fournisseurs / risque de provisionnement comptable."*
- Bouton "Exporter pour le Contrôle de Gestion" → CSV/Excel avec colonnes standardisées.

**🔮 Onglet 4 — Prévisions & Atterrissage**

- **Tableau de prévision mensuelle** : pour chaque mois restant, quelles dépenses sont prévues (extrapolation IA basée sur l'historique + engagements connus + initiatives PAA en cours).
- **Slider de scénarios** : *"Et si on lance l'AO Énergie ce trimestre ?"* / *"Et si on annule l'investissement mobilier ?"* — recalcule l'atterrissage en temps réel.
- **Compare Budget initial vs Budget révisé vs Atterrissage projeté** (3 lignes superposées).
- Bouton **"Demander une révision budgétaire"** → génère une note motivée à destination de la DAF.

**Tip soutenance** : ce module montre que les Achats sont un **vrai partenaire stratégique de la DAF**, pas juste un service support. Argument fort pour le jury.

---

### 11. 📊 Dashboards & Reporting (Power BI-like)
- Grille de **widgets drag & drop** : dépenses par catégorie (donut), top 10 fournisseurs (bar chart), évolution savings (line chart), répartition géographique (carte), KPI cards.
- Toutes les couleurs des graphiques **dérivées de la palette** (vert sauge → vert profond → doré → terre).
- Filtres globaux : période, BU, catégorie, fournisseur.
- Bouton **"📝 Raconte-moi"** : l'IA génère un commentaire en langage naturel sur les données affichées.
- Boutons d'export PDF / PPT / Excel.
- Alertes intelligentes en haut de page (rupture imminente, dérive prix…).

### 12. 📈 Suivi des dépenses & KPI ⭐ NOUVEAU MODULE — soigner particulièrement

**Objectif** : permettre à Mélanie d'avoir une **vision 360° de ses dépenses** avec analyses statistiques avancées (Pareto, ABC, concentration), pilotage de **KPI Achats clés**, et tableaux de bord exécutifs prêts pour la direction. Module ultra-démontrable en soutenance car il fait écho aux notions académiques (loi de Pareto, méthode ABC, spend analysis).

**Layout général** : navigation par onglets internes en haut → **Vue d'ensemble** · **Analyse Pareto** · **Classification ABC** · **KPI Achats** · **Tableau de bord exécutif**

---

**🔍 Onglet 1 — Vue d'ensemble**

- **Bandeau filtres globaux** persistants : Période (12 derniers mois, YTD, exercice précédent, custom), BU, Site, Catégorie, Devise.
- **4 KPI cards** premium :
  - **Dépenses totales** : montant € + variation N/N-1 (en %, flèche colorée).
  - **Nombre de fournisseurs actifs** + variation.
  - **Panier moyen par commande** + variation.
  - **Taux d'adressage (spend under management)** : % des dépenses gérées par les Achats vs maverick buying.
- **Graphique principal** : évolution mensuelle des dépenses sur 12 mois (bar chart vert sauge avec ligne de tendance dorée).
- **Top 10 catégories** (donut + tableau côté) : Achats indirects, IT, Logistique, BTP, Énergie, Marketing, Prestations intellectuelles, Frais généraux, Voyages, MRO. Chaque part cliquable pour zoomer.
- **Top 10 fournisseurs** (bar chart horizontal) : Schneider Electric, Veolia, Lafarge, Air Liquide, Decathlon Pro, Dell France, Engie, ADP, Sodexo, Computacenter — avec montants réalistes et badges (RSE, contrat-cadre, à risque).
- **Carte de chaleur géographique** des dépenses par site/région.
- **Bouton "📝 Raconte-moi cette période"** : l'IA génère 5 lignes de commentaire automatique sur les chiffres affichés.

---

**📊 Onglet 2 — Analyse Pareto (loi 80/20) — STAR DU MODULE**

C'est le **graphique signature** à soigner particulièrement (très impressionnant en soutenance car visuellement parlant et académiquement correct).

- **Sélecteur de dimension d'analyse** : Par fournisseur · Par catégorie · Par référence article · Par BU · Par site.
- **Graphique Pareto classique** :
  - Bar chart décroissant des dépenses (vert sauge).
  - Courbe cumulée superposée (vert profond).
  - **Ligne horizontale à 80%** (pointillés dorés) avec label *"Seuil 80%"*.
  - **Ligne verticale automatique** marquant le 20% des items qui font 80% des dépenses.
  - Zone surlignée en vert sauge clair sur la "zone critique 20/80".
- **Encart résultat IA** mis en valeur :
  > *"📌 Loi de Pareto vérifiée : **18% de vos fournisseurs (28 sur 154) concentrent 81,3% de vos dépenses**. Cette concentration est typique d'un portefeuille mature mais soulève un point de vigilance sur la dépendance fournisseur."*
- **Tableau détaillé** sous le graphique :
  - Colonnes : Rang, Nom, Dépense €, % du total, % cumulé, Zone (A/B/C colorée), Actions.
  - Tri par défaut décroissant.
  - Boutons d'action par ligne : Voir fiche fournisseur / Lancer renégociation / Évaluer dépendance.
- **3 recommandations IA contextuelles** sous l'analyse :
  - *"💰 Concentrez les efforts de négociation sur les 28 fournisseurs du top 80% — gain potentiel estimé : 2 à 4% du spend, soit 340-680 k€/an."*
  - *"⚠️ 4 fournisseurs représentent chacun > 5% du spend total : risque de dépendance critique. Plan de back-up recommandé."*
  - *"🪶 La queue longue (126 fournisseurs pour 18,7% du spend) est un levier de simplification : consolidation possible vers 30-40 références."*

---

**🅰️ Onglet 3 — Classification ABC (méthode ABC)**

- **Visualisation interactive** : 3 zones colorées (A en vert profond / B en vert sauge / C en beige sable) avec compteurs et montants.
  - **Zone A** : ~20% des items = ~80% du spend (suivi serré, contrats cadres, négociation annuelle).
  - **Zone B** : ~30% des items = ~15% du spend (suivi régulier).
  - **Zone C** : ~50% des items = ~5% du spend (gestion simplifiée, automatisation).
- **Sélecteur de critère** : valeur dépensée / volume / fréquence d'achat / criticité métier.
- **Tableau triable** avec filtres par classe (badges A/B/C colorés).
- **Stratégies de gestion recommandées par classe** (encarts pédagogiques) :
  - **A** : *"Contrats-cadres pluriannuels, négociation détaillée, suivi mensuel, plan B obligatoire."*
  - **B** : *"Référencement standard, revue trimestrielle, mutualisation possible."*
  - **C** : *"Catalogue électronique, auto-validation < 1k€, regroupement de commandes."*
- **Matrice croisée** ABC × Criticité (4 quadrants type Kraljic) : Effet de levier / Stratégique / Non-critique / Goulot d'étranglement — chaque fournisseur positionné en bulle. Bonus pédagogique fort en soutenance.

---

**📐 Onglet 4 — KPI Achats (le cœur du pilotage)**

Grille de **12 KPI** organisés en 4 thèmes, chacun en card avec valeur, variation, mini-sparkline, cible, et statut visuel (✅ Atteint / 🟡 À surveiller / 🔴 Hors cible).

**🎯 Performance économique**
1. **Savings réalisés YTD** (€ et % du spend) — cible : 4% du spend annuel
2. **Savings vs budget** (% d'atteinte de l'objectif annuel)
3. **Coût moyen par commande** (€/BdC) — efficience opérationnelle

**⚡ Performance opérationnelle**
4. **OTD — On Time Delivery** (% commandes livrées dans les délais)
5. **OTIF — On Time In Full** (% commandes livrées à temps ET complètes)
6. **Lead time moyen** (jours entre commande et livraison)
7. **Cycle time achat** (jours entre expression du besoin et signature du BdC)

**🤝 Pilotage fournisseurs**
8. **Taux de dépendance** (% spend concentré sur top 5 fournisseurs)
9. **Nombre de fournisseurs actifs** (et évolution)
10. **Taux de rationalisation** (réduction du nombre de fournisseurs YTD)

**🌱 RSE & conformité**
11. **% spend avec fournisseurs notés ESG** (>seuil minimal)
12. **Taux de couverture contractuelle** (% spend sous contrat formalisé)

**Comportement** :
- Chaque KPI cliquable → ouvre une vue détaillée avec graphique 24 mois, décomposition par BU/catégorie, benchmarks marché (mock), commentaires IA.
- Bouton **"+ Ajouter un KPI personnalisé"** : Mélanie peut créer ses propres KPI (formule, seuils, fréquence).

---

**🎨 Onglet 5 — Tableau de bord exécutif (one-pager direction)**

- **Format A4 paysage** simulé : layout figé optimisé pour export PDF / impression / présentation comité de direction.
- **En-tête** : logo AchatPro + titre *"Reporting Achats — Avril 2026"* + sous-titre *"Préparé par Mélanie Oudoire"*.
- **Pavé synthèse** (haut, 4 chiffres XL) : Spend total · Savings · Fournisseurs actifs · Taux d'adressage.
- **3 graphiques compacts en ligne** : évolution spend mensuel · top 10 catégories (donut) · Pareto fournisseurs simplifié.
- **Zone "Faits marquants"** : 4 bullet points générés par l'IA (ex: *"Renégociation Veolia : -12 800 €/an"*, *"Nouveau contrat-cadre IT signé : 25 fournisseurs → 3"*).
- **Zone "Points d'attention"** : 3 alertes (cuivre +14%, dépendance Schneider 28%, retard projet AO nettoyage).
- **Zone "Plan d'actions du mois"** : 5 actions prioritaires avec responsable et échéance.
- **Boutons d'export** (top right) : 📄 PDF · 📊 PowerPoint · 📧 Envoyer par email · 📅 Programmer envoi mensuel automatique.

**Tip soutenance** : ce tableau de bord exécutif est le **livrable concret** que Mélanie peut "tendre" au jury — c'est ce qu'elle produirait réellement en interne chaque mois.

---

### 13. 💰 Calculateur TCO
- **Wizard étape par étape** par catégorie : véhicules, IT, machines, logiciels SaaS, consommables, prestations.
- Inputs : coût d'acquisition, transport, installation, formation, maintenance annuelle, énergie, consommables, fin de vie, durée d'usage.
- **Visualisation iceberg** : coût visible en surface vs coûts cachés sous la ligne d'eau (illustration SVG élégante).
- Mode comparaison **multi-fournisseurs** côte à côte (jusqu'à 4).
- **Sliders de sensibilité** : *"Et si l'énergie augmente de 10% ?"*, *"Et si la durée d'usage passe de 5 à 7 ans ?"*.
- Export rapport TCO PDF prêt à présenter.

### 14. 📉 Analyse des coûts
- **Should-cost model** : décomposition automatique matière + main d'œuvre + énergie + marge fournisseur (donut + tableau détaillé).
- Benchmarks marché intégrés (mock : indices matières, MEPI, BTP01…).
- Détecteur de dérives prix automatique avec graphique d'alerte.
- Suggestions IA : *"Tu pourrais économiser 12% en regroupant les commandes A et B."*
- Mode Pareto interactif (les 20% qui font 80% des coûts).

### 15. 🤝 Évaluation fournisseurs
- Liste des fournisseurs évalués avec **scorecard** : qualité, délai, prix, RSE, innovation (radar chart).
- Plan de progrès partagé par fournisseur.
- Historique des incidents et résolutions.
- Bouton "Préparer la QBR" (Quarterly Business Review) → l'IA génère un brief.

### 16. 📑 Analyse de contrats
- Zone de **drop file** élégante au centre (illustration feuille subtile).
- Après dépôt : panneau split — à gauche le contrat avec **surlignage code couleur** 🟢 OK / 🟡 attention / 🔴 risque ; à droite le panneau d'analyse.
- **Score de risque global /100** avec décomposition (juridique, financier, opérationnel, conformité).
- Liste des **dates clés extraites** (échéance, renouvellement tacite, préavis) avec bouton "Ajouter au calendrier".
- **Résumé exécutif** en 5 lignes pour la direction.
- Comparaison automatique avec un contrat-type de référence.
- Bouton "Voir le prompt utilisé" → ouvre le prompt dans la Prompts Library (lien direct).

### 17. ✍️ Rédaction de contrats
- Sélection du type : Achat, Prestation, NDA, Contrat-cadre, SLA, Partenariat.
- Mode **construction par blocs** : drag & drop des clauses depuis une bibliothèque latérale.
- Surligneur des clauses sensibles avec explication contextuelle au survol.
- Versioning (V1, V2, V3) avec track changes visuel.
- Export Word avec mise en forme cabinet d'avocats.
- Bouton "Faire relire par l'IA" → ouvre l'analyse côte à côte.

### 18. 🗄️ GED Achats 🆕 NOUVEAU MODULE — coffre-fort documentaire

**Objectif** : centraliser **tous les documents** liés aux Achats — contrats actifs, CGV/CGA, attestations légales (URSSAF, Kbis, RC Pro, vigilance), certifications fournisseurs (ISO 9001, ISO 14001, Ecovadis…) — avec **gestion automatique des expirations**. Indispensable en conformité (devoir de vigilance, audits).

**Layout général** : navigation par onglets internes → **Vue d'ensemble** · **Contrats** · **Attestations légales** · **Certifications** · **Recherche**

**🏠 Onglet 1 — Vue d'ensemble**

- **4 KPI cards** :
  - **Documents archivés** : 1 247 (avec répartition par type).
  - **Contrats actifs** : 142 (dont 23 expirent dans 90 jours — badge orange).
  - **Attestations à renouveler** : 18 (dont 4 expirées — badge rouge terre).
  - **Couverture conformité** : 87% (% de fournisseurs actifs avec docs à jour).
- **🚨 Bloc "Alertes documentaires"** central :
  - **Expirations imminentes** (30 prochains jours) avec liste cliquable :
    - *"Contrat Veolia eau industrielle — expire dans 12 jours — renouvellement non lancé ⚠️"* → bouton "Lancer renouvellement"
    - *"Attestation URSSAF Schneider — expire dans 18 jours"* → bouton "Demander mise à jour"
    - *"Certification ISO 9001 Lafarge — expire dans 27 jours"* → bouton "Relancer fournisseur"
  - **Documents expirés** (à régulariser).
  - **Documents manquants** (fournisseurs actifs sans attestation à jour).
- **Mini-graphique** : pyramide d'âge des contrats (combien de contrats expirent par trimestre sur les 24 prochains mois).

**📑 Onglet 2 — Contrats**

- Tableau exhaustif de tous les contrats archivés avec colonnes :
  - N° contrat · Fournisseur · Catégorie · Type (cadre, ponctuel, NDA, SLA…) · Date signature · Date expiration · Tacite reconduction (Oui/Non) · Préavis · Montant · Statut.
- Filtres puissants : par catégorie, par fournisseur, par type, par statut (actif / expiré / résilié), par échéance.
- **Code couleur** sur la colonne expiration : 🟢 > 6 mois / 🟡 3-6 mois / 🟠 1-3 mois / 🔴 < 1 mois.
- Cliquer un contrat → vue détail :
  - Visualiseur PDF intégré avec surlignage.
  - **Métadonnées extraites par IA** : montant, dates clés, parties, juridiction, clauses spécifiques.
  - **Liens vers** : analyse IA du contrat (module 16), commandes liées, factures liées, fournisseur (fiche 360).
  - Boutons d'action : "Lancer le renouvellement" / "Programmer rappel" / "Marquer comme résilié" / "Télécharger".
- Bouton **"+ Archiver un nouveau contrat"** : drag & drop → l'IA extrait automatiquement les métadonnées et propose le classement.

**📜 Onglet 3 — Attestations légales (devoir de vigilance)**

- Liste des fournisseurs avec **matrice de conformité** :
  - Lignes : fournisseurs actifs.
  - Colonnes : URSSAF · Kbis · RC Pro · Vigilance (art. L8222-1) · DUER · Liste sociale · Anti-corruption Sapin II.
  - **Cellules colorées** : 🟢 valide / 🟡 expire bientôt / 🔴 expirée ou manquante / ⚪ non requise.
- **Bouton "Demander en masse"** : sélection multiple de fournisseurs → l'IA envoie un email automatique de demande d'attestations (avec lien upload sécurisé mocké).
- **Score de conformité globale** du portefeuille fournisseurs (%).
- **Alerte légale** : *"⚠️ La loi devoir de vigilance impose la collecte semestrielle de l'attestation Vigilance pour tout fournisseur > 5 000 € sur 12 mois. 12 fournisseurs sont concernés et non à jour."*

**🏆 Onglet 4 — Certifications fournisseurs**

- Vue identique mais pour les **certifications** : ISO 9001 (qualité), ISO 14001 (environnement), ISO 27001 (sécurité IT), ISO 45001 (santé & sécurité), Ecovadis (RSE), Sedex, B Corp, Made in France, Origine France Garantie, RGE.
- Filtres par certification → liste des fournisseurs certifiés (utile pour AO contraints).
- **Alerte** sur certifications proches de l'expiration.

**🔍 Onglet 5 — Recherche**

- Barre de **recherche full-text IA sémantique** : *"Cherche tous les contrats incluant une clause de tacite reconduction au-delà de 12 mois"* → résultats classés par pertinence.
- Filtres avancés : type de doc, période, fournisseur, montant, mots-clés dans le contenu, présence de clauses spécifiques.
- Export des résultats en CSV/PDF.

**Tip soutenance** : ce module montre la maîtrise de la **dimension juridique et conformité** du métier Achats — sujet de plus en plus critique avec CSRD, devoir de vigilance, etc.

---

### 19. 🛡️ Gestion des risques fournisseurs
- **Matrice de risque** visuelle : axe X probabilité, axe Y impact, fournisseurs en bulles colorées.
- Alertes news temps réel (mock) : actualités fournisseurs (procédures, rachats, scandales).
- Indicateur de **dépendance** par fournisseur (jauge : *"Représente 34% de tes achats catégorie IT"*).
- Plan de mitigation type généré par IA pour chaque risque.
- Cartographie géopolitique simplifiée (origines, transit).

### 20. 🌱 RSE / ESG / Conformité
- Score ESG moyen du portefeuille fournisseurs (jauge élégante).
- Liste fournisseurs avec score Ecovadis / Sedex / CDP (mock).
- Checklist devoir de vigilance (Loi Sapin II, CSRD, CS3D, CBAM).
- **Empreinte carbone Scope 3** estimée (graphique).
- Bouton "Envoyer le questionnaire ESG" aux fournisseurs.
- Alerte conformité (sanctions, embargos, listes noires) si pertinent.

### 21. 🔗 Intégrations
- **Galerie de connecteurs** : grille de logos cliquables (SAP, Oracle, Sage, DocuSign, Stripe, Slack, Teams, Excel, Google Workspace, Salesforce, HubSpot…).
- Statut visuel : Connecté ✅ / Disponible / Bientôt.
- Mode "import CSV" en fallback.
- Section Webhooks pour Zapier/Make.

### 22. 📚 Base de connaissances
- Barre de recherche IA sémantique : *"Pose ta question en langage naturel"*.
- Catégories : Glossaire, Procédures, Modèles de documents, Micro-formations vidéo (placeholders), FAQ.
- Glossaire interactif (survol d'un terme → définition en tooltip).
- Wiki contributif d'équipe.

### 23. 🪄 PROMPTS LIBRARY — module signature

C'est **LE différenciateur** du produit. Soigne particulièrement ce module.

**Layout** :
- Sidebar interne avec catégories : Tous, Contrats, TCO, Emails, Sourcing, Risques, Reporting, Personnalisés.
- Liste centrale des prompts (cards élégantes) : nom, description courte, badge "Système" / "Équipe" / "Perso", version (V3.2), date de modif, auteur, nombre d'utilisations.
- Panneau de détail à droite quand on sélectionne un prompt.

**Vue détail d'un prompt** :
- Onglets : **Vue** / **Édition** / **Versions** / **Sandbox**.
- **Vue** : prompt formaté, avec variables surlignées en vert sauge (`{nom_fournisseur}`, `{montant}`…).
- **Édition** : éditeur de texte enrichi, suggestions IA pour améliorer le prompt en temps réel ("Ce prompt est trop ambigu sur la partie X"), avertissement si trop long.
- **Versions** : timeline verticale élégante avec toutes les versions, possibilité de comparer 2 versions côte à côte (diff coloré), bouton rollback.
- **Sandbox** : zone de test — l'utilisateur dépose un document mock, voit le résultat de l'ancienne vs nouvelle version du prompt.

**Permissions** :
- Badge "Système" (verrouillé, modifiable par admin uniquement).
- Badge "Équipe" (modifiable par les acheteurs).
- Badge "Perso" (favoris perso).

**Marketplace interne** :
- Onglet "Partager avec l'équipe" + import/export JSON.
- Section "Prompts populaires de l'équipe" en haut.

**Tips intégrés** :
- Encart latéral "💡 Bonnes pratiques de prompting" (5 conseils).
- Compteur de tokens estimé.

**Exemples de prompts à mocker** (au moins 16) :
1. *"Analyse de contrat - Détection de clauses risquées"* (V4.1, Système)
2. *"Email - Relance commerciale ferme"* (V2.0, Équipe, par M. Oudoire)
3. *"TCO - Décomposition coûts cachés véhicules"* (V1.5, Système)
4. *"Sourcing - Qualification fournisseur ISO 9001"* (V3.0, Équipe)
5. *"Should-cost - Modélisation pièce mécanique"* (V2.2, Système)
6. *"Risque - Analyse santé financière fournisseur"* (V1.8, Système)
7. *"ESG - Évaluation conformité CSRD"* (V1.0, Équipe)
8. *"Reporting - Synthèse exécutive mensuelle"* (V2.5, Perso, par M. Oudoire)
9. *"Comparateur - Analyse pondérée multi-offres"* (V2.0, Système) ⭐ pour le Comparateur
10. *"Veille - Synthèse impact matières premières sur portefeuille"* (V1.2, Système) ⭐ pour la Veille
11. *"Processus - Checklist intelligente étape "Définir le besoin""* (V3.1, Système) ⭐ pour Processus A→Z
12. *"Spend Analysis - Pareto & classification ABC commentés"* (V1.5, Système) ⭐ pour Suivi des dépenses
13. *"PAA - Analyse stratégique du plan annuel et risques de surcharge"* (V1.0, Système) 🆕 pour PAA
14. *"DA - Détection de consolidation possible entre demandes similaires"* (V2.1, Système) 🆕 pour Demandes d'Achat
15. *"Budget - Projection atterrissage budgétaire et recommandations"* (V1.3, Système) 🆕 pour Budget & Engagements
16. *"GED - Extraction métadonnées contrat et alertes expiration"* (V2.0, Système) 🆕 pour GED Achats

Chaque prompt mocké doit avoir un **vrai contenu réaliste** (10-30 lignes de prompt expert métier, pas du Lorem Ipsum).

---

## 🤖 PANNEAU IA LATÉRAL (toujours accessible)

- Bouton flottant en bas à droite (icône feuille IA) qui ouvre un panneau latéral.
- Header : "Assistant AchatPro" + statut "En ligne".
- Zone de chat avec messages utilisateur (alignés à droite, fond crème) et IA (alignés à gauche, fond vert sauge clair).
- Suggestions d'actions contextuelles selon le module en cours (3 chips cliquables).
- Bouton "Voir/modifier le prompt utilisé" en bas → renvoie vers la Prompts Library.
- Mock : 2-3 conversations pré-remplies pour démo.

---

## ⚙️ CONTRAINTES TECHNIQUES

- **React** mono-fichier, export default d'un composant `App`.
- **Tailwind CSS** pour le styling — utiliser **uniquement les classes utilitaires de base** (pas de config custom).
- **Lucide React** pour les icônes.
- **Recharts** pour tous les graphiques, en personnalisant les couleurs avec la palette.
- Navigation par **état React** (`useState` pour le module actif), pas de routing externe.
- Toutes les **données mockées en dur** dans le composant (réalistes, en français, avec noms d'entreprises crédibles : *Lafarge, Veolia, Schneider, Decathlon, Air Liquide…*).
- Toggle **dark/light mode** fonctionnel.
- **Aucun localStorage / sessionStorage** (interdit dans les artifacts).
- Aucune dépendance externe non listée.

### 🌐 CONTRAINTES POUR DÉPLOIEMENT & PARTAGE PUBLIC

L'application doit pouvoir être **partagée par lien à n'importe qui** (jury de soutenance, collègues, direction) sans authentification. Le code doit donc respecter ces règles :

- **100% client-side** : aucune API backend, aucun appel serveur, aucune base de données externe. Tout tourne dans le navigateur.
- **Pas de variables d'environnement, pas de clés API** : si une fonctionnalité IA est simulée, le résultat doit être **mocké en dur** dans le code (textes pré-écrits, réponses pré-définies).
- **Pas de `localStorage` / `sessionStorage` / `IndexedDB`** : utiliser uniquement `useState` / `useReducer` pour l'état (rappel : c'est aussi interdit dans les artifacts).
- **Pas de `fetch` vers des URLs externes** sauf images publiques type Unsplash si vraiment nécessaire (préférer SVG inline ou placeholders en CSS).
- **Pas de polices à charger dynamiquement** : utiliser des polices déjà disponibles via Tailwind ou inline en `<style>`. Si tu utilises Playfair Display + Inter, importe-les en `<link>` Google Fonts dans un bloc `useEffect` qui injecte la balise dans `<head>`.
- **Toutes les images** : SVG inline ou data-URI, pas de chemins relatifs.
- **Aucune dépendance non bundlée par défaut** dans l'environnement Claude / sandpack.
- **Le code doit être copiable tel quel** dans un fichier `App.jsx` d'un projet React standard (Vite ou Create React App) et fonctionner immédiatement.

### 🚀 INSTRUCTIONS DE DÉPLOIEMENT (à inclure en commentaire en haut du code généré)

Le code généré doit commencer par un **commentaire d'en-tête** récapitulant les options de partage :

```jsx
/**
 * AchatPro — Maquette interactive
 * Auteure : Mélanie Oudoire
 *
 * 🌐 OPTIONS DE PARTAGE PUBLIC :
 *
 * Option 1 — Partage natif Claude (le plus simple)
 *   1. Cliquer sur "Publish" en haut à droite de l'artifact
 *   2. Copier le lien généré (ex: claude.ai/public/artifacts/xxx)
 *   3. Toute personne avec le lien peut ouvrir la maquette dans son navigateur
 *
 * Option 2 — Déploiement Vercel (URL pro pour soutenance)
 *   1. Créer un projet React : `npm create vite@latest achatpro -- --template react`
 *   2. Installer les deps : `npm i lucide-react recharts tailwindcss`
 *   3. Coller ce code dans src/App.jsx
 *   4. Configurer Tailwind (npx tailwindcss init -p)
 *   5. Pousser sur GitHub, importer dans vercel.com → URL type achatpro.vercel.app
 *
 * Option 3 — Netlify Drop (zéro config)
 *   1. Builder le projet localement : `npm run build`
 *   2. Glisser-déposer le dossier `dist` sur netlify.com/drop
 *   3. URL générée immédiatement
 */
```

Cet en-tête sert de **mémo** à Mélanie pour qu'elle sache comment partager sa maquette après génération.

---

## ✅ CRITÈRES DE QUALITÉ

À ne PAS faire :
- ❌ Couleurs Recharts par défaut (violet/bleu génériques).
- ❌ Bordures grises ternes type Bootstrap.
- ❌ Icônes emoji partout dans l'UI (utiliser Lucide, garder les emojis pour la sidebar nav).
- ❌ Lorem Ipsum — tout doit être du contenu Achats réaliste en français.
- ❌ Tout afficher d'un coup : prioriser **densité d'info maîtrisée**.
- ❌ Boutons criards, dégradés flashy, ombres dures.

À faire absolument :
- ✅ White space généreux, respiration entre les sections.
- ✅ Hiérarchie typographique claire (serif sur les gros titres uniquement).
- ✅ Données mock crédibles avec chiffres réalistes (économies en €, dates 2025-2026, noms FR).
- ✅ Au moins **1 micro-illustration botanique SVG** discrète sur la page d'accueil.
- ✅ Cohérence totale entre les modules (mêmes composants, mêmes patterns).
- ✅ Les 16 modules doivent être **navigables** (même si certains sont des layouts simples avec quelques cards).
- ✅ Le module **Prompts Library doit être le plus poussé et soigné** — c'est le différenciateur de la soutenance.

---

## 🚀 ORDRE DE LIVRAISON

Si la complexité dépasse la capacité d'un seul artifact, **prioriser dans cet ordre** :

1. **Squelette complet** : layout, sidebar avec les 23 modules + section Roadmap, topbar, panneau IA, dark/light mode, palette appliquée, profil "Mélanie Oudoire".
2. **Tableau de bord enrichi** (avec les 4 sous-onglets d'alertes IA développés).
3. **Demandes d'Achat (DA)** 🆕 (l'amont du processus, indispensable au déploiement interne).
4. **Plan Annuel des Achats (PAA)** 🆕 (vision stratégique, fort impact jury).
5. **Budget & Engagements** 🆕 (réconciliation Achats/DAF).
6. **Suivi des dépenses & KPI** ⭐ (Pareto + ABC + KPI + tableau de bord exécutif).
7. **Processus Achats A→Z** (assistant pas-à-pas, colonne vertébrale).
8. **Comparateur d'offres** ⭐ (le module phare pour la démo).
9. **GED Achats** 🆕 (conformité, devoir de vigilance).
10. **Prompts Library** entièrement designée (différenciateur).
11. **Veille & Alertes Marchés** (impressionnant en démo).
12. **Analyse de contrats** + **Calculateur TCO** + **Sourcing** + **Dashboards** (les autres modules forts).
13. Les modules restants avec un design soigné mais plus simple.
14. La section **Roadmap** dans la sidebar (juste visuelle, items non-cliquables).

Si tu manques de place, dis-le explicitement et propose de continuer dans une seconde itération en gardant l'état (*"je continue avec le module X au prochain message"*). **N'hésite pas à splitter en 2-3 artifacts si besoin** — la qualité prime sur la complétude en une seule fois.

---

## 🎬 TOUCHES FINALES POUR LA SOUTENANCE

- Sur la page d'accueil, mets une **citation inspirante** en bas de page :  
  *"L'achat n'est plus une fonction support. C'est un levier stratégique. — AchatPro"*
- Easter egg : dans le menu profil de Mélanie, ajoute une option *"Mode Présentation"* qui agrandit légèrement les éléments (mock, juste un bouton).
- Le logo "AchatPro" doit avoir une **icône feuille minimaliste** dessinée en SVG inline (vert sauge foncé).
- L'ensemble de l'application doit donner la sensation d'avoir été **conçue spécifiquement pour Mélanie** (personnalisation visible : prénom, prompts perso signés "M. Oudoire", suggestions IA contextuelles à son historique).

---

## 🌐 GUIDE DÉTAILLÉ — RENDRE LE LIEN ACCESSIBLE À TOUS

Cette section est un **mémo pour Mélanie** une fois la maquette générée. Trois options classées du plus simple au plus pro :

### Option A — Lien Claude natif ⚡ (le plus rapide)

1. Une fois l'artifact React généré, en haut à droite de l'artifact, clique sur **"Publish"** (ou "Partager").
2. Claude génère un lien public type `https://claude.ai/public/artifacts/...`
3. Toute personne (sans compte Claude) peut ouvrir ce lien dans son navigateur et **interagir avec la maquette**.
4. Idéal pour : partage rapide aux collègues, démos en interne, lien dans un email de présentation.
5. Limite : l'URL n'est pas personnalisée et la mention "Made with Claude" peut apparaître.

### Option B — Vercel 🏆 (recommandé pour la soutenance)

URL propre, professionnelle, totalement maîtrisée — environ **10 minutes de mise en place**.

1. Installer Node.js si ce n'est pas déjà fait : nodejs.org.
2. Créer un projet React :
   ```bash
   npm create vite@latest achatpro -- --template react
   cd achatpro
   npm install
   npm install lucide-react recharts
   npm install -D tailwindcss postcss autoprefixer
   npx tailwindcss init -p
   ```
3. Configurer Tailwind dans `tailwind.config.js` :
   ```js
   content: ["./index.html", "./src/**/*.{js,jsx}"]
   ```
4. Dans `src/index.css`, ajouter :
   ```css
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```
5. **Coller le code généré par Claude dans `src/App.jsx`** (remplacer le contenu existant).
6. Tester en local : `npm run dev` → ouvrir http://localhost:5173.
7. Pousser sur GitHub :
   ```bash
   git init && git add . && git commit -m "AchatPro v1"
   gh repo create achatpro --public --source=. --push
   ```
   (ou via l'interface GitHub).
8. Aller sur **vercel.com** → "Add New Project" → importer le dépôt GitHub → "Deploy".
9. **Lien public** généré automatiquement : `https://achatpro-melanie.vercel.app` (personnalisable dans les settings).
10. Chaque modification poussée sur GitHub redéploie automatiquement.

### Option C — Netlify Drop 🎯 (zéro config technique)

Idéal si tu veux juste un lien sans rien installer côté Git.

1. Créer un projet React local (mêmes étapes 1 à 6 que Vercel).
2. Builder le projet : `npm run build` → un dossier `dist/` est créé.
3. Aller sur **app.netlify.com/drop**.
4. **Glisser-déposer le dossier `dist`** sur la page.
5. Lien public généré immédiatement : `https://random-name-xyz.netlify.app` (renommable gratuitement dans les settings).

### 💡 Conseils pour la soutenance

- **Réserve un nom de domaine personnalisé** sur Vercel/Netlify (gratuit en `.vercel.app`, ~10€/an pour un `.com` propre type `achatpro.com`).
- **Teste la maquette sur plusieurs navigateurs** avant le jour J (Chrome, Safari, Firefox).
- **Ouvre le lien sur le PC du jury** en arrivant pour éviter tout stress technique.
- **Prévois une capture vidéo** (Loom, OBS) en backup au cas où la connexion internet de la salle serait défaillante.
- **Imprime un QR code** du lien à distribuer au jury — effet pro garanti.

---

**Démarre maintenant. Génère la maquette React complète en respectant toutes ces consignes. Sois ambitieux sur le design, généreux sur le contenu mock, rigoureux sur la cohérence visuelle.**
