# insight-draft

Kit de démarrage pour rédiger des articles **Insights RodiumAi** et les importer dans le dashboard via upload Markdown.

| Fichier | Rôle |
| ------- | ---- |
| [template.md](./template.md) | Modèle bilingue vide avec tous les marqueurs requis |
| [example.md](./example.md) | Exemple d'article rempli (quickstart API) |
| [AI-PROMPT.md](./AI-PROMPT.md) | Prompt à copier-coller pour ChatGPT, Claude, Cursor, etc. |
| [README.md](./README.md) | Version anglaise de ce guide |

Les insights publiés apparaissent sur [rodiumai.io/insights](https://rodiumai.io/insights).

---

## C'est quoi un Insight ?

Un **Insight** est un article du blog RodiumAi : tutoriels, actualités produit, guides d'intégration, focus modèles, stories communauté, etc.

Plutôt que tout saisir dans l'éditeur du dashboard, vous préparez **un seul fichier `.md`** en local. Le parseur du dashboard lit les marqueurs structurés (`*Title_EN*`, `*Content_EN*`, etc.) et remplit automatiquement le formulaire de publication.

---

## Workflow rapide

1. Copiez [template.md](./template.md) vers `mon-article.md`
2. Rédigez votre contenu (anglais obligatoire, français optionnel)
3. Validez marqueurs et longueur du résumé (voir ci-dessous)
4. Connectez-vous sur [rodiumai.io](https://rodiumai.io)
5. Allez dans **Dashboard → Insights → New**
6. Choisissez **Markdown upload** (ou collez le contenu du fichier)
7. Vérifiez l'aperçu, ajustez si besoin, puis **Publiez**

Vous pouvez aussi utiliser [AI-PROMPT.md](./AI-PROMPT.md) : collez vos notes brutes dans une IA et récupérez un fichier prêt à l'upload.

---

## Format du fichier

Le parseur attend des **marqueurs de section exacts**, chacun sur sa propre ligne. Ne les renommez pas.

```
*Title_EN*
Titre anglais ici

*Title_FR*
Titre français (optionnel)

*Summary_EN*
Résumé anglais (10–500 caractères)

*Summary_FR*
Résumé français (optionnel)

*Tags*
tag-un, tag-deux, sujet

*Content_EN*
## Votre premier titre

Corps Markdown en anglais...

*Content_FR*
## Votre premier titre

Corps Markdown en français (optionnel)...
```

### Sections requises

| Marqueur | Obligatoire | Notes |
| -------- | ----------- | ----- |
| `*Title_EN*` | Oui | Titre principal sur le site |
| `*Summary_EN*` | Oui | 10–500 caractères ; cartes et SEO |
| `*Tags*` | Oui | Séparés par des virgules, minuscules, sans `#` |
| `*Content_EN*` | Oui | Article complet en Markdown |
| `*Title_FR*` | Non | Affiché quand l'utilisateur passe en français |
| `*Summary_FR*` | Non | Résumé carte en français |
| `*Content_FR*` | Non | Corps complet en français |

### Commentaires d'en-tête (optionnels)

Les lignes `#` en haut du fichier sont pour les auteurs :

```markdown
# RodiumAi insight — Markdown upload format
# English required. French optional.
```

---

## Consignes de rédaction

**Marque :** écrire **RodiumAi** (pas RodiumAI, pas Rodium AI).

**Ton :** clair, pratique, accessible. Sections courtes. Pas de pavés.

**Titres :** privilégiez `##` et `###`. Titres courts.

**Liens :** URLs complètes (`https://rodiumai.io/...`).

**Code :** blocs avec langage (` ```bash `, ` ```python `).

**Marketing (si pertinent) :** renvoyez vers inscription, billing, catalogue modèles, clés API ou programme RODISTAR. Aidez le lecteur à passer à l'action.

**Ponctuation :** évitez les tirets longs (`—`). Préférez virgules, deux-points ou phrases courtes.

**Résumés :** une ou deux phrases. Dites ce que le lecteur apprendra et pourquoi c'est utile.

**Tags :** 3 à 8 tags. Exemples : `api`, `integration`, `continue`, `models`, `rodistar`, `getting-started`.

---

## Conseils Markdown

Dans `*Content_EN*` et `*Content_FR*`, le Markdown standard fonctionne :

- **Gras**, *italique*, listes, tableaux, citations
- Images : `![texte alt](https://votre-cdn.com/image.png)`
- Liens vers les pages RodiumAi

Ne **pas** entourer le corps de marqueurs `*Content_*` supplémentaires. Un marqueur d'ouverture, puis tout le contenu jusqu'au marqueur suivant.

---

## Articles bilingues

Bon réflexe : rédiger **anglais et français** pour toucher plus de lecteurs.

Minimum : anglais seul (`*Title_EN*`, `*Summary_EN*`, `*Content_EN*`, `*Tags*`).

Un contenu français sans anglais n'est **pas** pris en charge à l'upload.

---

## Valider avant upload

Checklist :

- [ ] Chaque marqueur est exact (`*Title_EN*`, pas `Title_EN` ou `*Title_EN*:`)
- [ ] `*Summary_EN*` entre 10 et 500 caractères
- [ ] `*Tags*` sur une ligne, virgules
- [ ] `*Content_EN*` non vide
- [ ] Pas de clés API ni secrets dans le fichier
- [ ] Marque **RodiumAi** respectée
- [ ] Fichier `.md` en UTF-8

---

## Fichiers exemples

| Fichier | Description |
| ------- | ----------- |
| [example.md](./example.md) | Quickstart API court (bilingue) |
| [template.md](./template.md) | Point de départ vide |

D'autres exemples publiés vivent dans le monorepo RodiumAi sous `rodiumai_docs/content/` (intégrations, modèles, programme RODISTAR, etc.).

---

## Générer avec une IA

Ouvrez [AI-PROMPT.md](./AI-PROMPT.md), copiez le bloc prompt, collez vos notes ou plan, et demandez à l'IA de renvoyer **uniquement** le fichier `.md` final.

Passez ensuite la checklist ci-dessus avant l'upload.

---

## Dépannage

| Problème | Correction |
| -------- | ---------- |
| Titre non détecté | Marqueur exact `*Title_EN*` sur sa propre ligne |
| Résumé refusé | Ajuster entre 10 et 500 caractères |
| Corps FR absent | Ajouter `*Content_FR*` ou publier en anglais seul |
| Mise en forme cassée | Éviter le HTML ; rester en Markdown |
| Tags non lus | Une ligne, virgules, sans crochets |

---

## Liens

- Hub Insights : [rodiumai.io/insights](https://rodiumai.io/insights)
- Dashboard : [rodiumai.io/dashboard](https://rodiumai.io/dashboard)
- Modèles : [rodiumai.io/models](https://rodiumai.io/models)
- Docs : [rodiumai.io/docs](https://rodiumai.io/docs)

Questions sur la publication ? Contactez l'équipe RodiumAi via [rodiumai.io/contact](https://rodiumai.io/contact).
