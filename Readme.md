# Calculateur d'Intérêts de Retard V3 - Guide d'utilisation

## 📋 Description

Application web professionnelle pour calculer automatiquement les **intérêts de retard** selon le **taux d'intérêt légal français**. Conçue pour les professionnels du droit (avocats, juristes, huissiers) et toute personne devant calculer des intérêts moratoires conformément à la réglementation française.

### ✨ Nouveautés Version 3

- 🆕 **Import Excel** - Collez directement vos données depuis Excel
- 🆕 **Calculs multiples** - Traitez plusieurs dettes simultanément
- 🆕 **Parser intelligent** - Détection automatique des montants et dates
- 🆕 **Rapport PDF enrichi** - Tableau des taux légaux appliqués
- 🆕 **Interface modernisée** - UX améliorée avec animations
- ✅ **Taux S2 2025 à jour** - 6,65% particuliers / 2,76% professionnels

## ⚖️ Cadre légal

L'application se base sur :
- **Articles L. 313-2 et suivants** du Code monétaire et financier
- **Article L. 313-3 CMF** - Majoration de 5 points en cas de condamnation
- **Loi n° 75-619 du 11 juillet 1975**, article 3
- **Ordonnance n° 2014-947 du 20 août 2014** (réforme du taux)
- **Décret n° 2014-1115 du 2 octobre 2014** (modalités de calcul)
- **Arrêté du 19 juin 2025** (taux S2 2025)

### Taux actuels (2nd semestre 2025)
- **Créancier particulier / Commerçant** : 6,65%
- **Créancier professionnel (B2B)** : 2,76%

## 🚀 Installation et utilisation

### Méthode simple (recommandée)
1. **Téléchargez** le fichier `calculateur_til_v3.html`
2. **Double-cliquez** sur le fichier pour l'ouvrir dans votre navigateur
3. L'application fonctionne **entièrement hors ligne** - aucune connexion internet requise

### Configuration requise
- Navigateur moderne (Chrome, Firefox, Safari, Edge)
- Aucune installation supplémentaire nécessaire
- JavaScript activé (activé par défaut)

## 📖 Guide d'utilisation

### Mode 1 : Calcul unique

#### 1.1 Informations de base

##### Montant de la dette
- Saisissez le montant principal de la créance en euros
- Utilisez le point ou la virgule pour les décimales
- Exemple : `15625.00` ou `15625,00`

##### Date d'exigibilité
- Date à partir de laquelle les intérêts commencent à courir
- Généralement : date de mise en demeure, date d'échéance impayée, ou date fixée par contrat
- Format : JJ/MM/AAAA via le sélecteur de date

##### Type de créancier
- **Particulier / Commerçant** : Personne physique, commerçant, artisan (taux plus élevé)
- **Professionnel (B2B)** : Relations entre professionnels uniquement (taux réduit)

#### 1.2 Options de calcul

##### Capitalisation des intérêts
- **Activée** : Les intérêts sont ajoutés au capital à chaque fin de semestre (anatocisme)
- **Désactivée** : Intérêts simples calculés uniquement sur le capital initial

**Important** : La capitalisation est soumise aux conditions de l'article 1343-2 du Code civil. Elle nécessite généralement :
- Une mise en demeure préalable
- Une durée d'au moins un an
- Une décision de justice pour les intérêts antérieurs au jugement

##### Condamnation judiciaire
Si une décision de justice a été rendue :
1. Cochez l'option **"Condamnation judiciaire"**
2. Indiquez la **date du jugement**
3. La majoration de **+5 points** s'applique automatiquement **2 mois après** le jugement (Art. L.313-3 CMF)

**Exemple** : 
- Jugement le 01/01/2024 → Majoration à partir du 01/03/2024
- Taux particulier S1 2024 : 8,01% → devient 13,01%

### Mode 2 : Import Excel (Nouveau ✨)

#### 2.1 Préparation des données

