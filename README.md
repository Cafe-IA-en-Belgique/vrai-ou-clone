# Vrai ou Cloné ?

Quiz de Café IA Bruxelles sur le clonage de voix par intelligence artificielle.

Site : https://vrai-ou-clone.cafe-ia.be

## Publication

GitHub Pages publie automatiquement `index.html` depuis la racine de la branche `main`.
Le fichier `CNAME` conserve le domaine personnalisé.

`index.html` est une copie du fichier HTML fourni. Les cinq extraits audio et le logo
sont intégrés dans le HTML. Aucune compilation ni installation n’est nécessaire.
Les fichiers originaux restent disponibles dans le dossier local.

Pour mettre le quiz à jour, modifier `index.html`, puis envoyer les changements
sur la branche `main`.

## Inscription aux nouvelles du Café IA

Le formulaire sous le quiz envoie directement les inscriptions au formulaire
public Brevo « Membres du Café IA — Vrai ou Cloné », relié à la liste
« Membres du Café IA » (ID `3`). Il utilise l’intégration HTML simple de Brevo :
email obligatoire, consentement obligatoire non précoché et champ piège antispam.
La confirmation est affichée dans la page après une réponse de réussite de Brevo,
sans perdre la progression du quiz. Les échecs restent visibles et permettent de
réessayer. Sans JavaScript, l’envoi HTML ouvre la réponse Brevo dans un nouvel onglet.
Aucun email de confirmation n’est envoyé.

La liste et les réglages se gèrent dans Brevo → Marketing → Formulaires.
En cas de remplacement du formulaire, reporter son adresse publique `action`
dans `index.html` et vérifier que la liste sélectionnée est toujours la bonne.
L’affichage du résultat dans le quiz est géré localement, à partir de la réponse Brevo.

Les clés `BREVO_API_KEY` et `BREVO_MCP_API_KEY` ne sont nécessaires que pour
l’administration de Brevo. Elles restent dans le `.env` local du dossier parent,
ne doivent jamais être intégrées au HTML ni committées, et ne sont pas utilisées
par les visiteurs. GitHub Pages n’exécute aucun code serveur.
