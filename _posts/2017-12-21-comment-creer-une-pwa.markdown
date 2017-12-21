---
layout: post
url: "/common/2017/12/21/comment-creer-unr-pwa.html"
title:  "Comment créer une Progressive Web App (PWA)"
author: "Moetaz Torkhani"
date:   2016-04-12 14:33:00 +0100
pitch:  "L'objectif de cet article est de voir comment créer une progressive web app (PWA)"
comments: True
categories: common
---

**Les étapes principales de la conception d'une Progressive Web App**

- Définir et concevoir une interface système (app shell)
- Optimiser le chargement du contenu en gérant le cache par l'intermédiaire de service workers
- Définir un manifeste d'application pour perfectionner l'expérience applicative
- Proposer une navigation sécurisée à l'utilisateur

**ÉTAPE 1, App shell**

L'app shell contient les composants HTML, CSS et basiques de votre application permettant d'afficher l'interface utillisateur basique de la Progressive Web App.
Il sépare complètement l'UI et les données de l'application pour se concentrer sur la vitesse du chargement initial.
Lorsque l'app shell est défini et chargé en tant que première couche de l'application, les service workers font leur entrée.

**ÉTAPE 2, LE SERVICE WORKER**
Le service worker est un fichier javascript à enregistrer dans le navigateur.

Nous allons tout d’abord créer un fichier vide service-worker.js dans le dossier public.

```touch public/service-worker.js```

Puis, pour enregistrer le service worker, il vous suffit d’ajouter le code suivant dans le fichier public/index.html

```<script>;
   if('serviceWorker' in navigator) {
     navigator.serviceWorker
              .register('/sw.js')
              .then(function() { console.log("Service Worker Registered"); });
   }
   </script>;```

**ÉTAPE 3, LE Manifest**


Bon développement à tous !

<blockquote>Moetaz Torkhani</blockquote>
