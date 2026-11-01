# Alphade

Supprimez les filigranes semi-transparents, les logos et les textes incrustés de vos propres vidéos, directement sur votre Mac. Alphade fait réapparaître l’image d’origine au lieu de la flouter.

[English](README.md) | [Deutsch](README-de.md) | [Español](README-es.md) | Français | [日本語](README-ja.md) | [한국어](README-ko.md) | [繁體中文](README-zh_TW.md)

![Alphade compare la vidéo d’origine et la vidéo traitée](images/compare.png)

## Ce qu’il fait

Tracez un cadre autour de l’incrustation. Alphade étudie toute la vidéo, détermine comment l’incrustation a été mélangée à l’image et inverse l’opération sur chaque image. Si un logo est opaque et posé sur un fond simple, Alphade remplit plutôt la zone en douceur à partir de ce qui l’entoure.

- **Restaurer, pas flouter**&nbsp;: le filigrane semi-transparent est retiré de l’image, et ce qui se trouvait dessous réapparaît.
- **Le résultat annoncé avant l’export**&nbsp;: après l’analyse, Alphade indique si le filigrane donnera une «&nbsp;Suppression nette&nbsp;», une «&nbsp;Suppression par remplissage&nbsp;» ou un résultat «&nbsp;Flou après suppression&nbsp;».
- **Chaque image vérifiable**&nbsp;: parcourez le résultat image par image, comparez-le côte à côte avec l’original et lancez la lecture depuis n’importe quel moment.
- **Seul le cadre change**&nbsp;: exportez en taille d’origine ou réduite en 1080p ou 720p, en H.264 ou HEVC. Le son est copié tel quel.
- **Confidentiel**&nbsp;: tout se passe sur votre Mac. Les vidéos ne sont jamais envoyées en ligne, aucun compte n’est nécessaire, Alphade n’établit aucune connexion réseau et ne collecte aucune donnée.
- **Gratuit**.

## Installation

Nécessite macOS 26 ou version ultérieure. Testé sur Mac avec puce Apple. Alphade est signé avec un Developer ID et notarié par Apple.

### Téléchargement

1. Téléchargez [`Alphade.zip`](../../releases/latest/download/Alphade.zip) depuis la [dernière version](../../releases/latest).
2. Ouvrez le zip et faites glisser **Alphade** dans le dossier Applications.
3. Ouvrez Alphade. macOS vous demande si vous voulez ouvrir une app téléchargée sur Internet&nbsp;; cliquez sur **Ouvrir**.

Pour le désinstaller, faites glisser Alphade dans la Corbeille. Ses réglages et fichiers temporaires se trouvent dans `~/Library/Containers/app.vulcanshen.alphade`, que vous pouvez aussi supprimer.

### Homebrew

```sh
brew install --cask vulcanshen/tap/alphade
```

Mise à jour avec `brew upgrade --cask alphade`. Désinstallation avec `brew uninstall --cask alphade`&nbsp;; ajoutez `--zap` pour supprimer aussi ses réglages et fichiers temporaires.

## Prise en main

1. Cliquez sur **Choisir une vidéo…** (ou déposez une vidéo dans la fenêtre).
2. Tracez un cadre autour du filigrane, en laissant un peu de marge de chaque côté.
3. Cliquez sur **Analyser**.
4. Vérifiez le résultat avec **Original**, **Traité** et **Comparer**.
5. Cliquez sur **Exporter…** et choisissez où enregistrer. Le nom proposé est `<nom d’origine>_nowm.mp4`.

L’interface suit la langue du système&nbsp;: English, Deutsch, Español, Français, 日本語, 한국어 ou 繁體中文. Vous pouvez la changer dans les Réglages.

## Clavier

| Touches | Action |
|---|---|
| ⌘O | Ouvrir une vidéo |
| ⌘E | Exporter |
| ⌘1 / ⌘2 / ⌘3 | Original / Traité / Comparer |
| ← / → | Image précédente / suivante |
| Espace | Lecture ou pause (son coupé) |
| Maintenir O | Affiche l’original tant que la touche est enfoncée |
| ⌘+ / ⌘− | Zoom avant / arrière (après avoir tracé le cadre) |
| ⌘, | Réglages (langue) |

## Fonctionne le mieux avec

- Les filigranes, logos et textes semi-transparents qui restent au même endroit pendant toute la vidéo
- Les logos opaques sur des fonds simples comme des couleurs unies, des dégradés ou des diapositives
- Les vidéos MP4, MOV et M4V en 8 bits (SDR)

## Non pris en charge

- Les filigranes qui bougent ou changent de position
- Les filigranes opaques sur des fonds détaillés ou des prises de vue réelles (la zone devient floue)
- Les vidéos 10 bits et HDR

## Utilisez-le sur vos propres vidéos

Ne modifiez que des vidéos qui vous appartiennent ou que vous avez le droit de modifier. Retirer le filigrane de quelqu’un d’autre peut enfreindre le droit d’auteur de votre pays, et vous êtes responsable de l’usage que vous faites d’Alphade.

## Retours

Signalez les problèmes et les idées dans les [Issues](../../issues). Le code source n’est pas public.

## Contributeurs

<a href="https://github.com/vulcanshen"><img src="https://github.com/vulcanshen.png" width="48" alt="Vulcan Shen"></a>
<a href="https://github.com/claude"><img src="https://github.com/claude.png" width="48" alt="Claude"></a>

Développé par [Vulcan Shen](https://github.com/vulcanshen) et [Claude](https://github.com/claude) avec Claude Code.

## Licence

Alphade est gratuit à télécharger et à utiliser. © 2026 Vulcan Shen. Tous droits réservés. Alphade est fourni «&nbsp;tel quel&nbsp;», sans garantie d’aucune sorte.
