# # Où est le HTML ?

## Il se trouve ici

En général :
```` js
switch (page) {
        case "landing-page":
          mainPanel.innerHTML = `
// ICI IL Y AS LE HTML QUI VAS DANS MAIN PANEL
````
Il est ouvert par le case qui définit la page à afficher :
````js
case "landing-page":
`````
…et il se ferme à chaque break :
````js
break;
````
## La page est affichée depuis cette fonction :
````js
const params = new URLSearchParams(window.location.search);
const page = params.get("page") || "landing-page";
const mainPanel = document.querySelector(".main_panel");
let actorsData = [];

// Cette partie récupère les arguments de l'URL, ex : ?page=s01
````
Ensuite, la page est choisie par :
````js
switch (page)
// 'page' est l’argument intercepté juste au-dessus
````
Informations supplémentaires :
la page default (
````js
default:
````
)
est la page 404 