Dans Excel ou LibreOffice, organisez vos données avec au minimum :
- **Une colonne** pour les montants (en euros)
- **Une colonne** pour les dates d'exigibilité

Optionnel :
- **Une colonne** pour les références/numéros de facture

**Formats acceptés** :

| Format montant | Exemples acceptés |
|----------------|-------------------|
| Sans espace | `15625` `15625.50` |
| Avec espaces | `15 625` `15 625.50` |
| Avec virgule | `15625,50` `15 625,50` |
| Avec € | `15625€` `15 625 €` `15625,50€` |

| Format date | Exemples acceptés |
|-------------|-------------------|
| Français | `31/12/2023` `31-12-2023` `31.12.2023` |
| ISO | `2023-12-31` |

#### 2.2 Import des données

1. **Sélectionnez** vos lignes dans Excel (avec ou sans en-tête)
2. **Copiez** (Ctrl+C ou Cmd+C)
3. Cliquez sur le mode **"Import Excel"**
4. **Collez** dans la zone de texte (Ctrl+V ou Cmd+V)
5. Cliquez sur **"🔍 Analyser les données"** pour vérifier

#### 2.3 Aperçu et validation

Après le collage, l'application affiche :
- ✅ **Nombre de dettes détectées** avec aperçu
- ⚠️ **Erreurs de parsing** si certaines lignes sont invalides

Chaque dette détectée montre :
- Référence (ou "Dette N" par défaut)
- Date d'exigibilité
- Montant

#### 2.4 Calcul groupé

1. Vérifiez que les données détectées sont correctes
2. Sélectionnez le **type de créancier** (commun à toutes les dettes)
3. Activez/désactivez la **capitalisation** (commune à toutes)
4. Cliquez sur **"Calculer toutes les dettes"**

#### 2.5 Résultats multi-dettes

L'application affiche :
- **Récapitulatif global** : Capital total, intérêts totaux, montant total
- **Tableau détaillé** : Une ligne par dette avec numéro, référence, dates, montants
- **Export PDF** : Rapport complet professionnel

## 📄 Exports et rapports

### Format PDF

Le rapport PDF généré contient :

#### Rapport simple (1 dette)
1. **Informations générales** - Dette, date, type, capitalisation
2. **Montant total à régler** (encadré bleu)
3. **Résumé financier** - Détail capital/intérêts/total
4. **Détail des calculs** - Tableau complet par période
5. **Taux d'intérêt appliqués** ✨ - Liste tous les taux utilisés avec base légale
6. **Références légales** - Formule, principes, avertissement

#### Rapport multi-dettes
1. **Informations générales** - Nombre de créances, paramètres
2. **Montant total à régler** (encadré bleu)
3. **Résumé financier global**
4. **Détail par créance** - Tableau récapitulatif compact
5. **Exemple de calcul détaillé** (1ère créance)
6. **Taux d'intérêt appliqués** ✨ - Tous les taux de toutes les périodes
7. **Références légales et méthodologie**

### Caractéristiques du PDF
- ✅ Mise en page professionnelle
- ✅ En-têtes et pieds de page
- ✅ Numérotation des pages
- ✅ Tableaux avec alternance de couleurs
- ✅ Références juridiques complètes
- ✅ Date et heure de génération

## 🔍 Particularités techniques

### Périodes de calcul
- **Avant 2015** : Taux annuel unique pour tous
- **Depuis 2015** : Taux semestriels distincts selon le créancier
  - **S1** : 1er janvier → 30 juin
  - **S2** : 1er juillet → 31 décembre

### Base de calcul
- Année civile de **365 jours** (même les années bissextiles)
- Formule officielle : `Intérêts = (Capital × Taux × Jours) ÷ (365 × 100)`
- Calcul au jour près

### Capitalisation semestrielle
Quand activée :
1. Les intérêts sont calculés pour le semestre
2. À la fin du semestre, les intérêts s'ajoutent au capital
3. Le nouveau capital produit des intérêts pour le semestre suivant
4. Répété jusqu'à la date de calcul

