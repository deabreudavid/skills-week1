# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'état (_state_) pour contrôler l'affichage d'un composant ✔️
- les composants enfants et les _props_ qu'on leur passe ✔️
- le déclenchement d'instructions en fonction des actions de l'utilisateur  ✔️
- le déclenchement d'instructions en fonction de l'étape du cycle de vie du composant ou du changement de valeur de ses props ❌ / ✔️ Encore fragile dans l'explication
- l'usage d'un reducer (_useReducer_) pour gérer un état composé dans un composant ❌ / ✔️ Encore fragile dans l'explication
- l'état stocké dans un composant avec un _context provider_ et accessible dans ses descendants via `useContext` ❌ / ✔️ Encore fragile dans l'explication

## 💻 J'utilise

### Un exemple personnel commenté  ✔️

### Utilisation dans un projet  ✔️

[lien github]

voici une copie exemple: 

import html2canvas from "html2canvas";
import Board from "./Board";

import canvasToImage from 'canvas-to-image';
import '../../../App.css';
import { confirmAlert } from 'react-confirm-alert'; // Import
import 'react-confirm-alert/src/react-confirm-alert.css'; // Import css
import { useEffect } from "react";

export default function MainBoard({imagedimensions,mesConditions,monTab,time,tabCH,check,mesTemperatures,imUr,typeaffichage,typeAnita}) {
  useEffect(() => {
    window.scrollTo(0, 0)
  })
  // mesconditions c'est une liste contient les conditions avec la variable de la condition , et la couleur de l'hexagone et la couleur du text du hexagone
  // la derniere ligne de mesconditions contient [0] la premiere minute de l'animation et [1] la derniere minute de l'animation
  // typeaffichage pour savoir si on affiche la temperature dans l'hexagone ou bien la difference entre temp et sp
  // imUr l'url de l'image du background
  // mesTemperatures tableau qui contients toutes les informations du csv 
  // check si false donc on est dans le placement des TC si non on est dans l'animation
  // monTab contient x y de chaque TC qu'on a place
  // tabCH pour savoir le tc le plus chaud et le plus froid


  /* const Screen = () => {
    const [showResults, setShowResults] = useState(false)
    const onClick = () => {setShowResults(!showResults);
      if(!showResults)
      {html2canvas(document.querySelector("#capture")).then(canvas => {
           document.getElementById("targetimg").append(canvas);
          return canvasToImage(canvas, {
            name: 'myImage',
            type: 'png',
            quality: 1
          });
        }); } 
    }
   
    return (
      <div className="clock-holder" >
        <div className='container'>
      
      </div>
        <input type="submit" value="Capture" onClick={onClick} />
        { showResults ? <div className="stopwatch" > <a class="close" href="#">&times;</a><div  className="search-results">
        <span style={{ background:"Red", color: "#fff" }}>
        {time.m}</span>
        
    </div><button>save</button>
        <button>cancel</button></div>
     : null }
      </div>
    )
  }*/
  const submit = () => {
      try {
    confirmAlert({
      title: 'Download a screenshot of the animation',
      message: 'Download a picture of the animtation at H:M '+time.m+":"+time.s+" ?.",
      buttons: [
        {
          label: 'Yes',
          onClick: () => {html2canvas(document.querySelector("#capture")).then(canvas => {
           
           return canvasToImage(canvas, {
             name: 'animation'+time.m+time.s,
             type: 'png',
             quality: 1
           });
         }); }
        },
        {
          label: 'No'
        }
      ]
    });}
    catch(e){
      confirmAlert({
        title: 'Download a screenshot of the TCs placement',
        message: 'Are you sure you want to take a picture of the TCs placement ? ',
        buttons: [
          {
            label: 'Yes',
            onClick: () => {html2canvas(document.querySelector("#capture")).then(canvas => {
             
             return canvasToImage(canvas, {
               name: 'animation',
               type: 'png',
               quality: 1
             });
           }); }
          },
          {
            label: 'No'
          }
        ]
      });}
  };

/*
 <label htmlFor="icon-button-file">
        <IconButton color="primary" aria-label="upload picture"  onClick={submit} component="span">
          <PhotoCamera />
        </IconButton>
      </label>
*/
    return <div>
     
     <div id="capture"
    style={{
        backgroundImage: `url(${imUr})`,
        width: imagedimensions[0],
        height: imagedimensions[1],
        backgroundRepeat : 'no-repeat',
        backgroundSize: 'contain',
        backgroundPosition: 'center',
        WebkitBackgroundSize : 'contain',
        MozBackgroundSize : 'contain',
        OBackgroundSize : 'contain',
    }}
  >
    
    <Board  mesConditions={mesConditions} tabCH={tabCH} monTab={monTab} typeaffichage={typeaffichage}  time={time} check={check} mesTemperatures={mesTemperatures} typeAnita={typeAnita}></Board>
    
  </div>
  </div>
  }


Description :

### Utilisation en production si applicable❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ / ✔️

Description :

## 🌐 J'utilise des ressources

### Titre

- lien
- description

## 🚧 Je franchis les obstacles

### Point de blocage ❌ / ✔️

Description: L'autonomie reste un grand problème de mon coté. En entreprise je suis le seul dev et parfois cest assez pesant car je n'ai personne qui me tire vers le haut. Je fais beaucoup de debug et d'amélioration sur du code qui n'est pas le mien mais je fais rarement de la création seul ou accompagné.

Plan d'action : (à valider par le formateur)

- action 1 ❌ / ✔️
- action 2 ❌ / ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌ / ✔️
- J'ai fait une [présentation](...) ❌ / ✔️
