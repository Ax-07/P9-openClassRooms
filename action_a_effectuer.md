## rapport
- [x] Score Lighthouse avant optimisation : Faire une capture d'écran des scores Lighthouse avant optimisation
- [ ] Score Lighthouse après optimisation : Faire une capture d'écran des scores Lighthouse après optimisation
## action effectuer
## Performances:
- [x] Modifier la taille et le format des images. (https://www.img2go.com/)
- [x] Utilisation de des attribut 'srcset' et 'sizes' pour gérer la taille des images à afficher.
    - Dans le fichier maugallery.js, j'ai modifier les fonction openLigthBox(), prevImage() et nextImage() de la manière suivante : 
        - l.116  openLightBox(element, lightboxId) {
                  const lightboxImage = $(`#${lightboxId}`).find(".lightboxImage");
                  lightboxImage.attr("src", element.attr("src")); console.log(lightboxImage.attr("src"));
                  lightboxImage.attr("srcset", element.attr("srcset")); // ligne ajouter
                  lightboxImage.attr("sizes", element.attr("sizes")); // ligne ajouter
                  $(`#${lightboxId}`).modal("toggle");
                          },  
        - l.123  prevImage() et nextImage()
                // => 
                next = imagesCollection[index] || imagesCollection[0];
                  $(".lightboxImage").attr("src", $(next).attr("src"));
                  $(".lightboxImage").attr("srcset", $(next).attr("srcset")); // ligne ajouter
- [x] Renommer les images avec des mots clés pertinents.
- [x] Minifier le code. [js](https://jscompress.com/), [css](https://purifycss.online/)
    - maugallery.js: Stats: 41.76% compression, saving 3.5 kb (+4 accessibilité )
    - script.js: Stats: 46.67% compression, saving 0.14 kb ( aucune amélioration )
    - style.css: Stats: 25.1% compression, saving  1.36 kb ( +1 performance )
    - bootstrap.css: before: 200.67 KB after: 33.18 KB 

- [x] Différer le chargement des scripts non essentiels. (Déplacez vos scripts non essentiels en bas de la page, juste avant la fermeture de la balise </body>.) (fait gagner 1 pts de performance)
- [x] Utiliser le fichier minifier de boostrap.bunddle.js. (fait gagner 1 pts de performance)

## Accessibilité

- [x] Ajouter les attributs alt aux images.
- [x] Ajouter un titre au document (balise `<head></head>`).
- [x] Ajouter des labels aux inputs du formulaire.
- [x] Modifier le contraste de couleur ".nav-pills .nav-link.active, .nav-pills .show > .nav-link"
  - solution 1 : text #ffffff background #7d733c (score contrast adobe = 4.78)
    on garde le texte en blanc et on assombrie le background
  - solution 2 ( retenue ): text #000000 background #BEB45A (score contrast = 9.87)
    on garde la couleur du background et on met le text en noir
- [x] Ajouter `lang` dans la balise html.
- [x] Modifier le classement séquentiel des titre (h1, etc..)
    - l.72 h3 => h1
    - l.148 h3 => h2
    - l.149 h6 => p  
        - modif css  => ".about-me__introduction", ajout !important à	"width: 60%" et ajout de font-size: 1rem !important( !important permet de prendre le dessus sur "#about-me p");
    - l.216 et 261 h1 => h3
        - modif css => ".quote__text", ajout font-size: calc(1.375rem + 1.5vw);


## Bonnes pratiques

- [x] Remplacer certaines div par des sections.
- [x] Ajouter une balise <main>.

## SEO

- [x] Ajouter un titre au document (balise `<head></head>`).
- [x] Ajouter une description au document.
- [x] Ajouter les attributs alt aux images.
- [x] Les liens n'ont pas de nom discernable. (logo instagram)
- [x] Ajouter `lang` dans la balise html.

## Étape 5 : Ajoutez le référencement local et réseaux

sociaux
70 % de progression
Avant de démarrer cette étape, je dois avoir :
● Le rapport Lighthouse au vert sur la partie SEO (note supérieure ou
égale à 90 %).
Une fois cette étape terminée, je devrais avoir :
● Le rapport de Rich Snippet Google avec les informations du client.
● Les balises meta liées aux principaux réseaux sociaux, comme les
metas OpenGraph pour Facebook, et les Twitter Cards.
Recommandations :
● Utilisez les microdonnées Schema.org pour le référencement local.
Utilisez la documentation (lien plus bas) pour trouver les
définitions qui conviennent le mieux pour le client.
Ressources :
● Améliorer le référencement local : 10 conseils : cet article vous
donnera des astuces pour améliorer votre référencement local.
● Schema.org : cet outil vous permettra d’optimiser le référencement
local du site web.
● Google Rich Snippet : cet outil vous permettra de tester votre
référencement local.
● Open Graph et Twitter Cards : cet article vous aidera à mettre en
place le référencement sur les réseaux sociaux.
● Balises Meta pour le SEO : cet article vous guidera sur le choix et
l’utilisation des bonnes balises meta pour le référencement global
du site.
