## rapport

- [x] Score Lighthouse avant optimisation : Faire une capture d'écran des scores Lighthouse avant optimisation
- [ ] Score Lighthouse après optimisation : Faire une capture d'écran des scores Lighthouse après optimisation

## action effectuer

## Performances:

- [x] Modifier la taille et le format des images. (https://www.img2go.com/)
<<<<<<< HEAD
- [x] Utilisation de des attribut 'srcset' et 'sizes' pour gérer la taille des images à afficher. - Dans le fichier maugallery.js, j'ai modifier les fonction openLigthBox(), prevImage() et nextImage() de la manière suivante : 
  - l.116  
       <code>
      openLightBox(element, lightboxId) {
          const lightboxImage = $(`#${lightboxId}`).find(".lightboxImage");
          lightboxImage.attr("src", element.attr("src")); console.log(lightboxImage.attr("src"));
          lightboxImage.attr("srcset", element.attr("srcset")); // ligne ajouter
          lightboxImage.attr("sizes", element.attr("sizes")); // ligne ajouter
                  $(`#${lightboxId}`).modal("toggle");
      },  
      </code>
  - l.123 
      <code>prevImage() et nextImage()
      // =>
      next = imagesCollection[index] || imagesCollection[0];
      $(".lightboxImage").attr("src", $(next).attr("src"));
      $(".lightboxImage").attr("srcset", $(next).attr("srcset")); // ligne ajouter
      </code>
=======
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
>>>>>>> 7b4e45ee3e4c9dd8cdde2dec19a9611b26c188dd
- [x] Renommer les images avec des mots clés pertinents.
- [x] Minifier le code. [js](https://jscompress.com/), [css](https://purifycss.online/)

  - maugallery.js: Stats: 41.76% compression, saving 3.5 kb (+4 accessibilité )
  - script.js: Stats: 46.67% compression, saving 0.14 kb ( aucune amélioration )
  - style.css: Stats: 25.1% compression, saving 1.36 kb ( +1 performance )
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
    - modif css => ".about-me\_\_introduction", ajout !important à "width: 60%" et ajout de font-size: 1rem !important( !important permet de prendre le dessus sur "#about-me p");
  - l.216 et 261 h1 => h3
    - modif css => ".quote\_\_text", ajout font-size: calc(1.375rem + 1.5vw);

## Bonnes pratiques

- [x] Remplacer certaines div par des sections.
- [x] Ajouter une balise <main>.

## SEO

- [x] Ajouter un titre au document (balise `<head></head>`).
- [x] Ajouter une description au document.
- [x] Ajouter les attributs alt aux images.
- [x] Les liens n'ont pas de nom discernable. (logo instagram)
- [x] Ajouter `lang` dans la balise html.
