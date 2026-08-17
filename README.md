# Website-Twin-Agent-V1

Site vitrine Twin Agents — une seule page, `index.html`, sans build ni dépendances.
Tout est dedans : HTML, CSS et JS. Les visuels sont dans `images/` et `images-biens-immo/`.

- **Dépôt** : https://github.com/JulesMartin/Website-Twin-Agent-V1 (branche `main`)
- **Hébergement** : Vercel, projet `website-twin-agent-v1`
- **URL publique** : https://website-twin-agent-v1.vercel.app

---

## ⚠️ À FAIRE : l'auto-déploiement est cassé

**Symptôme** — vous poussez sur GitHub, le site en ligne ne change pas.

**Constat au 17 août 2026** — le projet Vercel n'a qu'**un seul déploiement depuis sa
création**, celui du 5 août (commit `f28c3ae`). Les commits poussés depuis n'ont
déclenché aucun build : aucun déploiement, aucun check GitHub. Le 5 août
l'intégration marchait encore (le build partait 55 secondes après le commit), donc
la connexion GitHub → Vercel s'est rompue quelque part entre les deux.

### La marche à suivre

1. Ouvrir https://vercel.com/jules-projects-4bdb74f2/website-twin-agent-v1
2. Aller dans **Settings → Git**
3. Regarder l'état du dépôt connecté :
   - **Aucun dépôt connecté** → cliquer **Connect Git Repository** et choisir
     `JulesMartin/Website-Twin-Agent-V1`, branche de production `main`.
   - **Le dépôt est connecté** → le problème vient des droits de l'app GitHub.
     Aller sur https://github.com/settings/installations → **Vercel** →
     **Configure**, et vérifier que `Website-Twin-Agent-V1` fait bien partie des
     dépôts autorisés (si l'accès est en « Only select repositories », il faut
     ajouter ce dépôt à la liste). Puis revenir sur Vercel et reconnecter.
4. Vérifier aussi, dans **Settings → Git**, que l'**Ignored Build Step** est vide
   et que les déploiements automatiques sur `main` ne sont pas désactivés.
5. Une fois reconnecté, déclencher un build : soit en poussant n'importe quel
   commit, soit depuis l'onglet **Deployments → Redeploy** en cochant
   *Use existing Build Cache = off*.

### Vérifier que c'est reparti

```bash
# doit afficher le commit courant, pas f28c3ae
gh api repos/JulesMartin/Website-Twin-Agent-V1/deployments \
  --jq '.[] | "\(.created_at)  \(.sha[0:7])"'

# doit renvoyer 1 ou plus (la police actuelle du site)
curl -s https://website-twin-agent-v1.vercel.app/ | grep -c Lora
```

### Solution de secours : déployer à la main

Si l'intégration Git reste capricieuse, un déploiement ponctuel depuis la machine :

```bash
npx vercel login          # login navigateur, à faire une fois
npx vercel link           # rattacher le dossier au projet website-twin-agent-v1
npx vercel --prod         # publier en production
```

⚠️ Un déploiement CLI publie le **dossier local**, pas le contenu de GitHub.
Pensez à commiter et pousser d'abord, sinon le site et le dépôt divergent.

---

## Workflow normal (une fois l'auto-déploiement réparé)

```bash
git add -A
git commit -m "…"
git push origin main      # Vercel rebuild et publie tout seul en ~1 min
```

---

## Personnalisation rapide

Tout se règle dans le bloc `:root` en haut du `<style>` de `index.html`.

### Les couleurs — 3 lignes

```css
--brand:#0f4c81;        /* couleur principale : boutons, accents, liens actifs */
--brand-soft:#eaf4fb;   /* couleur secondaire : fonds clairs, badges, halos    */
--brand-rgb:15, 76, 129;/* LA MÊME que --brand, en R,G,B (ombres translucides) */
```

`--brand-rgb` doit toujours rester synchronisée avec `--brand`, sinon les ombres
et les halos gardent l'ancienne teinte.

### La police des titres — 1 ligne

```css
--font-serif:'Lora', Georgia, serif;
```

Elle pilote toute la typo « serif » du site : titres, chiffres du parcours,
tarifs, citations, noms d'offres.

**Si vous changez pour une police qui n'est pas déjà chargée**, il faut aussi
remplacer le mot `Lora` dans le `<link>` Google Fonts du `<head>` — Google ne
sert que les familles explicitement demandées dans l'URL.

---

## Structure de la page

Les sections dans l'ordre, avec leur ancre :

| `id` | Contenu |
|---|---|
| `#top` | hero |
| `#probleme` | les constats, en zigzag texte / visuel |
| `#profil` | sélecteur Propriétaire / Candidat locataire |
| `#tunnel` | le parcours, 6 étapes en version propriétaire **et** 6 en version locataire |
| `#video` | le concept expliqué |
| `#autonomie` | console Twin AI / Twin AI + Twin Human |
| `#pricing` | tarifs, cartes retournables |
| `#fonctionnalites` | détail des fonctionnalités |
| `#confiance` | réassurance |
| `#faq` | questions fréquentes |
| `#final` | appel à l'action |

Le sélecteur de profil pose `data-profile` sur le `<body>` ; les classes
`.only-owner` et `.only-tenant` font le tri. Les animations au défilement passent
toutes par un `IntersectionObserver` qui ajoute la classe `.in`.

## Aperçu en local

```bash
python3 -m http.server 8000   # puis http://localhost:8000
```

Ouvrir le fichier en `file://` fonctionne aussi, mais un serveur local évite les
surprises sur les chemins d'images.

## Fichiers annexes

- `index copie.html` — ancienne version conservée, **non publiée**
- `anciennes-notes/` — notes projet et white paper
- `Composition*.mp4` — rushes vidéo
