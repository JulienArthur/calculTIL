# Calculateur d'Intérêts de Retard - Guide d'utilisation

## 📋 Description

Cette application web permet de calculer automatiquement les intérêts de retard selon le **taux d'intérêt légal français**. Elle est conçue pour les professionnels du droit (avocats, juristes, huissiers) et toute personne devant calculer des intérêts moratoires conformément à la réglementation française.

## ⚖️ Cadre légal

L'application se base sur :
- **Articles L. 313-2 et suivants** du Code monétaire et financier
- **Article L. 313-3 CMF** - Majoration de 5 points en cas de condamnation
- **Loi n° 75-619 du 11 juillet 1975**, article 3
- **Ordonnance n° 2014-947 du 20 août 2014** (réforme du taux)
- **Décret n° 2014-1115 du 2 octobre 2014** (modalités de calcul)

### Taux actuels (1er semestre 2025)
- **Créancier particulier** : 7,21%
- **Créancier professionnel** : 3,71%

## 🚀 Installation et utilisation

### Méthode simple (recommandée)
1. **Téléchargez** le fichier `Calculateut_TIL_v2.html`
2. **Double-cliquez** sur le fichier pour l'ouvrir dans votre navigateur
3. L'application fonctionne **entièrement hors ligne** - aucune connexion internet requise

### Configuration requise
- Navigateur moderne (Chrome, Firefox, Safari, Edge)
- Aucune installation supplémentaire nécessaire

## 📖 Guide d'utilisation

### 1. Informations de base

#### Montant de la dette
- Saisissez le montant principal de la créance en euros
- Utilisez le point ou la virgule pour les décimales

#### Date d'exigibilité
- Date à partir de laquelle les intérêts commencent à courir
- Généralement : date de mise en demeure, date d'échéance impayée, ou date fixée par contrat

#### Type de créancier
- **Particulier** : Personne physique n'agissant pas dans le cadre professionnel
- **Professionnel** : Entreprise, commerçant, artisan, profession libérale

### 2. Options de calcul

#### Capitalisation des intérêts
- **Activée** : Les intérêts sont ajoutés au capital à chaque fin de semestre (anatocisme)
- **Désactivée** : Intérêts simples calculés uniquement sur le capital initial

**Important** : La capitalisation est soumise aux conditions de l'article 1343-2 du Code civil

#### Condamnation judiciaire
Si une décision de justice a été rendue :
1. Activez l'option "Jugement prononcé"
2. Indiquez la date du jugement
3. La majoration de **5 points** s'applique automatiquement **2 mois après** le jugement (Art. L.313-3 CMF)

### 3. Événements additionnels

Permet d'ajouter des événements modifiant le capital :
- **Paiements partiels** : réduisent le capital
- **Nouveaux impayés** : augmentent le capital
- **Frais de justice** : peuvent être ajoutés au principal

Pour chaque événement :
1. Date de l'événement
2. Montant (positif pour ajout, négatif pour réduction)
3. Description claire

### 4. Résultats et exports

#### Lecture des résultats
- **Dette initiale** : Montant de départ
- **Intérêts totaux** : Somme des intérêts calculés
- **Total à payer** : Dette + intérêts (+ événements)

#### Exports disponibles
- **PDF** : Rapport complet avec références légales
- **Excel** : Tableaux détaillés pour vérification/personnalisation

## 🔍 Particularités techniques

### Périodes de calcul
- **Avant 2015** : Taux annuel unique
- **Depuis 2015** : Taux semestriels distincts (S1 : janvier-juin, S2 : juillet-décembre)

### Base de calcul
- Année civile de **365 jours** (même les années bissextiles)
- Formule : `Intérêts = (Capital × Taux × Jours) ÷ (365 × 100)`

### Précision
- Calcul au jour près
- Arrondis à 2 décimales pour les montants

## ⚠️ Avertissements importants

1. **Vérification** : Ce calculateur est un outil d'aide. Vérifiez toujours les calculs pour les procédures judiciaires.

2. **Capitalisation** : L'anatocisme est soumis à conditions légales strictes. Consultez l'article 1343-2 du Code civil.

3. **Prescription** : L'outil ne vérifie pas les délais de prescription applicables.

4. **Cas particuliers** : Certaines créances suivent des régimes spéciaux (baux commerciaux, marchés publics, etc.)

## 📱 Compatibilité

- ✅ Windows, Mac, Linux
- ✅ Chrome, Firefox, Safari, Edge
- ✅ Fonctionne hors ligne
- ✅ Responsive (ordinateur, tablette, mobile)

## 🛡️ Sécurité et confidentialité

- **Aucune donnée transmise** : Tous les calculs sont effectués localement
- **Pas de stockage** : Les données ne sont pas sauvegardées
- **Open source** : Code source visible et vérifiable

## 📞 Support et évolutions

### Signaler un problème
En cas d'erreur de calcul ou de bug, notez :
- Le navigateur utilisé
- Les données saisies
- Le résultat obtenu vs attendu

### Mises à jour des taux
Les taux d'intérêt légaux sont publiés par arrêté ministériel :
- **1er semestre** : Publication fin décembre
- **2ème semestre** : Publication fin juin

Vérifiez sur [Legifrance](https://www.legifrance.gouv.fr) ou le site de la Banque de France.

## 📝 Exemples d'utilisation

### Cas 1 : Facture impayée simple
- Facture de 10 000€ due le 01/01/2024
- Créancier professionnel
- Pas de jugement
- → Calcul direct des intérêts jusqu'à aujourd'hui

### Cas 2 : Condamnation judiciaire
- Créance de 50 000€
- Jugement du 01/03/2024
- Majoration automatique à partir du 01/05/2024 (+2 mois)
- → Taux majoré de 5 points appliqué

### Cas 3 : Paiements échelonnés
- Dette initiale 20 000€
- Paiement partiel de 5 000€ le 01/06/2024
- Ajout de frais de 1 000€ le 01/09/2024
- → Calcul ajusté selon l'évolution du capital

## ✅ Checklist avant utilisation en procédure

- [ ] Vérifier la date d'exigibilité exacte
- [ ] Confirmer le type de créancier (particulier/professionnel)
- [ ] Vérifier l'existence d'une décision de justice
- [ ] Contrôler les conditions de capitalisation (art. 1343-2 C.civ)
- [ ] S'assurer de l'absence de régime spécial applicable
- [ ] Exporter et conserver le rapport PDF pour le dossier

---

**Note** : Cet outil est fourni à titre informatif. Pour toute procédure judiciaire, il est recommandé de faire vérifier les calculs par un professionnel du droit.