<div align="center">

# 🍃 Konoha

**Votre bibliothèque de mangas, sur votre téléphone. Rien d'autre.**

Lecteur de mangas personnel, sans compte, sans pub, sans serveur : tout vit dans une seule page web installable (PWA).

[![Version](https://img.shields.io/badge/version-2.5-7c6cff?style=flat-square)](https://census-specs.github.io/konoha/)
[![PWA](https://img.shields.io/badge/PWA-installable-8b5cf6?style=flat-square&logo=googlechrome&logoColor=white)](https://census-specs.github.io/konoha/)
[![100% local](https://img.shields.io/badge/donn%C3%A9es-100%25%20locales-4ad991?style=flat-square)](https://census-specs.github.io/konoha/)
[![Monofichier](https://img.shields.io/badge/monofichier-HTML%2FJS-E34F26?style=flat-square&logo=html5&logoColor=white)](https://census-specs.github.io/konoha/)
[![Hors-ligne](https://img.shields.io/badge/mode-hors%20ligne-22c55e?style=flat-square)](https://census-specs.github.io/konoha/)

### 🚀 [Essayer Konoha maintenant](https://census-specs.github.io/konoha/)

</div>

---

## ✨ Fonctionnalités

### 📚 Bibliothèque locale
- 📂 Import **CBZ, CBR, PDF, EPUB** (glisser-déposer ou import par URL)
- 💾 Stockage **IndexedDB** : vos mangas restent sur votre appareil, lisibles hors-ligne
- 🗂️ Détection automatique des **séries** (Tome 12, v03, chapitre 110, one_piece_v03…)
- 🏷️ Badges tomes / chapitres, favoris ⭐, progression de lecture, couvertures personnalisées
- 🧠 **Classement automatique** en un tap : nettoie et regroupe toute la bibliothèque
- 📊 Statistiques de lecture, thèmes sombre ☀️/🌙, export / import de la progression

### 📖 Lecteur confortable
- 📖 Sens de lecture **RTL japonais**, LTR, et mode **vertical** (webtoon)
- 🔍 Zoom pinch / double-tap, navigation par zones tactiles, slider de pages
- 📱 Plein écran, barres d'outils auto-masquées, tutoriel interactif intégré
- 🛌 Mode veille désactivé pendant la lecture

### 🌐 Sources en ligne (via proxy personnel)
- 🌍 **MangaDex** : catalogue FR, recherche, lecture en ligne, téléchargement hors-ligne, enrichissement des séries (couverture, synopsis, auteur, genres)
- 📺 **Anime-Sama** : scans VF/VA en lecture intégrée, téléchargement hors-ligne en CBZ, rangement automatique par manga
- 🎬 **Animés en streaming** (v2.3) : saisons, épisodes VOSTFR/VF, lecteurs multiples, épisodes vus cochés automatiquement, reprise de lecture
- 🔎 Onglet En ligne repensé (v2.5) : chaque source bien séparée (MangaDex / Anime-Sama / Autres)
- 🩺 **Test de connexion intégré** (v2.5) : diagnostique le proxy, les sources et la lecture image par image

---

## 🚀 Installation (2 minutes)

1. Ouvrez **[Konoha](https://census-specs.github.io/konoha/)** dans Chrome sur Android (ou tout navigateur récent).
2. Menu du navigateur → **« Ajouter à l'écran d'accueil »** ou **« Installer l'application »**.
3. C'est tout : Konoha s'ouvre désormais comme une vraie app, plein écran, avec sa propre icône 火.

> 💡 Vous pouvez l'utiliser immédiatement pour lire vos fichiers CBZ/CBR/PDF/EPUB. Les sources en ligne demandent un petit réglage en plus (voir ci-dessous).

---

## 🛰️ Activer les sources en ligne (optionnel)

La lecture en ligne (MangaDex, Anime-Sama) passe par un **proxy Cloudflare Worker personnel** que vous déployez gratuitement en 5 minutes. Il contourne les blocages CORS et protège votre vie privée : tout le trafic passe par votre propre Worker, il n'y a aucun serveur tiers.

Trois routes suffisent :

| Route | Rôle |
| --- | --- |
| `/md/*` | API MangaDex |
| `/as/*` | Pages Anime-Sama (catalogue, chapitres, épisodes) |
| `/img?u=…` | Relais d'images MangaDex / Anime-Sama |

Une fois le Worker déployé, copiez son URL dans Konoha : **menu ⋮ → « Proxy en ligne… »**. En cas de souci, **⋮ → « Test de connexion »** diagnostique chaque étape.

---

## 🔄 Mettre à jour Konoha

1. Remplacez `index.html` et `sw.js` sur la branche `main` (GitHub → *Add file* → *Upload files*).
2. Sur le téléphone : fermez puis rouvrez Konoha (la mise à jour s'active au 2ᵉ lancement grâce au Service Worker).
3. Vérifiez la version dans **menu ⋮ → « À propos »**.

---

## 🧰 Technique

- **Un seul fichier** `index.html` : aucun build, aucune dépendance, aucun framework. Il suffit d'ouvrir le fichier.
- **IndexedDB** pour les mangas et couvertures, **localStorage** pour les réglages.
- **Service Worker** pour l'installation PWA et le mode hors-ligne complet.
- Fonctionne partout : Android, iOS, ordinateur (dépôt GitHub Pages, serveur local, ou simple fichier).

---

## 🔒 Confidentialité

- Vos fichiers restent **dans votre navigateur**. Aucune donnée n'est envoyée, aucun compte requis.
- Les sources en ligne passent uniquement par **votre propre** Worker Cloudflare.
- Aucune publicité, aucun traceur, aucune statistique externe.

---

## ⚖️ Mentions légales

Konoha est un lecteur personnel fourni tel quel. Les contenus en ligne proviennent de **MangaDex** et d'**Anime-Sama** : créditez les équipes de scantrad et les auteurs originaux. Usage strictement personnel et privé.

---

## 📜 Historique des versions

| Version | Nouveautés |
| --- | --- |
| **2.5** | 🎨 Onglet En ligne repensé (sources séparées), 🩺 test de connexion intégré, lecture MangaDex/Anime-Sama fiabilisée |
| **2.4** | 🔧 Correction des chapitres « introuvables » sur Anime-Sama, rangement par nom de manga, migration automatique |
| **2.3** | 📺 Streaming des animés Anime-Sama (saisons, épisodes, lecteurs vidéo intégrés) |
| **2.2** | 🧠 Classement intelligent en séries, enrichissement MangaDex, tutoriel de lecture animé |
| ≤ 2.1 | 📚 Base : CBZ/CBR/PDF/EPUB, séries, MangaDex, scans Anime-Sama, PWA |

---

<div align="center">

### 火 Konoha

*Fait avec ❤️ pour les amoureux de mangas.*

[Signaler un souci](https://github.com/census-specs/konoha/issues) · [Voir le code](https://github.com/census-specs/konoha)

</div>