### Majoration judiciaire
- **Déclenchement** : 2 mois après la date du jugement
- **Montant** : +5 points de pourcentage
- **Application** : Sur toutes les périodes suivant le déclenchement
- **Base légale** : Article L.313-3 du Code monétaire et financier

### Historique des taux (référence)

| Période | Particulier | Professionnel |
|---------|-------------|---------------|
| 2025-S2 | 6,65% | 2,76% |
| 2025-S1 | 7,21% | 3,71% |
| 2024-S2 | 8,16% | 4,92% |
| 2024-S1 | 8,01% | 4,92% |
| 2023-S2 | 6,82% | 4,47% |
| 2023-S1 | 3,15% | 3,15% |
| 2022-S2 | 3,15% | 3,15% |
| 2022-S1 | 3,13% | 3,13% |

*Taux complets jusqu'à 2013 intégrés dans l'application*

## ⚠️ Avertissements importants

### 1. Vérification juridique
Ce calculateur est un **outil d'aide à la décision**. Pour toute procédure judiciaire :
- ✅ Faites vérifier les calculs par un professionnel du droit
- ✅ Vérifiez l'applicabilité du taux d'intérêt légal à votre situation
- ✅ Consultez un avocat pour les cas complexes

### 2. Capitalisation des intérêts
L'anatocisme (capitalisation) est soumis à **conditions strictes** :
- Article 1343-2 du Code civil
- Nécessite une mise en demeure ou une demande en justice
- Conditions de délai (généralement 1 an d'intérêts échus)

⚠️ **Ne pas activer sans vérification juridique préalable**

### 3. Prescription
L'outil ne vérifie **PAS** les délais de prescription :
- Prescription de droit commun : 5 ans (art. 2224 C.civ)
- Prescriptions spéciales selon la nature de la créance
- Consultez un professionnel pour vérifier la prescription

### 4. Régimes spéciaux
Certaines créances suivent des règles particulières :
- Baux commerciaux (L. 145-1 et s. C.com)
- Marchés publics (CCP)
- Transactions commerciales (L. 441-10 C.com - pénalités de retard)
- Créances bancaires
- Créances fiscales et sociales

### 5. Pénalités contractuelles
Si le contrat prévoit des pénalités de retard :
- Elles se substituent souvent aux intérêts légaux
- Vérifier la clause du contrat
- Possible cumul selon stipulations

## 🛠️ Dépannage

### Le parser ne détecte pas mes données

**Problème** : Après collage, aucune dette détectée

**Solutions** :
1. Vérifiez que vous avez bien collé les données (pas juste copié)
2. Assurez-vous d'avoir au moins 2 colonnes (montant + date)
3. Vérifiez le format des dates (JJ/MM/AAAA recommandé)
4. Les montants doivent contenir des chiffres
5. Cliquez sur "🔍 Analyser les données" après collage

### Erreurs de parsing

**Problème** : Certaines lignes ne sont pas détectées

**Causes fréquentes** :
- Date dans un format non reconnu (ex: "janvier 2024")
- Montant avec texte (ex: "environ 1000€")
- Ligne d'en-tête non ignorée

**Solution** : Nettoyez les données dans Excel avant de copier

### Le PDF ne se télécharge pas

**Problème** : Clic sur "Télécharger PDF" sans effet

**Solutions** :
1. Vérifiez que les popups ne sont pas bloqués
2. Essayez un autre navigateur
3. Désactivez temporairement les extensions de navigateur
4. Vérifiez l'espace disque disponible

### Calculs incohérents

**Problème** : Les résultats semblent incorrects

**Vérifications** :
1. Date d'exigibilité correcte ?
2. Type de créancier approprié ?
3. Capitalisation voulue ou non ?
4. Majoration judiciaire activée à bon escient ?
5. Période de calcul (trop longue = montants élevés)

## 💡 Conseils d'utilisation

### Bonne pratique 1 : Documentation
- Conservez le PDF généré dans votre dossier
- Notez les paramètres utilisés (capitalisation, jugement)
- Datez vos calculs

### Bonne pratique 2 : Vérification
- Testez avec un cas simple d'abord
- Comparez avec un calcul manuel sur une période courte
- Vérifiez la cohérence des taux appliqués dans le rapport

### Bonne pratique 3 : Import Excel
- Nommez clairement vos références de factures
- Triez par ordre chronologique
- Vérifiez l'aperçu avant de calculer

### Bonne pratique 4 : Mise à jour des taux
- Vérifiez les taux sur [Legifrance](https://www.legifrance.gouv.fr)
- Les nouveaux taux sont publiés :
  - **S1** : Fin décembre pour application au 1er janvier
  - **S2** : Fin juin pour application au 1er juillet

## 📱 Compatibilité

### Systèmes d'exploitation
- ✅ Windows (7, 10, 11)
- ✅ macOS (toutes versions récentes)
- ✅ Linux (toutes distributions)

### Navigateurs
- ✅ Google Chrome (recommandé)
- ✅ Mozilla Firefox
- ✅ Microsoft Edge
- ✅ Safari
- ⚠️ Internet Explorer non supporté

### Appareils
- ✅ Ordinateurs de bureau
- ✅ Ordinateurs portables
- ✅ Tablettes (interface responsive)
- ⚠️ Smartphones (utilisable mais écran petit)

## 🛡️ Sécurité et confidentialité

### Protection des données
- ✅ **Aucune donnée transmise** - Calculs 100% locaux
- ✅ **Pas de serveur** - Fonctionne sans connexion internet
- ✅ **Pas de cookies** - Aucun tracking
- ✅ **Pas de stockage** - Les données ne sont jamais sauvegardées
- ✅ **Open source** - Code source vérifiable

### Confidentialité
Vos données restent sur votre ordinateur :
- Les montants saisis ne quittent jamais votre machine
- Les PDF sont générés localement
- Aucun service externe n'est contacté

## 📊 Exemples d'utilisation

### Exemple 1 : Facture impayée simple

**Contexte** :
- Facture de 10 000€ due le 01/01/2024
- Client professionnel
- Pas de jugement
- Date du calcul : 01/11/2025

**Paramètres** :
- Montant : `10000`
- Date : `01/01/2024`
- Type : `Professionnel`
- Capitalisation : `Non`
- Jugement : `Non`

**Résultat attendu** : Environ 2000€ d'intérêts

---

### Exemple 2 : Condamnation judiciaire

**Contexte** :
- Créance de 50 000€
- Exigible depuis le 01/06/2023
- Jugement du 15/03/2024
- Créancier particulier

**Paramètres** :
- Montant : `50000`
- Date exigibilité : `01/06/2023`
- Type : `Particulier`
- Jugement : `Oui`
- Date jugement : `15/03/2024`
- Capitalisation : `Oui`

**Résultat** : Taux de base jusqu'au 15/05/2024, puis +5 points après

---

### Exemple 3 : Import Excel - Plusieurs factures

**Contexte** :
- 12 loyers impayés sur l'année 2024
- Montant mensuel : 1 500€
- Dates : 31 de chaque mois
- Bailleur particulier

**Données Excel** :
```
Loyer Janvier    1500    31/01/2024
Loyer Février    1500    28/02/2024
Loyer Mars       1500    31/03/2024
...
```

**Procédure** :
1. Copier les 12 lignes depuis Excel
2. Mode "Import Excel"
3. Coller les données
4. Type : Particulier
5. Calculer toutes les dettes

**Résultat** : Rapport global avec total des intérêts sur tous les loyers

## ✅ Checklist avant utilisation en procédure

### Avant de calculer
- [ ] Vérifier la **date d'exigibilité exacte** (contrat, mise en demeure, échéance)
- [ ] Confirmer le **type de créancier** (particulier vs professionnel B2B)
- [ ] Vérifier l'existence d'une **décision de justice** et sa date
- [ ] Contrôler les **conditions de capitalisation** (art. 1343-2 C.civ)
- [ ] S'assurer de l'absence de **régime spécial** applicable
- [ ] Vérifier la **prescription** de la créance

### Après le calcul
- [ ] Vérifier la **cohérence des montants** obtenus
- [ ] Contrôler les **taux appliqués** dans le tableau
- [ ] Vérifier les **dates de changement de taux**
- [ ] Exporter et **conserver le rapport PDF**
- [ ] **Dater et signer** le rapport si usage professionnel
- [ ] Faire **vérifier par un avocat** si montants importants

## 📞 Support et mises à jour

### Mises à jour des taux
Les taux d'intérêt légaux sont publiés par arrêté ministériel :
- **1er semestre** : Publication fin décembre (application 1er janvier)
- **2ème semestre** : Publication fin juin (application 1er juillet)

**Sources officielles** :
- [Legifrance](https://www.legifrance.gouv.fr)
- [Banque de France](https://www.banque-france.fr/statistiques/taux-et-cours/taux-dinteret-legal)
- Journal Officiel de la République Française (JORF)

### Signaler un problème

En cas d'erreur de calcul ou de bug :
1. Notez le **navigateur utilisé** (nom et version)
2. Notez les **données saisies** (montant, dates, options)
3. Notez le **résultat obtenu vs résultat attendu**
4. Conservez une **capture d'écran** si possible

### Évolutions futures

Fonctionnalités envisagées :
- Export Excel natif
- Sauvegarde/chargement de configurations
- Calcul avec taux contractuels personnalisés
- Gestion des devises étrangères
- Mode expert avec paramètres avancés

## 📚 Références juridiques

### Textes principaux
- Code monétaire et financier : Articles L. 313-1 à L. 313-3
- Code civil : Article 1343-2 (capitalisation)
- Loi n° 75-619 du 11 juillet 1975
- Ordonnance n° 2014-947 du 20 août 2014
- Décret n° 2014-1115 du 2 octobre 2014

### Jurisprudence utile
- Cass. com., 28 septembre 2010, n° 09-68.652 (capitalisation)
- Cass. com., 20 mai 2014, n° 13-12.932 (taux applicable)

### Doctrine
- Jurisclasseur Civil Code - Art. 1343 à 1343-5
- Lamy Droit du contrat - Intérêts moratoires

## 📄 Mentions légales

### Limitation de responsabilité
L'auteur ne saurait être tenu responsable :
- Des erreurs de calcul liées à une mauvaise saisie
- De l'utilisation inappropriée de l'outil
- Des conséquences juridiques de l'usage des résultats
- Des mises à jour législatives non intégrées

### Licence
Cet outil est fourni à titre informatif et éducatif. L'utilisation des résultats dans un cadre professionnel ou judiciaire reste sous la responsabilité de l'utilisateur.

### Usage professionnel
Pour un usage professionnel régulier, il est recommandé de :
- Faire valider l'outil par votre service juridique
- Conserver des logs des calculs effectués
- Mettre en place un processus de double vérification

---

## 🎯 Résumé rapide

| Action | Mode unique | Mode Excel |
|--------|-------------|------------|
| **1 dette** | ✅ Optimal | Possible |
| **2-5 dettes** | Possible | ✅ Recommandé |
| **6+ dettes** | Fastidieux | ✅✅ Obligatoire |
| **PDF détaillé** | ✅ Complet | ✅ Synthétique |
| **Temps** | 2 minutes | 30 secondes |

**En un mot** : Mode unique pour les cas isolés, mode Excel pour le traitement en masse.

---

**Version du document** : 3.0  
**Dernière mise à jour** : Novembre 2025  
**Taux à jour** : S2 2025 (Arrêté du 19 juin 2025)

---

*Cet outil est fourni à titre informatif. Pour toute procédure judiciaire, il est recommandé de faire vérifier les calculs par un professionnel du droit.*
