
## 🧠 1. `console.log()`

### 📘 Définition :

Affiche un message dans la **console du navigateur** (outil de débogage pour les développeurs).
➡️ Sert à vérifier les valeurs des variables, tester du code, etc.

### 💻 Exemple :

```js
let nom = "Mounir";
console.log("Bonjour " + nom);
```

### 🔍 Explication :

* `let nom = "Mounir";` → on crée une variable `nom`.
* `console.log(...)` → affiche dans la console :
  👉 **Bonjour Mounir**

---

## 🧠 2. `document.write()` et `document.writeln()`

### 📘 Définition :

Ces deux méthodes **écrivent directement dans la page HTML**.

* `document.write()` → écrit sans saut de ligne.
* `document.writeln()` → écrit **avec un saut de ligne** à la fin.

### 💻 Exemple :

```js
document.write("Bonjour");
document.writeln("Mounir");
document.write("Bienvenue !");
```

### 🔍 Résultat affiché dans la page :

```
BonjourMounir
Bienvenue !
```

### ⚠️ Attention :

À éviter dans les vrais sites modernes, car cela peut **effacer le contenu du document** si exécuté après le chargement de la page.

---

## 🧠 3. `alert()` et `window.alert()`

### 📘 Définition :

Affiche une **boîte de dialogue** à l’écran avec un message.
Les deux sont identiques (`window.alert` est la version complète).

### 💻 Exemple :

```js
alert("Salut Mounir !");
window.alert("Bienvenue sur mon site !");
```

### 🔍 Explication :

Le navigateur montre une petite fenêtre modale avec le texte.

---

## 🧠 4. `document.getElementById()`

### 📘 Définition :

Permet de **sélectionner un élément HTML** grâce à son attribut `id`.

### 💻 Exemple :

HTML :

```html
<p id="message">Bonjour</p>
```

JS :

```js
let element = document.getElementById("message");
console.log(element);
```

### 🔍 Explication :

* Le navigateur cherche l’élément avec `id="message"`.
* On peut ensuite modifier ou lire son contenu.

---

## 🧠 5. `innerHTML`, `innerText`, `textContent`

| Propriété     | Description                                                                   | Garde les balises HTML ? |
| ------------- | ----------------------------------------------------------------------------- | ------------------------ |
| `innerHTML`   | Récupère ou modifie le **contenu HTML** d’un élément                          | ✅ Oui                    |
| `innerText`   | Récupère ou modifie uniquement le **texte visible** (respecte les styles CSS) | ❌ Non                    |
| `textContent` | Récupère ou modifie **tout le texte brut**, même caché                        | ❌ Non                    |

### 💻 Exemple :

HTML :

```html
<p id="exemple"><b>Salut</b> Mounir</p>
```

JS :

```js
let el = document.getElementById("exemple");

console.log(el.innerHTML);   // "<b>Salut</b> Mounir"
console.log(el.innerText);   // "Salut Mounir"
console.log(el.textContent); // "Salut Mounir"
```

### 🔍 Explication :

* `innerHTML` garde les balises `<b>`.
* `innerText` et `textContent` ne gardent que le texte.

---

## 🧠 6. `document.` et `window.`

* `document` → représente **la page HTML** (DOM = Document Object Model).
* `window` → représente **la fenêtre du navigateur** (tout le contexte global).

Exemples :

```js
window.alert("Hello !");
document.write("Texte ajouté dans la page !");
```

Ici :

* `window.alert` → agit sur la fenêtre entière.
* `document.write` → agit sur le contenu du document.

---

## ✅ **Résumé rapide :**

| Commande                                  | Fonction principale                | S’affiche où ? |
| ----------------------------------------- | ---------------------------------- | -------------- |
| `console.log()`                           | Affiche un message dans la console | Console        |
| `document.write()`                        | Écrit dans la page HTML            | Page           |
| `alert()`                                 | Affiche une alerte modale          | Fenêtre        |
| `document.getElementById()`               | Sélectionne un élément HTML        | —              |
| `innerHTML` / `innerText` / `textContent` | Lis ou modifie le contenu          | —              |
| `document.`                               | Représente la page                 | —              |
| `window.`                                 | Représente la fenêtre              | —              |

---

## 💡 Exemple complet combiné :

HTML :

```html
<!DOCTYPE html>
<html lang="fr">
<body>
  <h1 id="titre">Bonjour</h1>
  <script>
    let titre = document.getElementById("titre");
    console.log(titre.innerText); // affiche "Bonjour"
    titre.innerHTML = "<b>Salut Mounir !</b>"; // change le texte
    alert("Titre changé !");
    document.write("Texte ajouté à la page");
  </script>
</body>
</html>
```

### 🔍 Explication :

1. On récupère l’élément `<h1>`.
2. On affiche son texte dans la console.
3. On change son contenu en gras.
4. On affiche une alerte.
5. On ajoute un texte dans la page.

---

## 🧩 **25 Exercices (pratiques et progressifs)**

**Niveau 1 — Bases (console, alert, write)**

1. Affiche "Bonjour tout le monde" dans la console.
2. Affiche "Bienvenue sur mon site" avec `alert()`.
3. Écris "Hello" dans la page avec `document.write()`.
4. Fais une alerte avec le nom de l’utilisateur (stocké dans une variable).
5. Affiche la somme de 5 + 10 dans la console.

**Niveau 2 — DOM et sélections**
6. Crée un paragraphe avec `id="texte"` et affiche-le dans la console.
7. Change le texte d’un paragraphe en "Salut Mounir !" via JS.
8. Utilise `innerHTML` pour ajouter `<b>Bonjour</b>` dans un paragraphe.
9. Affiche la différence entre `innerText` et `innerHTML`.
10. Écris dans la page le texte contenu dans un élément récupéré.

**Niveau 3 — Interactions**
11. Demande le prénom de l’utilisateur (avec `prompt()`) et affiche-le avec `alert()`.
12. Affiche le contenu d’un `<div>` dans la console.
13. Change le texte d’un bouton quand on clique dessus.
14. Utilise `textContent` pour afficher du texte sans HTML.
15. Écris le résultat d’un calcul directement dans la page.

**Niveau 4 — Mélange (window, document)**
16. Utilise `window.alert` au lieu de `alert`.
17. Affiche la largeur de la fenêtre avec `window.innerWidth`.
18. Écris le titre du document (`document.title`) dans la console.
19. Change le titre de la page.
20. Utilise `document.write()` pour écrire le nom de la page.

**Niveau 5 — Petits mini-projets**
21. Crée un bouton qui affiche un `alert()` quand on clique.
22. Crée un script qui affiche dans la console le texte d’un paragraphe.
23. Crée un bouton qui change le texte d’un `<p id="test">`.
24. Affiche la date actuelle dans la page avec `document.write()`.
25. Combine tout : `console.log`, `alert`, `innerHTML` dans une même page.

---


