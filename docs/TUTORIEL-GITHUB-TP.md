# Tutoriel GitHub pour les TPs — la soumission pas à pas

Ce tutoriel s'adresse à ceux du groupe qui n'ont **jamais utilisé GitHub**. Il couvre tout ce qu'il faut pour rendre un TP d'exercices résolus : créer un compte, récupérer le notebook, le travailler, et ouvrir la Pull Request. Suivez les étapes dans l'ordre ; chacune prend quelques minutes. Aucune installation de logiciel spécifique n'est nécessaire en dehors de ce que vous utilisez déjà pour les notebooks (Jupyter ou Google Colab).

Si une étape bloque, ne restez pas seuls : ouvrez une [demande d'accompagnement](https://github.com/jsboigeEPF/2026-MSAPP3IN08-GenAI/issues/new?template=demande-accompagnement.yml), c'est prévu pour.

## Trois notions, deux minutes

- Un **dépôt** est un dossier de fichiers partagé, avec l'historique de toutes ses modifications.
- Un **fork** est votre copie personnelle d'un dépôt : vous y travaillez sans risque pour l'original.
- Une **Pull Request** (PR) est votre demande officielle : « voici mes modifications, merci de les intégrer au dépôt d'origine ». C'est elle qui est évaluée, et c'est sur elle que l'enseignant vous répond.

Le TP se déroule donc en un aller-retour : vous **téléchargez** le notebook depuis votre copie, vous le **travaillez** dans Jupyter ou Colab, vous le **renvoyez** sur votre copie, puis vous ouvrez la **PR** vers le dépôt d'origine `jsboige/CoursIA`.

## Étape 0 — Créer un compte GitHub (une fois, 2 minutes)

1. Allez sur [github.com/signup](https://github.com/signup).
2. Choisissez un identifiant professionnel (il sera visible sur votre contribution).
3. Validez l'e-mail de confirmation.

Un seul compte par personne suffit. Le groupe désigne **un membre** dont le compte hébergera la copie de travail (étape 1) — mais tout le monde peut y être invité (étape 2).

## Étape 1 — Forker le dépôt CoursIA (une fois par groupe)

1. Connectez-vous, puis ouvrez [`github.com/jsboige/CoursIA`](https://github.com/jsboige/CoursIA).
2. Cliquez sur le bouton **Fork** en haut à droite de la page.
3. Laissez les options par défaut et cliquez sur **Create fork**.

GitHub crée `votre-compte/CoursIA` : c'est la copie de travail du groupe pour les deux TPs. Le dépôt est volumineux, la création peut prendre une dizaine de secondes.

## Étape 2 — Inviter vos coéquipiers sur le fork

Pour que les trois membres du groupe puissent déposer des fichiers sur la copie :

1. Sur la page de `votre-compte/CoursIA`, allez dans l'onglet **Settings** du dépôt.
2. Dans le menu de gauche, **Collaborators** (GitHub peut demander de confirmer un code : suivez l'invite).
3. **Add people** : saisir l'identifiant GitHub de chaque coéquipier, puis **Add to this repository**.
4. Chaque invité accepte l'invitation reçue par e-mail ou dans ses notifications.

## Étape 3 — Créer une branche de travail (une fois par TP)

Une **branche** est une version parallèle où vos modifications restent isolées, sans toucher au travail déjà rendu.

1. Sur `votre-compte/CoursIA`, cliquez sur le sélecteur de branche (il affiche **main**) en haut à gauche de la liste de fichiers.
2. Tapez le nom de la nouvelle branche, par exemple `tp1-groupe-nomcourt`.
3. Cliquez sur **Create branch tp1-groupe-nomcourt from main**.

Le sélecteur affiche désormais votre branche. **Vérifiez-le avant chaque dépôt de fichier** : c'est l'erreur la plus fréquente.

## Étape 4 — Télécharger le notebook du TP

1. Ouvrez le notebook indiqué en classe dans la liste du TP. Il se trouve dans votre fork au même chemin que dans le dépôt d'origine, par exemple `MyIA.AI.Notebooks/GenAI/...` (naviguez dans les dossiers jusqu'au fichier `.ipynb`).
2. GitHub affiche un aperçu du notebook. Cliquez sur le bouton **Raw** (à droite, au-dessus du contenu).
3. Le fichier brut s'affiche : enregistrez-le avec **Ctrl+S** (ou clic droit, *Enregistrer sous*), en gardant **exactement le même nom de fichier**.

## Étape 5 — Travailler le notebook dans Jupyter ou Colab

Ouvrez le fichier `.ipynb` téléchargé dans votre outil habituel :

- **Jupyter** (Anaconda, VS Code...) : ouvrez le fichier, ou modifiez-le dans votre clone local si vous en avez un ;
- **Google Colab** : *Fichier > Importer un notebook*, puis travaillez directement.

Puis :

1. Corrigez les exercices ouverts annoncés pour le TP (cellules à compléter). Les attentes détaillées (qu'est-ce qu'une correction acceptée, combien d'exercices pour quel bonus) sont dans [TPs dans CoursIA et bonus](TPS-ET-BONUS.md).
2. **Exécutez tout le notebook depuis le début** (dans Colab : *Exécution > Tout exécuter*). Les sorties des cellules font partie du rendu : elles prouvent que votre correction tourne. Aucune cellule ne doit rester en erreur.
3. Enregistrez : *Fichier > Télécharger > Télécharger le .ipynb* (Colab), ou simple sauvegarde (Jupyter). Le fichier garde le même nom.

**Ne modifiez jamais le contenu du fichier `.ipynb` à la main dans GitHub** (l'éditeur web de GitHub y montrerait du JSON illisible) : passez toujours par Jupyter ou Colab, puis déposez le fichier obtenu à l'étape suivante.

## Étape 6 — Déposer le notebook sur votre branche

1. Revenez sur `votre-compte/CoursIA` dans le navigateur, **sur votre branche de TP** (étape 3).
2. Naviguez jusqu'au **dossier exact** contenant le notebook d'origine (même chemin qu'à l'étape 4).
3. Cliquez sur **Add file > Upload files**.
4. Glissez le fichier `.ipynb` travaillé (même nom : GitHub propose de l'écraser, c'est bien ce qu'on veut).
5. En bas de page, sous *Commit changes*, remplacez le message par quelque chose d'explicite, par exemple : `TP1 : correction des exercices 2 et 3 de <nom du notebook>`.
6. Vérifiez que **Commit directly to the `tp1-groupe-nomcourt` branch** est sélectionné, puis cliquez sur **Commit changes**.

Pour une modification après review, refaites simplement cette étape : la Pull Request se met à jour toute seule.

## Étape 7 — Ouvrir la Pull Request vers CoursIA

1. Dans `votre-compte/CoursIA`, un bandeau jaune **Compare & pull request** apparaît après votre premier dépôt. Cliquez dessus. (Sinon : onglet **Pull requests > New pull request > compare across forks**.)
2. Vérifiez la direction en haut du formulaire — c'est la ligne qui décide de tout :
   - **base repository** : `jsboige/CoursIA`, base `main` (le dépôt d'origine) ;
   - **head repository** : `votre-compte/CoursIA`, compare `tp1-groupe-nomcourt` (votre branche).
3. Le bouton **Create pull request** doit être vert (il indique *Able to merge*). S'il parle de conflit, ne forcez rien : ouvrez une demande d'accompagnement.
4. Remplissez le titre et la description, en précisant :
   - le numéro du TP et le groupe ;
   - le notebook corrigé (son chemin) ;
   - les exercices corrigés, un par un ;
   - comment vous avez vérifié (exécution complète, cas limites testés).
5. **Create pull request.** Notez le lien de la PR et transmettez-le selon la consigne donnée en classe : sans PR ouverte, le travail ne peut pas être compté.

## Étape 8 — Suivre la review

L'enseignant relit la PR ; il peut demander des ajustements — c'est normal, cela fait partie du processus, et l'évaluation des TPs est bienveillante.

- Les remarques apparaissent dans l'onglet **Conversation** (commentaires généraux) et **Files changed** (commentaires ligne à ligne).
- Pour répondre : cliquez sur **Reply** sous la remarque, écrivez, puis **Comment**.
- Pour corriger : refaites les étapes 5 et 6 (travail dans Jupyter/Colab, dépôt sur la même branche). La PR et les discussions se mettent à jour automatiquement — inutile d'en ouvrir une nouvelle.
- Le dépôt d'origine lance des contrôles automatiques sur la PR. S'ils passent au rouge pour une raison d'environnement qui vous dépasse, signalez-le simplement dans la conversation ; concentrez-vous sur les remarques humaines.
- Une fois la remarque traitée, l'enseignant clôt le fil lui-même : pas d'inquiétude si un fil reste ouvert quelques jours.

## Pièges classiques

| Symptôme | Cause probable | Que faire |
|---|---|---|
| Le bouton **Fork** semble ne rien faire | Dépôt volumineux | Patienter puis rafraîchir ; le fork n'est à faire qu'une fois |
| Le dépôt s'est fait sur **main** au lieu de la branche de TP | Sélecteur de branche non vérifié (étape 6.1) | Ouvrir une demande d'accompagnement plutôt que d'improviser |
| GitHub affiche du JSON illisible | Édition web du `.ipynb` | Ne jamais éditer le JSON : reprendre à l'étape 5 |
| *This branch has no changes* à l'ouverture de la PR | Dépôt sur une autre branche que celle comparée | Vérifier le sélecteur **compare** à l'étape 7.2 |
| Conflits signalés | Le dépôt d'origine a bougé sur le même fichier | Demande d'accompagnement — ne pas cliquer sur *Resolve conflicts* en aveugle |
| Deux groupes sur les mêmes exercices | Réservation non vérifiée | Vérifier les PR ouvertes avant de choisir (voir [TPS-ET-BONUS.md](TPS-ET-BONUS.md)) |

## Rappel sécurité

Ne déposez **jamais** de clé API, de fichier `.env`, de mot de passe ou de donnée personnelle dans un commit — tout ce qui est déposé est public. En cas d'erreur, prévenez immédiatement l'enseignant. Les détails sont dans [TPs dans CoursIA et bonus](TPS-ET-BONUS.md), section *Hygiène et sécurité*.

## En cas de blocage

Chaque séance de TP est l'occasion de poser des questions, et entre les séances, la [demande d'accompagnement](https://github.com/jsboigeEPF/2026-MSAPP3IN08-GenAI/issues/new?template=demande-accompagnement.yml) est le canal prévu — mieux vaut une question tôt qu'un blocage la veille de l'échéance.
