# ✅ Class Draw — Tirage au sort pour le passage au tableau

Une petite application web moderne permettant à un professeur de tirer au sort, de façon aléatoire et **sans répétition**, l'étudiant qui passe au tableau.

Le site est conçu pour être utilisé facilement en classe, notamment sur un vidéoprojecteur ou un écran partagé.

## ✨ Fonctionnalités

- 🎯 Tirage aléatoire sans répétition pendant un cycle
- 👨‍🎓 Nombre d'étudiants personnalisable (1 à 200)
- 🏫 Filière / classe personnalisable
- ✍️ Ajout des noms des étudiants, un par ligne
- 🔢 Association automatique des noms avec N1, N2, N3, etc.
- 📜 Historique des tirages
- ↶ Annulation du dernier tirage
- 🔄 Nouveau cycle
- 🖥️ Mode tableau pour vidéoprojecteur
- ⛶ Mode plein écran
- 🔊 Son activable / désactivable
- 💾 Sauvegarde automatique de la configuration dans le navigateur
- 📥 Import de listes TXT / CSV / JSON
- 📤 Export de la configuration de la classe en JSON
- ⌨️ Raccourcis clavier

## 🛠️ Technologies

Projet volontairement simple et léger, sans framework ni backend :

- HTML5
- CSS3
- JavaScript vanilla
- LocalStorage pour la sauvegarde locale

Aucune base de données et aucune installation de dépendances ne sont nécessaires.

## 🚀 Utilisation locale

### Méthode 1 — la plus simple

1. Télécharger le projet.
2. Ouvrir le fichier `index.html` avec Chrome, Edge ou Firefox.
3. Cliquer sur **Configuration**.
4. Renseigner le nom de la filière ou de la classe.
5. Choisir le nombre d'étudiants.
6. Saisir les noms, un par ligne.
7. Cliquer sur **Enregistrer la classe**.
8. Lancer le tirage avec **Tirer au sort** ou avec la touche **Espace**.

Exemple :

```text
Filière : GLD
Nombre d'étudiants : 27

N1  →  Nom Étudiant 1
N2  →  Nom Étudiant 2
N3  →  Nom Étudiant 3
...
N27 →  Nom Étudiant 27
```

### Méthode 2 — avec un serveur local

Pour lancer le site via un petit serveur HTTP Python :

```bash
cd chemin/vers/le/projet
python -m http.server 8000
```

Puis ouvrir :

```text
http://localhost:8000
```

Cette méthode est pratique lorsque l'on souhaite tester le projet comme un véritable site web local.

## ⌨️ Raccourcis clavier

| Touche | Action |
|---|---|
| `Espace` | Tirer au sort |
| `F` | Activer / quitter le mode tableau |
| `R` | Nouveau cycle |
| `C` | Ouvrir la configuration |
| `Ctrl + Z` | Annuler le dernier tirage |

## 📥 Importer une liste d'étudiants

La configuration permet d'importer une liste depuis un fichier `.txt`, `.csv` ou `.json`.

Pour un fichier texte, utiliser un nom par ligne :

```text
Ahmed
Yassine
Sara
Imane
Hamza
```

Le nombre de lignes importées est adapté à la configuration du nombre d'étudiants.

## 📤 Exporter une classe

La configuration de la classe peut être exportée en JSON afin de conserver ou partager une liste d'étudiants.

Exemple de structure :

```json
{
  "program": "GLD",
  "count": 27,
  "names": [
    "Ahmed",
    "Yassine",
    "Sara"
  ]
}
```

## 🔒 Données et confidentialité

Les noms des étudiants sont enregistrés uniquement dans le **LocalStorage du navigateur utilisé**.

L'application n'envoie pas les noms vers un serveur et ne nécessite aucune base de données.

⚠️ Si vous utilisez GitHub Pages, ne publiez pas dans le dépôt des données personnelles ou une liste réelle d'étudiants. Le code peut être public, mais les listes de classe doivent rester locales ou être importées directement dans le navigateur.

## 🌐 Publier avec GitHub Pages

Le projet est un site statique : `index.html` peut donc être publié avec GitHub Pages.

### 1. Créer le dépôt

Sur GitHub, créer un nouveau repository, par exemple :

```text
class-draw
```

Placez `index.html` et `README.md` directement à la racine du repository.

### 2. Envoyer le projet avec Git

Dans le dossier du projet :

```bash
git init
git add .
git commit -m "Initial commit - Class Draw"
git branch -M main
git remote add origin https://github.com/VOTRE-USERNAME/class-draw.git
git push -u origin main
```

Remplacer `VOTRE-USERNAME` par votre nom d'utilisateur GitHub.

### 3. Activer GitHub Pages

Dans le repository GitHub :

**Settings → Pages → Build and deployment → Source → Deploy from a branch**

Puis choisir :

```text
Branch: main
Folder: / (root)
```

Enregistrer. GitHub Pages pourra ensuite fournir l'URL publique du site.

## 📁 Structure du projet

```text
class-draw/
├── index.html
└── README.md
```

## 🎓 Cas d'utilisation

Cette application peut être utilisée pour :

- passage au tableau ;
- présentation orale ;
- interrogations aléatoires ;
- participation en classe ;
- tirage de groupes ou de rôles ;
- activités pédagogiques nécessitant une sélection aléatoire.

## 📌 Idée du projet

L'objectif est de transformer un tirage au sort classique en une petite expérience de classe plus fluide, visuelle et interactive, tout en gardant une utilisation extrêmement simple pour l'enseignant.

---

Made for classroom use 🎓
