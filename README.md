# n8n - Automatisation du traitement des notes

Mini-projet réalisé dans le cadre de mon apprentissage de **Docker** et **n8n**.

## 🎯 Objectif

Automatiser le traitement d'un fichier Excel contenant les notes d'étudiants.

Le workflow permet de :

* Lire un fichier Excel
* Extraire les données
* Vérifier automatiquement les notes
* Séparer les étudiants admis et non admis
* Générer deux fichiers Excel : `Etudiant-admis.xlsx` et `Etudiant-non-admis.xlsx`

## ⚙️ Technologies

* Docker
* Docker Compose
* n8n
* Excel / XLSX

## 🔄 Workflow

Le workflow suit le processus suivant :

```text
Fichier Excel
     ↓
Lecture du fichier
     ↓
Extraction des données
     ↓
       IF
      /  \
    TRUE FALSE
     ↓     ↓
  Admis  Non admis
     ↓     ↓
 admis.xlsx  non-admis.xlsx
```


## 📥 Récupération du projet

Cloner le repository :

```bash
git clone https://github.com/Mandroro/n8n-excel-automation-note-etudiant.git
cd n8n-excel-automation-note-etudiant
```

## 🐳 Exécution avec Docker

Lancer n8n avec Docker Compose :

```bash
docker compose up -d
```

Vérifier que le conteneur est en cours d'exécution :

```bash
docker ps
```

## 🌐 Ouvrir n8n en local

Une fois le conteneur lancé, accéder à :

```text
http://localhost:5678
```

## 📂 Importer le workflow

Une fois n8n ouvert dans le navigateur :

1. Ouvrir l'interface n8n.
2. Créer un nouveau workflow ou accéder au menu d'importation.
3. Importer le fichier JSON présent dans le dossier `workflows`.
4. Vérifier les nodes et leurs connexions.
5. Exécuter le workflow.

> ⚠️ Le workflow utilise un fichier Excel local. Il est donc nécessaire d'adapter le chemin du fichier et la configuration du volume Docker à votre environnement.

## 📁 Structure du projet

```text
n8n-excel-automation-note-etudiant/
│
├── docker-compose.yml
├── README.md
│
├── workflows/
│   └── student-automation.json
│
├── data/
│   └── Note-etutiant.xlsx
│
└── screenshots/
    └── workflow.png
```

## 📚 Objectifs d'apprentissage

Ce mini-projet m'a permis de pratiquer :

* Les conteneurs Docker
* Les volumes Docker
* Le partage de fichiers entre l'hôte et le conteneur
* La création de workflows avec n8n
* Les expressions n8n
* Les conditions `IF`
* Le traitement de fichiers Excel
* La génération automatique de fichiers
