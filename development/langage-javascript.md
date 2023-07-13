# Langage Javascript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les `structures` de base du langage ✔️
- les normes `ecmascript` ✔️ Normalisation du code
- l'utilisation de l'`asynchrone` ✔️ Permet de demarrer une tache plus ou moins longue tout en continuant de pouvoir réagir aux autres evenements. 

Exemple (moyen de mieux comprendre):
etape1: Je branche ma cafetiere
etape2: je mets de l'eau
etape3: je fais chauffer l'eau
a ce moment la leau continue de chauffer mais en meme temps que cela se produit je prépare ma capsule, ma tasse...
etape4: je fais couler le café
etape5: je bois mon café

au niveau de mon étape trois je peux continuer le processus en continuant de préparer mon café
l'étape3 ne me bloque pas. 

- les spécifités du mot-clef `this` ❌

## 💻 Je code en Javascript

### Un exemple de code commenté ✔️ Tiré des révisions JS de mon GITHUB

const title1 = document.querySelector("h1");
const title2 = document.querySelector("h2");
const box = document.querySelector(".box");
const list = document.querySelector("ul");
const img = document.querySelector("img");
const form = document.querySelector("form");
const input = document.querySelector("#test");

//innerText permet d'ajouter du texte

title1.innerText = "ajout1 de texte";

//textContent permet d'ajouter du texte

title2.textContent = "ajout2 de texte";

//innerHTML ajoute du HTML
box.innerHTML = `<p>Hey html</p>`;

//creer des elements HTML
let newLi = document.createElement("li");
newLi.innerText = "new LI";
list.appendChild(newLi);

//replaceWith pour choisir l'ordre de l'élément
list.children[1].replaceWith(newLi);

//style changement de couleur de la box
box.style.background = "#333";

//changement de source d'image accèder à l'attribut image
img.src =
  "https://images.unsplash.com/photo-1675410541565-af66672ad1f9?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHx0b3BpYy1mZWVkfDN8Ym84alFLVGFFMFl8fGVufDB8fHx8&auto=format&fit=crop&w=1100&q=60";

form.addEventListener("submit", (e) => {
  e.preventDefault();
  let val = input.value;
  console.log(val);
  title1.innexText = `${val}`;
});

//récupérer les coordonnées de la souris

const cor = document.querySelector(".cor");
let y = 0;
let x = 0;

window.addEventListener("mousemove", (even) => {
  x = even.clientX;
  y = even.clientY;

  cor.textContent = `X : ${x} Y ${y}`;
});

### Utilisation dans un projet ✔️

[lien github](https://github.com/deabreudavid/FullJS)

Description : Ce repository GITHUB me permet d'avancer en parallèle sur les basics et fondamentaux de JS a un petit niveau. 

### J'ai utilisé ce langage en production ❌

[lien du projet](...)

Description :

### J'ai utilisé ce langage en environement professionnel ✔️

Description : J'ai pu utiliser ce langage de façon assez basique pour corriger des bugs de fonctionnement des applications de l'entreprise. Cependant je ne peux le partager car je n'ai pas la main sur les répos

## 🌐 J'utilise des ressources

### Titre

- lien
- description

## 🚧 Je franchis les obstacles

### Point de blocage ❌ 

Description: Les termes ne sont pas maitrisés encore. Bien que je sache appliqué les principes fondamentaux il est encore difficile pour moi d'expliquer les choses.

Plan d'action : (à valider par le formateur)

- action 1 ❌ / ✔️
- action 2 ❌ / ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](https://github.com/deabreudavid/FullJS)  ✔️

J'ai réalisé un repository github afin de revoir les fondamentaux depuis le début et je poursuis dès que j'ai un peu de temps

- J'ai fait une [présentation](...) ❌ / ✔️

