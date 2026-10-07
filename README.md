# Léo Fuster — The Playlist (version à héberger)

Ce dossier est le site complet, prêt à être mis en ligne tel quel. Aucune étape de build.

## Mettre en ligne

- **Netlify Drop** (le plus simple) : glisse le dossier `leo-fuster-playlist` sur https://app.netlify.com/drop, connecte-toi pour garder le site, puis renomme-le (Site configuration → Change site name, ex. `leofuster.netlify.app`). Un nom de domaine perso se branche ensuite dans Domain management.
- **Vercel** : `npx vercel` depuis le dossier, ou import depuis GitHub.
- **GitHub Pages** : pousse le dossier dans un repo, puis Settings → Pages → branche `main`, dossier `/`.

Test en local : `npx serve .` puis http://localhost:3000. Le site doit être servi en http(s) (pas en double-clic sur le fichier) pour que la musique YouTube fonctionne.

## La musique

Comme sur la version Figma Make, chaque piste est lue par un lecteur YouTube invisible :

- « Start Journey » ou le bouton Play lance la musique (les navigateurs exigent un clic avant de jouer du son) ;
- la timeline avance au rythme du morceau, entre le point de la piste et le suivant, puis passe à la slide suivante à la fin de la chanson ;
- si une vidéo YouTube refuse la lecture intégrée, la timeline continue en silence à la durée du morceau ;
- le bouton ↗ du lecteur ouvre le morceau sur YouTube.

Les identifiants YouTube sont dans `index.html` (champ `youtubeId` de chaque piste) si tu veux changer une version.

## Vidéos

Les vignettes Vimeo ouvrent la vidéo directement dans la page.

## Polices

Brule, JV Signature, Acorn et FranceTV Brown sont intégrées dans `index.html`. Vérifie que leurs licences autorisent un usage web public (FranceTV Brown est la police maison de France Télévisions ; la Brule fournie semble être une version d'essai).
