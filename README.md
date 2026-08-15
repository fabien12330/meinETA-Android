# meinETA Android

Application Android dédiée ouvrant directement :

https://www.meineta.at/registered/boilers/boiler.xhtml?id=63365

## Fonctionnement

- ouverture dans une WebView indépendante de Chrome ;
- JavaScript et stockage DOM activés ;
- cookies persistants pour conserver la session lorsque le serveur meinETA le permet ;
- aucun identifiant ni mot de passe intégré dans l'APK ;
- bouton Retour Android = page précédente ;
- connexions HTTP non chiffrées interdites.

## Compilation sans ordinateur avec GitHub Actions

### 1. Créer un dépôt GitHub

Depuis le navigateur du téléphone :

1. Aller sur GitHub.
2. Créer un nouveau dépôt, par exemple `meinETA-Android`.
3. Le mettre en `Private` si souhaité.

### 2. Envoyer tous les fichiers

Décompresser ce ZIP sur le téléphone puis envoyer tout son contenu à la racine du dépôt.

Important : le dossier `.github/workflows/` doit être conservé.

### 3. Lancer la compilation

Dès que les fichiers sont présents sur la branche `main`, GitHub Actions démarre automatiquement.

Sinon :

1. ouvrir l'onglet `Actions` ;
2. ouvrir `Build meinETA APK` ;
3. utiliser `Run workflow`.

### 4. Télécharger l'APK

Une fois le job terminé avec une coche verte :

1. ouvrir le job terminé ;
2. descendre jusqu'à `Artifacts` ;
3. télécharger `meinETA-APK` ;
4. décompresser le ZIP obtenu ;
5. installer `meinETA.apk`.

Android peut demander d'autoriser l'installation d'applications inconnues pour le navigateur ou le gestionnaire de fichiers utilisé.

## Première connexion

Lors du premier lancement :

1. se connecter à meinETA ;
2. utiliser l'option de mémorisation proposée par le site si disponible ;
3. fermer puis rouvrir l'application pour vérifier la persistance de session.

Les cookies WebView sont conservés entre les lancements de l'application.
