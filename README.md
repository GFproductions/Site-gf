🎭 GF Productions - Site Officiel

Ce dépôt contient le code source du site vitrine de Gabriel Francès (GF Productions), propulsé par Firebase et Google Apps Script.

🔴 CHECKLIST DÉPLOIEMENT

À vérifier avant chaque mise en ligne officielle

[x] Relais Mail : Script Google Apps Script déployé et URL à jour.

[ ] Réseaux Sociaux : Liens Instagram/Facebook saisis dans Firestore (site_content/contact).

[ ] Catalogue : Images de test remplacées par les URLs HD du Firebase Storage.

[ ] Dossiers de Presse : Vérifier que les PDF sont accessibles dans la section "Press Kits".

[ ] Favicon : S'assurer que le logo s'affiche bien dans l'onglet navigateur.

⌨️ COMMANDES CLOUD SHELL

Copiez et collez ces commandes dans votre console Google Cloud Shell

1. Préparation de l'environnement

Configure le projet Google Cloud et entre dans le dossier racine :

gcloud config set project gf-productions-aa94c


cd ~/Site-gf


2. Synchronisation GitHub

Récupère les dernières modifications (comme ce README) faites sur le Web :

git pull origin main


3. Firebase : Test & Déploiement

Vérifie le projet actif, teste en privé, puis publie officiellement :

firebase use gf-productions-aa94c


Aperçu temporaire (Lien de test) :

firebase hosting:preview


Mise en ligne définitive :

firebase deploy --only hosting


🛠 ARCHITECTURE & LIENS UTILES

Gestion des e-mails (Relais Mail)

Le formulaire "Booking Pro" utilise un script Google Apps Script pour transformer les envois en e-mails Gmail.

URL du Relai : https://script.google.com/macros/s/AKfycbyIFj8U82r3ejZjYIBfF7Cxh83vMzzMIHIS4EPGnUPtncATiNvTiMOy9q-lg5K6tKfZ/exec

Destinataire : contact@gfproductions.fr

Données (Firestore)

Collection spectacles : Contient un document par pièce (titre, poster_url, description, etc.).

Collection site_content : Contient les textes fixes du site (Bio, Contact, Liens sociaux).

Liens Rapides

Console Cloud Shell : Ouvrir le terminal

Console Firebase : Accéder au projet

Éditeur Google Apps Script : Gérer le script mail

© 2025 GF Productions.
