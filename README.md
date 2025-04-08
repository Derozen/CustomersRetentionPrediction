## 📊 Telco Customer Churn Dataset

Ce projet utilise le dataset **Telco Customer Churn** pour prédire si un client se désabonnera ou non d’un service de télécommunication.

### 🎯 Objectif

Prédire le **churn client** (désabonnement) à partir de caractéristiques personnelles, contractuelles, et d’usage du service.  
La variable cible est `Churn` (Yes / No).

---

### 📁 Description du dataset

- **Nombre d’entrées** : 7043 clients  
- **Nombre de colonnes** : 21  
- **Type de problème** : Classification binaire

| Colonne              | Description |
|----------------------|-------------|
| `customerID`         | Identifiant unique du client |
| `gender`             | Sexe du client (`Male`, `Female`) |
| `SeniorCitizen`      | 1 si client est senior (>= 65 ans), 0 sinon |
| `Partner`            | A un partenaire (`Yes`, `No`) |
| `Dependents`         | A des personnes à charge (`Yes`, `No`) |
| `tenure`             | Nombre de mois en tant que client |
| `PhoneService`       | A un service de téléphone (`Yes`, `No`) |
| `MultipleLines`      | A plusieurs lignes (`Yes`, `No`, `No phone service`) |
| `InternetService`    | Type de connexion Internet (`DSL`, `Fiber optic`, `No`) |
| `OnlineSecurity`     | A un service de sécurité en ligne (`Yes`, `No`, `No internet service`) |
| `OnlineBackup`       | A un service de sauvegarde en ligne |
| `DeviceProtection`   | A une protection d'appareil |
| `TechSupport`        | A un support technique |
| `StreamingTV`        | A la télévision en streaming |
| `StreamingMovies`    | A les films en streaming |
| `Contract`           | Type de contrat (`Month-to-month`, `One year`, `Two year`) |
| `PaperlessBilling`   | Facturation sans papier (`Yes`, `No`) |
| `PaymentMethod`      | Méthode de paiement (`Electronic check`, `Mailed check`, etc.) |
| `MonthlyCharges`     | Montant mensuel facturé |
| `TotalCharges`       | Total payé depuis le début |
| `Churn`              | **Variable cible** : le client a-t-il quitté ? (`Yes`, `No`) |

---

### 🧹 Prétraitement effectué

- Suppression de la colonne `customerID`
- Conversion de `TotalCharges` en float (certaines valeurs étaient invalides)
- Encodage :
  - Label Encoding pour les colonnes binaires
  - One-Hot Encoding pour les colonnes catégorielles multiples
- Gestion des valeurs manquantes
- Split des données en **train/test**

---

### 🔍 Source des données

- [IBM Sample Dataset - Telco Churn (Kaggle)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

