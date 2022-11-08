---
theme: blood 
transition: concave
slideNumber: true
---

# RevealJS

Être partisan du moindre effort.

![Mon github](assets/gh.jpg) {style="width: 20%; margin-left: 40%;"}

---

## Comment fonctionne les slides ?

Il suffit de trois tirets pour que cela crée une slide horizontale.

Deux pour une slide verticale

---

## Stylisation du texte

--

### Les titres de sections

Il suffit de mettre des "#" au début de la ligne pour indiquer un titre.
Plus vous mettez de "#", plus la section est petite.
> Exemple
>
> ```md
> # Grand titre
> ## Moyen titre
> ### Petit titre
> #### Encore plus petit titre, etc...
> ```

--

### Style du texte

Résultat :

*italic*

**bold**

***italic and bold***

Résultat :

> Bloc de texte

--

### Listes

1. Ordonnée
2. Comme
3. Ceci

Ou encore

- Non
- ordonnée

---

## Images & liens

[Google](www.google.fr)

![texte de remplacement](https://www.evilznet.com/vscode-reveal/assets/images/logo-v2.png) {style="width: 30%; margin-left: 35%;"}

---

## Code

```cpp
struct personne {
    char* nom, prenom;
}
```

---

## Équations

Les équations sont en LaTeX, très utile pour mettre en forme équations et
documents dédiés à la recherche.

$$f(x) = \frac{x}{2}$$

---

## Définitions

*[mollit]: Définition de mollit

Sit mollit occaecat nisi qui qui reprehenderit velit occaecat aute adipisicing et incididunt. Quis laborum ut incididunt cillum dolore eiusmod laboris duis amet laboris Lorem ex nostrud. Aute pariatur amet ea quis excepteur deserunt eiusmod reprehenderit sit elit est et. Ad laborum esse magna nulla. Id nulla duis deserunt fugiat duis mollit minim proident veniam ut anim. Et qui veniam eiusmod reprehenderit mollit laboris laboris aute non magna eu non reprehenderit est.

--

Term 1

:   Definition 1

Term 2 with *inline markup*

:   Definition 2

    ```c
    // Définition
    ```

    Third paragraph of definition 2.

---

## Support CSS

```md
paragraphe {style="color: red; /*css */"}
```

Nisi cillum adipisicing cupidatat et labore nostrud pariatur. Amet aliqua sint adipisicing dolor amet occaecat dolor nostrud proident nisi esse occaecat culpa ullamco. Nostrud pariatur labore elit proident et. Ipsum ipsum voluptate duis qui non nostrud deserunt. {style="color: red; text-align: left; /*css*/"}

---

## Support Awesome

```md
:fa-address-card:
:fa-align-left:
:fa-tiktok:
:fa-ambulance:
:fa-american-sign-language-interpreting:
:fa-anchor:
:fa-audio-description:
:fa-battery-full:
:fa-box-open:
:fa-broadcast-tower:
```

:fa-address-card:
:fa-align-left:
:fa-tiktok:
:fa-ambulance:
:fa-american-sign-language-interpreting:
:fa-anchor:
:fa-audio-description:
:fa-battery-full:
:fa-box-open:
:fa-broadcast-tower:

---

## Iframe

/i/https://www.youtube.com/embed/kurZDZ5jT2Y

---

## TODOS

- [ ] Mercury
- [x] Venus
- [x] Earth (Orbit/Moon)
- [x] Mars
- [ ] Jupiter
- [ ] Saturn
- [ ] Uranus
- [ ] Neptune
- [ ] Comet Haley

---

## Documentation

Libre à vous de piocher !

:   [Documentation de RevealJS](https://revealjs.com/)

:   [Documentation de l'extension vscode](https://www.evilznet.com/vscode-reveal/#/README?id=why-vscode-reveal-)
