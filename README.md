# n8n - Automatisation du traitement des notes

Mini-projet réalisé dans le cadre de mon apprentissage de Docker et n8n.

## 🎯 Objectif

Automatiser le traitement d'un fichier Excel contenant les notes d'étudiants.

Le workflow permet de :

- Lire un fichier Excel
- Extraire les données
- Vérifier les notes
- Séparer les étudiants admis et non admis
- Générer deux fichiers Excel

## ⚙️ Technologies

- Docker
- Docker Compose
- n8n
- Excel / XLSX

## 🔄 Workflow

Excel
↓
Read File
↓
Extract From File
├── IF
   ├── TRUE → Admis → admis.xlsx
   └── FALSE → Non admis → non-admis.xlsx

## 🐳 Exécution avec Docker

Cloner le repository :

```bash
git clone https://github.com/Mandroro/n8n-excel-automation-note-etudiant.git
cd n8n-excel-automation