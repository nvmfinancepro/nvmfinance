# NVM Finance — Site statique

Site statique 3 pages, fidèle au contenu de nvmfinance.wordpress.com,
optimisé mobile-first avec points de confiance ajoutés.

## Structure des fichiers

```
nvm-finance/
├── index.html       ← Page d'accueil
├── services.html    ← Page Services
├── contact.html     ← Page Contact
├── style.css        ← CSS partagé (nav, footer, composants)
├── main.js          ← JS partagé (hamburger, scroll reveal)
├── assets/
│   ├── logo.png         ← Ton logo (à télécharger depuis WordPress)
│   ├── dashboard.png    ← Screenshot dashboard (page accueil)
│   └── services.png     ← Screenshot services (page services)
└── README.md
```

## Étape 1 — Récupérer les images

Télécharge ces 3 images et place-les dans le dossier `assets/` :

1. **logo.png**
   https://nvmfinance.wordpress.com/wp-content/uploads/2026/02/capture-decran-2026-02-12-a-20.39.57.png

2. **dashboard.png**
   https://nvmfinance.wordpress.com/wp-content/uploads/2026/03/capture-decran-2026-02-15-a-16.36.08-2.png

3. **services.png**
   https://nvmfinance.wordpress.com/wp-content/uploads/2026/03/capture-decran-2026-03-05-a-16.37.39.png

## Étape 2 — Tester en local

Ouvre simplement `index.html` dans ton navigateur.
Ou utilise une extension VS Code comme "Live Server" pour un vrai serveur local.

## Étape 3 — Mettre en ligne

**Option A — Hébergement gratuit (recommandé pour démarrer)**
- Netlify : glisse-dépose le dossier sur https://app.netlify.com/drop
- Vercel : `npx vercel` dans le dossier

**Option B — Hébergement classique**
- FTP chez OVH, Infomaniak, o2switch, etc.
- Upload tous les fichiers à la racine de ton domaine

## Formulaire de contact (optionnel)

Le formulaire dans contact.html simule l'envoi côté frontend.
Pour recevoir vraiment les messages, remplace l'action dans contact.html par Formspree :

1. Crée un compte sur https://formspree.io (gratuit jusqu'à 50 msg/mois)
2. Remplace dans contact.html :
   ```html
   <form class="contact-form" id="contactForm" novalidate>
   ```
   par :
   ```html
   <form class="contact-form" action="https://formspree.io/f/TON_ID" method="POST">
   ```
3. Retire le `<script>` de gestion du formulaire en bas de contact.html

## Pages

| Page | Fichier | Contenu |
|------|---------|---------|
| Accueil | index.html | Hero + trust strip + dashboard + bénéfices + témoignages + CTA |
| Services | services.html | Présentation + image + 3 blocs de services détaillés + CTA |
| Contact | contact.html | Lien RDV Brevo + formulaire de contact + coordonnées |
