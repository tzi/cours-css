# Responsive

Le responsive est le fait d'adapter un site internet aux différents type d'appareils, notamment aux téléphones.

## Activer le responsive

Par défaut, les navigateurs mobiles va partir du principe que votre site internet n'est pas adapté aux téléphones portables. Ainsi, ils vont afficher les sites web avec une largeur de `1024px` (par exemple), alors même que votre téléphone ne fait que `360px`. Pour un exemple concret, vous pouvez visiter [le site de majorette](https://www.majorette.com/fr/accueil/) avec votre téléphone ou avec le [mode mobile de Chrome](https://developers.google.com/web/tools/chrome-devtools/device-mode/#viewport).

Vous pouvez indiquer que votre site internet est responsive à l'aide d'une balise `<meta>` placé dans la partie `<head>` de votre document HTML :

```html
<meta name="viewport" content="width=device-width,initial-scale=1">
```

## Les requêtes média

Les requêtes média (_media queries_) permettent de modifier l'apparence d'un site en fonction du type d'appareil. La plupart du temps elles permettent d'appliquer certains styles en fonction de ses caractéristiques, notamment la largeur de la zone d'affichage (_viewport_).

Exemple de syntaxe :

```css
/* Des titres asssez grands par défaut (quelque soit l'appareil) */
h1 {  
	font-size: 36px;  
}

/* Des titres plus petits pour les appareils qui font maximum 560px de large */
@media (max-width: 560px) {  
	h1 {  
		font-size: 24px;  
	}
}
```

Voir la [documentation sur les media-queries](https://wiki.developer.mozilla.org/fr/docs/Web/CSS/Requ%C3%AAtes_m%C3%A9dia/Utiliser_les_Media_queries)

## Flexbox

On n'a pas toujours besoin de requêtes média pour faire un site responsive. Par exemple, les gabarits réalisés avec Flexbox peuvent s'adapter à l'espace disponible avec la propriété `flex-wrap`. Cette propriété indique si les éléments flexibles sont contraints à être disposés sur une seule ligne ou s'ils peuvent être affichés sur plusieurs lignes avec un retour automatique.

```css
/* Éléments flexibles sans césure */
.conteneur {
	display: flex;
	width: 350px;
}
.boite {
	flex: none;
	width: 100px;
}
```

![Exemple d'éléments flexibles sans césure](https://ibin.co/4zYviWZoDiYn.png)

```css
/* Éléments flexibles avec césure */
.conteneur {
	display: flex;
	flex-wrap: nowrap;
	width: 350px;
}
.boite {
	flex: none;
	width: 100px;
}
```

![Exemple d'éléments flexibles avec césure](https://ibin.co/4zYvrGaSgBvC.png)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTA1ODA0Nzg3Myw0MTMxMzc1MywtMjA0MD
U2MzU0LDEwNjA0MDA3NjcsMTExMTQ4Njg1NiwtMTIzNTE1OTUw
MywtMTAwNTMxNTcwOCwtMTU5MzE4ODAzMiwxODQ2MzQ5ODk4LC
0xNDE4MTk5MDcxLDE3NzI0OTUzOTYsMTE0MjU4OTkyMSwtMzM0
OTYyMTZdfQ==
-->