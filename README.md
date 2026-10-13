# Objectif NCLC — entraînement gratuit TCF Canada (expression orale et écrite)

Site : https://outils.vread.fr/tcf-canada-entrainement/ (FR) · https://outils.vread.fr/tcf-canada-entrainement/en/ (EN)

Pack gratuit : format officiel des tâches (source FEI), guide du temps, 42 sujets **originaux**, table IRCC des notes vers les
NCLC et grilles d'auto-évaluation. Un produit de READ FRANCE SAS.

**Non officiel** : non affilié à France Éducation international (FEI) ni à IRCC. TCF est une marque de France Éducation
international. Aucun sujet d'examen réel n'est utilisé ni accepté dans ce dépôt (les sujets sont confidentiels).

Téléchargement gratuit (GitHub Releases) : `pack-entrainement-tcf-canada-expression.pdf`

Version payante (pass corrigé par IA, 29 $ CA / 30 jours) : **pas encore disponible**, aucun paiement possible.

## Mesure d'audience (depuis le 2026-10-13)

`assets/mesure.js` (compteur d'audience anonyme, `v:2`, robots / navigateurs automatisés / `octave_notrack=1` comptés à
part) et `assets/cro.js` (compteurs agrégés de comportement) sont copiés **à l'identique** depuis
`VREAD-corp/octave-checkout` (`gas/web/`, ne jamais modifier les copies). Chargés sur chaque page par `build.py`
(`data-site="tcf-canada-entrainement"`, avec empreinte `?v=`), ils envoient l'action `track` au backend France `octave-pay-gas`, qui
accepte ce site. Clics comptés : PDF gratuits (`free_download`) et page « version payante » (`cta_click`). Aucun cookie,
aucun identifiant, rien sous Do Not Track / GPC ; nos tests ajoutent `?octave_notrack=1`. Détails :
`content/confidentialite.html`. Après une mise à jour du snippet maître : recopier les deux fichiers puis
`node tests/cro.check.mjs assets/cro.js`.

## Structure

- `content/` — pages ; `pdf/` — source HTML du PDF ; `build.py` — générateur statique sans dépendance
- `tests/test_site.py` — vérifications ; `scripts/make_pdf.mjs` — rendu PDF ; `scripts/check_live.mjs` — contrôle en ligne

```sh
python3 build.py && python3 tests/test_site.py
npm i && node scripts/make_pdf.mjs
```

Contenus : CC BY 4.0. Code : MIT. Signaler une erreur : onglet Issues (tickets publics, aucune donnée personnelle).
