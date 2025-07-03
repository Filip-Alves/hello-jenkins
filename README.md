# Hello Jenkins

Un exemple minimal de CI/CD avec Jenkins, qui exécute un simple `Hello World` dans un pipeline déclaratif.

---

## 🚀 Objectif

Mettre en place une intégration continue simple avec Jenkins utilisant un `Jenkinsfile` et un pipeline déclencheur à chaque commit.

---

## 📦 Prérequis

- Java JDK 8+
- Git
- Jenkins (`jenkins.war` téléchargé depuis https://www.jenkins.io/download/)

---

## ⚙️ Lancement de Jenkins

Dans le dossier où se trouve `jenkins.war`, exécuter :

```
java -jar jenkins.war --httpPort=8080
```

Puis ouvrir Jenkins à l'adresse :  
http://localhost:8080

---

## 📁 Arborescence minimale du projet

```
hello-jenkins/
├── Jenkinsfile
```

---

## 🛠 Contenu du `Jenkinsfile`

```
pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
```

---

## ✅ Étapes réalisées

1. Création d’un dépôt GitHub vide.
2. Ajout d’un fichier `Jenkinsfile` à la racine.
3. Lancement local de Jenkins avec `jenkins.war`.
4. Création d’un **Multibranch Pipeline** dans l'interface Jenkins.
5. Ajout du dépôt GitHub comme source dans Jenkins.
6. Lancement du scan → Jenkins détecte `Jenkinsfile` → exécution automatique.
7. Résultat attendu dans la console : `Hello World`.

---

## 🔁 Pour tester

1. Modifier un fichier.
2. Commit & push (`git add`, `commit`, `push`).
3. Jenkins détectera la mise à jour → relance du pipeline.

---

## 📚 Liens utiles

- Jenkins Hello World : https://www.jenkins.io/doc/pipeline/tour/hello-world/
- Syntaxe pipeline : https://www.jenkins.io/doc/book/pipeline/syntax/

---
