---
title: Prompts images — bloc « candidat / propriétaire / IA-humain » (4 séries de 3)
projet: TwinAgent
date: 2026-08-23
remplace: images/3.png, images/2.jpeg, images/4.jpeg
tags: [prompts, images, direction-artistique, twinagent]
---

# Prompts images — bloc « candidat / propriétaire / IA-humain »

**4 séries de 3 images, au choix.** Chacune couvre les mêmes trois lignes `.zz` de
`index.html` (lignes ~1110, ~1135, ~1166) et remplace les visuels actuels. Elles
partagent toutes la **même charte** ci-dessous : ce qui change d'une série à l'autre,
c'est uniquement le **parti pris de cadrage** — donc le rapport au visage.

| Série | Parti pris | Où |
|---|---|---|
| **A** | Documentaire, gens en action, visages de trois quarts | ci-dessous |
| **B** | Aucun visage, gros plans sur les mains | plus bas |
| **C** | La même pièce cadrée trois fois, plans larges | plus bas |
| **D** | Portraits frontaux, protocole identique | plus bas |

→ Comparatif et reco en fin de document. **Ne pas mélanger deux séries** sans lire
la note « combinaison possible ».

**Pourquoi on change.** Les 3 visuels actuels sont exactement ce qu'on veut fuir :
costumes-cravates, tours de bureaux vitrées, open-space gris-bleu, poignée de main
implicite. Or TwinAgent, c'est de la location **entre particuliers**, à Bruxelles,
dans de vrais appartements. Le sujet n'est pas l'entreprise : ce sont deux personnes
ordinaires et un logement.

---

## Charte commune — à coller en tête de CHAQUE prompt, quelle que soit la série

C'est **ce bloc** qui crée l'unité. Il ne change ni d'une image à l'autre, ni d'une
série à l'autre — chaque série ne fait qu'y ajouter un *delta* de cadrage.
Si une seule ligne saute, les 3 images cessent d'être une série.

**Univers**
- Bruxelles, aujourd'hui. Appartement réel : parquet à lames, moulures au plafond,
  châssis bois, radiateur en fonte, mur peint mat, hauteur sous plafond.
  **Jamais** de bureau vitré, d'open-space, de salle de réunion, de gratte-ciel.
- **Les images 2 et 3 se passent dans le MÊME appartement** (même parquet, même
  fenêtre, même mur). C'est ce qui fait tenir la série visuellement.

**Les gens**
- Des habitants, pas des cadres. Vêtements du quotidien : pull, chemise ouverte,
  cardigan, manches retroussées. **Aucun costume, aucune cravate, aucun badge.**
- Âges et morphologies réels, peau réelle (pores, cernes, mèche de travers).
- **Jamais** de regard caméra, jamais de sourire commercial, jamais de pose
  « bras croisés ». Toujours pris en pleine action, de 3/4 ou de profil,
  attention portée sur un objet réel (papier, fenêtre, téléphone).
- Une seule personne par image, sauf image 3 (deux).

**Lumière & optique**
- Lumière naturelle de fenêtre, fin d'après-midi, ciel couvert bruxellois adouci —
  jamais de flash, jamais de néon, jamais de contre-jour spectaculaire.
- 35 mm, f/2.0, hauteur d'yeux, sujet légèrement décentré, arrière-plan qui se
  dissout doucement. Photographie documentaire, pas publicité.

**Étalonnage (aligné sur la palette du site : fond `#F6F5F1`, bleu `#0f4c81`)**
- Base chaude et désaturée : beige, sable, bois, blanc cassé.
- **Un seul rappel de bleu profond par image** (un vêtement, un objet), discret.
- Noirs délavés façon film, grain fin, contraste doux. Pas de bleu-gris froid.

**Interdits (negative prompt)**
> suit, tie, business attire, corporate office, glass partition, open space,
> skyscraper, meeting room, handshake, stock photo smile, looking at camera,
> HDR, oversaturated, teal and orange, neon, lens flare, text, letters, numbers,
> logo, watermark, UI screen, app interface, icons, 3D render, illustration,
> plastic skin, perfect teeth

---

# Série A — « Documentaire »

*Des gens pris en pleine action, visages de trois quarts ou de dos. Le compromis :
on voit des humains, mais jamais frontalement — c'est ce qui évite la banque d'images.*

## A1 · Espace candidat locataire

**Ce que le texte dit :** « Votre dossier est constitué pour chaque annonce.
Les mêmes pièces rassemblées, envoyées par mail, puis dispersées chez des inconnus. »

**L'idée visuelle :** la répétition. On ne montre pas quelqu'un de triste, on montre
**le même dossier photocopié plusieurs fois**, en petites piles identiques. C'est
l'effort refait à zéro, rendu littéral — et ça reste chaleureux parce qu'on est
chez elle, pas dans un bureau.

**Prompt (FR)**
```
[CHARTE COMMUNE ci-dessus]

Photographie documentaire. Une femme d'environ 28 ans, assise à la table de la
cuisine de son petit appartement bruxellois, en fin d'après-midi. Elle porte un
pull en laine bleu profond, les cheveux attachés à la va-vite. Elle est penchée
en avant, de trois quarts dos, en train de glisser une feuille dans une enveloppe.

Devant elle, étalées sur la table en bois : quatre ou cinq petites piles de
documents STRICTEMENT IDENTIQUES, chacune agrafée séparément — la répétition
est le sujet de l'image. À côté, un téléphone posé écran éteint et une tasse
froide. Lumière douce venant de la fenêtre à sa gauche.

Au fond, flou : deux cartons de déménagement encore fermés contre le mur, et un
manteau sur une chaise. L'appartement est vécu, un peu encombré, chaleureux.

Aucun texte lisible sur les documents — seulement la trame grise d'un texte
imprimé, hors de mise au point. 35 mm, f/2.0, grain fin, teintes chaudes et
désaturées.
```

**Prompt (EN — pour Midjourney / Flux)**
```
[COMMON CHARTER]

Documentary photograph. A woman around 28, sitting at the kitchen table of her
small Brussels apartment, late afternoon. Deep blue wool sweater, hair tied up
loosely. Leaning forward, three-quarters from behind, sliding a sheet of paper
into an envelope.

Spread on the wooden table in front of her: four or five small stacks of
STRICTLY IDENTICAL documents, each separately stapled — the repetition is the
subject of the image. Beside them a phone face up, screen off, and a cold cup
of coffee. Soft window light from her left.

Background, out of focus: two still-sealed moving boxes against the wall, a coat
on a chair. Lived-in, slightly cluttered, warm.

No legible text on the documents — only the grey texture of print, out of focus.
35mm, f/2.0, fine grain, warm desaturated tones.
```

---

## A2 · Espace propriétaire

**Ce que le texte dit :** « La préparation du bien, l'annonce et le lien de
candidature ne coûtent rien. Le forfait se déclenche au moment où les dossiers
arrivent. » + badge « Gratuit jusqu'aux candidatures ».

**L'idée visuelle :** le geste gratuit. Une propriétaire ordinaire prépare son
bien **elle-même** — elle photographie sa pièce vide avec son téléphone. Pas de
facture, pas d'agence, pas d'argent à l'image. Le bien est propre, vide, prêt.

> ⚠️ L'image actuelle (facture d'honoraires) racontait l'ancien texte
> « l'agence coûte cher ». Le texte parle maintenant de gratuité et de
> préparation : la facture est devenue hors-sujet. À remplacer, pas à retoucher.

**Prompt (FR)**
```
[CHARTE COMMUNE ci-dessus]

Photographie documentaire. Une femme d'environ 55 ans, cheveux gris coupés court,
cardigan beige, manches retroussées, debout au milieu d'un appartement bruxellois
entièrement vide et fraîchement nettoyé. Parquet à lames clair, moulures au
plafond, grande fenêtre à châssis bois, radiateur en fonte sous la fenêtre.

Elle tient son téléphone à deux mains, à hauteur de poitrine, et photographie
la pièce vide face à elle. Vue de trois quarts, son visage de profil, concentrée,
paisible. On ne voit pas l'écran du téléphone.

Au sol près d'elle : un trousseau de clés, un chiffon plié et une bouteille de
produit ménager. Rien d'autre dans la pièce.

Grande lumière de fin d'après-midi entrant par la fenêtre, qui dessine un
rectangle clair sur le parquet. 35 mm, f/2.0, teintes chaudes et désaturées,
grain fin.
```

**Prompt (EN)**
```
[COMMON CHARTER]

Documentary photograph. A woman around 55, short grey hair, beige cardigan,
sleeves rolled up, standing in the middle of a completely empty, freshly cleaned
Brussels apartment. Pale plank parquet, ceiling mouldings, tall wooden-frame
window, cast-iron radiator beneath it.

She holds her phone with both hands at chest height, photographing the empty
room in front of her. Three-quarter view, face in profile, focused and calm.
The phone screen is not visible.

On the floor near her: a bunch of keys, a folded cloth, a bottle of cleaning
spray. Nothing else in the room.

Broad late-afternoon light through the window drawing a bright rectangle on the
parquet. 35mm, f/2.0, warm desaturated tones, fine grain.
```

---

## A3 · Le travail se répartit. La décision, non.

**Ce que le texte dit :** « L'IA prend l'administratif, répétitif et continu.
L'agent immobilier IPI intervient là où la présence physique et le jugement
changent le résultat. Les visites d'abord. »

**L'idée visuelle :** **ce qui exige d'être là.** Deux personnes, la même
attention portée au même détail physique — une fenêtre qu'on ouvre, qu'on
touche. Pas de poignée de main, pas de contrat tendu, pas de doigt qui pointe
un plan. Le savoir passe par la main sur le châssis.

**Même appartement que l'image 2**, même fenêtre, même heure. C'est la suite
de la même journée.

**Prompt (FR)**
```
[CHARTE COMMUNE ci-dessus]

Photographie documentaire. Le MÊME appartement bruxellois vide que précédemment
(même parquet clair, même grande fenêtre à châssis bois, mêmes moulures), même
lumière de fin d'après-midi.

Deux personnes debout côte à côte devant la fenêtre ouverte, vues de trois
quarts dos. À gauche, un homme d'environ 40 ans, veste en laine bleu profond
sans cravate, chemise ouverte : il a posé la paume à plat sur le montant du
châssis et l'examine de près. À droite, la propriétaire d'environ 55 ans en
cardigan beige, qui suit son geste du regard, une main sur la poignée.

Les deux regardent le même point : le bois de la fenêtre. Aucun contact visuel
entre eux, aucune poignée de main, aucun document dans les mains.

Air extérieur : toits bruxellois flous derrière la vitre. 35 mm, f/2.0, teintes
chaudes et désaturées, grain fin, contraste doux.
```

**Prompt (EN)**
```
[COMMON CHARTER]

Documentary photograph. The SAME empty Brussels apartment as before (same pale
parquet, same tall wooden-frame window, same mouldings), same late-afternoon
light.

Two people standing side by side at the open window, seen three-quarters from
behind. On the left, a man around 40 in a deep blue wool jacket, no tie, open
shirt: his palm rests flat on the window frame as he examines it closely. On
the right, the woman around 55 in the beige cardigan, following his gesture with
her eyes, one hand on the handle.

Both look at the same point: the wood of the window. No eye contact between
them, no handshake, no documents in hand.

Outside: blurred Brussels rooftops through the glass. 35mm, f/2.0, warm
desaturated tones, fine grain, soft contrast.
```

---

# Série B — « Les mains »

*Aucun visage. Trois gros plans sur le geste, dans la même lumière d'appartement.*

**Le pari.** Le visage généré par IA est le premier symptôme « corporate » : dents
parfaites, peau lissée, regard vide. En le supprimant, on supprime le problème à
la racine. Ce qui reste — des mains qui agrafent, qui photographient, qui touchent
un châssis — est **plus humain**, pas moins : c'est le travail réel, pas la pose.

**Delta charte.** On garde tout le bloc commun, on remplace la règle de cadrage :
- 50 mm ou 85 mm, **f/2.8**, distance de travail 40–60 cm. Cadrage serré sur les
  mains et les avant-bras, **le visage est hors champ, coupé au-dessus du coude**.
- Mains réelles : ongles courts non manucurés, une bague usée, une petite cicatrice,
  veines apparentes. **Jamais** de mains de modèle, jamais de manucure.
- Ajouter au negative prompt : `face, portrait, headshot, manicure, hand model`

**B1 · Espace candidat locataire**
```
[CHARTE COMMUNE + DELTA B]

Gros plan sur les mains d'une femme d'environ 28 ans, assise à une table en bois
clair. Manches d'un pull bleu profond retroussées aux avant-bras. Ses deux mains
pressent une agrafeuse de bureau sur une liasse de documents.

Autour, sur la table : quatre autres liasses STRICTEMENT IDENTIQUES, déjà agrafées,
alignées côte à côte. La répétition est le sujet. Une enveloppe kraft vide en bord
de cadre. Le visage est hors champ.

Lumière rasante de fenêtre venant de la gauche. 50 mm, f/2.8, grain fin, teintes
chaudes et désaturées.
```

**B2 · Espace propriétaire**
```
[CHARTE COMMUNE + DELTA B]

Gros plan sur les mains d'une femme d'environ 55 ans, manches d'un cardigan beige
retroussées. Elle tient un téléphone à deux mains, à la verticale, bras tendus
vers l'avant. On voit le dos du téléphone, jamais l'écran.

Derrière ses mains, hors de mise au point : un appartement bruxellois entièrement
vide — parquet clair, plinthe blanche, grande fenêtre à châssis bois. Un trousseau
de clés posé sur le parquet en bas de cadre, net.

Grande lumière de fin d'après-midi. 50 mm, f/2.8, grain fin, teintes chaudes.
```

**B3 · Le travail se répartit. La décision, non.**
```
[CHARTE COMMUNE + DELTA B]

Gros plan sur deux paires de mains devant une fenêtre à châssis bois ouverte, dans
le même appartement vide. À gauche, la main d'un homme d'environ 40 ans, manche de
laine bleu profond, paume posée à plat sur le montant en bois, doigts qui suivent
une fissure de la peinture. À droite, la main d'une femme plus âgée, manche de
cardigan beige, tenant la poignée de la fenêtre.

Les deux mains sont à quelques centimètres l'une de l'autre sans se toucher.
Aucun visage, aucun document. Toits bruxellois flous derrière la vitre.

50 mm, f/2.8, grain fin, contraste doux, teintes chaudes.
```

---

# Série C — « La même pièce, trois fois »

*Un seul appartement, un seul cadrage, trois occupants différents. Plans larges.*

**Le pari.** L'unité n'est plus une question de style, elle devient **structurelle** :
c'est littéralement la même image, au même endroit, à trois moments. Au scroll, le
lecteur reconnaît la pièce et comprend tout seul que les trois rôles tournent autour
du même bien. C'est le concept « Twin » rendu visible sans une seule icône.

**Delta charte.** On garde tout le bloc commun, on remplace la règle de cadrage :
- **Plan large, 28 mm, f/4**, appareil sur pied, **hauteur 1 m 40, angle rigoureusement
  identique** dans les trois images. Le mur du fond, la fenêtre et le bord du parquet
  sont exactement aux mêmes coordonnées.
- La personne occupe **moins d'un cinquième** de la hauteur du cadre, décentrée.
  La pièce est le sujet ; l'humain l'habite.
- La lumière progresse : C1 milieu de journée → C2 fin d'après-midi → C3 lumière
  basse et dorée. Même fenêtre, même angle, heure différente.
- Ajouter au negative prompt : `close-up, portrait, shallow depth of field`

**C1 · Espace candidat locataire**
```
[CHARTE COMMUNE + DELTA C]

Plan large, appareil sur pied à 1 m 40. Un séjour bruxellois vide : parquet à lames
clair, moulures au plafond, grande fenêtre à châssis bois au fond à droite,
radiateur en fonte dessous, mur peint blanc cassé. Lumière neutre de milieu de
journée.

Au fond de la pièce, petite dans le cadre, une femme d'environ 28 ans en pull bleu
profond, debout, de trois quarts dos, en train de sortir. Elle serre une liasse de
documents contre elle d'un bras. Elle vient de visiter. La porte est entrouverte
derrière elle.

La pièce est vide, propre, un peu froide. 28 mm, f/4, tout est net, grain fin,
teintes chaudes et désaturées.
```

**C2 · Espace propriétaire**
```
[CHARTE COMMUNE + DELTA C]

EXACTEMENT le même séjour, le même cadrage, le même angle et la même hauteur
d'appareil que l'image précédente — même parquet, même fenêtre au fond à droite,
même radiateur, mêmes moulures. Lumière de fin d'après-midi, plus chaude, qui
dessine un rectangle clair sur le parquet.

Cette fois, seule dans la pièce : une femme d'environ 55 ans, cardigan beige,
manches retroussées, debout au centre-gauche, petite dans le cadre. Elle lève son
téléphone à deux mains et photographie le mur du fond. Un seau et un chiffon posés
au sol près d'elle.

28 mm, f/4, tout est net, grain fin, teintes chaudes.
```

**C3 · Le travail se répartit. La décision, non.**
```
[CHARTE COMMUNE + DELTA C]

EXACTEMENT le même séjour, le même cadrage, le même angle et la même hauteur
d'appareil que les deux images précédentes. Lumière basse et dorée de fin de
journée, entrant en biais par la fenêtre du fond.

Deux personnes debout côte à côte devant la fenêtre, petites dans le cadre, vues
de trois quarts dos : un homme d'environ 40 ans en veste de laine bleu profond sans
cravate, paume posée sur le montant de la fenêtre, et la femme d'environ 55 ans en
cardigan beige à côté de lui. Ils regardent tous les deux le même point : le bois
du châssis.

La pièce est toujours vide. Aucune poignée de main, aucun document. 28 mm, f/4,
tout est net, grain fin, teintes chaudes.
```

---

# Série D — « Le protocole » (portraits frontaux)

*Le pari inverse de la série B : que des visages, mais tous shootés à l'identique.*

**Le pari.** Ce qui rend une photo « corporate », ce n'est pas le visage frontal —
c'est la **pose**. Bras croisés, sourire, menton relevé. Un protocole de portrait
documentaire (même distance, même hauteur, même posture, aucune expression jouée,
mains le long du corps ou tenant un objet réel) produit exactement l'inverse :
des gens qui existent, filmés comme un inventaire humain. C'est la série la plus
chaleureuse — et la plus risquée à générer.

**Delta charte.** On garde tout le bloc commun, on remplace la règle des visages :
- **Regard caméra assumé, expression neutre, aucun sourire.** Bouche fermée,
  épaules relâchées, aucune main sur la hanche, aucun bras croisé.
- **Protocole identique** : 50 mm, f/2.8, appareil à hauteur des yeux, personne
  cadrée à mi-cuisse, centrée, à 2 m 50 du mur du fond, même distance dans les trois.
- Peau réelle et non retouchée : pores, cernes, rides d'expression au repos, une
  mèche mal placée, un col légèrement de travers.
- Ajouter au negative prompt : `smiling, laughing, arms crossed, hand on hip,
  retouched skin, beauty retouch, headshot lighting, studio backdrop`

> ⚠️ **C'est la série où l'IA se plantera le plus.** Un visage frontal généré
> retombe vite dans le lissé publicitaire. Prévoir beaucoup d'itérations — ou
> assumer que cette direction mérite un vrai shooting photo (2 h, 3 personnes,
> un appartement prêté). C'est aussi celle qui, bien faite, décrocherait le site
> de tout ce qui existe sur le marché belge.

**D1 · Espace candidat locataire**
```
[CHARTE COMMUNE + DELTA D]

Portrait documentaire, protocole fixe. Une femme d'environ 28 ans, pull en laine
bleu profond, cheveux attachés à la va-vite, debout et centrée dans son petit
séjour bruxellois. Cadrée à mi-cuisse, à hauteur des yeux.

Elle tient devant elle, à deux mains, une liasse épaisse de documents agrafés.
Elle regarde l'objectif, expression neutre, bouche fermée, aucun sourire. Épaules
relâchées, fatiguée mais droite.

Derrière elle, légèrement flou : un mur blanc cassé, deux cartons de déménagement
encore fermés, un manteau sur une chaise. Lumière douce de fenêtre venant de la
gauche.

50 mm, f/2.8, peau réelle non retouchée, grain fin, teintes chaudes et désaturées.
```

**D2 · Espace propriétaire**
```
[CHARTE COMMUNE + DELTA D]

Portrait documentaire, MÊME protocole exactement : même distance, même hauteur
d'appareil, même cadrage à mi-cuisse, personne centrée.

Une femme d'environ 55 ans, cheveux gris coupés court, cardigan beige, manches
retroussées, debout au centre de son appartement bruxellois entièrement vide.
Elle tient un trousseau de clés dans la main droite, le long du corps. Un
téléphone dans l'autre main, écran contre la cuisse.

Elle regarde l'objectif, expression neutre, aucun sourire. Derrière elle, flou :
parquet clair, plinthe blanche, grande fenêtre à châssis bois. Lumière de fin
d'après-midi.

50 mm, f/2.8, peau réelle non retouchée, grain fin, teintes chaudes.
```

**D3 · Le travail se répartit. La décision, non.**
```
[CHARTE COMMUNE + DELTA D]

Portrait documentaire à deux, MÊME protocole exactement : même distance, même
hauteur d'appareil, même cadrage à mi-cuisse. Les deux personnes centrées, côte à
côte, séparées d'une vingtaine de centimètres, dans le même appartement vide que
l'image précédente.

À gauche, un homme d'environ 40 ans, veste en laine bleu profond sans cravate,
chemise ouverte, une main tenant un mètre ruban replié le long du corps. À droite,
la femme d'environ 55 ans en cardigan beige, trousseau de clés à la main.

Tous les deux regardent l'objectif, expression neutre, aucun sourire, aucun
contact entre eux, aucune poignée de main. Ils sont là ensemble, à égalité.

Lumière de fin d'après-midi par la fenêtre hors champ à gauche. 50 mm, f/2.8,
peau réelle non retouchée, grain fin, teintes chaudes.
```

---

## Comparatif des 4 séries

| | Unité | Risque « corporate » | Difficulté de génération | Ce que ça raconte |
|---|---|---|---|---|
| **A · Documentaire** | Bonne | Faible | Moyenne | Le travail réel, en cours |
| **B · Les mains** | **Très forte** | **Quasi nul** | **Faible** | Le geste, l'effort concret |
| **C · La même pièce** | **Maximale** | Faible | Moyenne | Un bien, trois rôles autour |
| **D · Le protocole** | Forte | Moyen | **Élevée** | Des gens, à égalité |

**Ma reco.** **B en principale.** C'est la seule qui neutralise complètement le
problème de fond — les visages générés par IA — tout en étant *plus* humaine que
les visuels actuels, et c'est la plus rapide à produire correctement. **C en
alternative forte** si Laurent veut qu'on comprenne le concept « twin » au premier
coup d'œil : le cadrage répété fait le travail narratif à la place du texte.

**A** reste le filet de sécurité : c'est la plus consensuelle, celle qui ressemble
le plus à ce à quoi on s'attend, sans les costumes.

**D** est la plus forte artistiquement et la seule qui donnerait au site une
identité vraiment propre — mais elle ne tiendra probablement pas en 100 % IA.
À proposer à Laurent comme la version « si on met un budget shooting ».

**Combinaison possible** si aucune ne tranche : **B pour les images 1 et 2** (les
gestes solitaires, où le visage n'apporte rien) et **A3 ou D3 pour la troisième**
(la rencontre, où voir deux personnes ensemble porte le message « IA + humain »).
C'est un mélange assumé, pas un compromis mou — à condition de garder la charte
commune intacte.

---

## Format & specs techniques — valables pour les 4 séries

| | Valeur |
|---|---|
| **Ratio** | **4:3** (imposé par le CSS `aspect-ratio:4/3` sur `.photo`) |
| **Taille de génération** | **1600 × 1200 px** (minimum acceptable 1400 × 1050) |
| **Export final** | JPEG qualité 82–85, **< 350 Ko** par image |
| **Nom de fichier** | `images/candidat.jpg`, `images/proprietaire.jpg`, `images/repartition.jpg` |

**Points de vigilance liés au code**

- Les images actuelles font **1408 × 768** (≈16:9). Le CSS les recadre en
  `object-fit:cover` dans un cadre 4:3 → **~30 % de la largeur est perdue** à
  gauche et à droite. Générer directement en 4:3 supprime ce problème.
- `.photo::after` pose un **dégradé blanc semi-transparent depuis le coin haut
  gauche** (`radial-gradient(120% 90% at 20% 10%, rgba(255,255,255,.55)…)`).
  → **Ne rien mettre d'important dans le quart supérieur gauche** : visage,
  main, objet clé. Cette zone sera lavée.
- Le cadre a des **coins arrondis de 22 px** appliqués par le CSS →
  ne pas les dessiner dans l'image.
- Une **boule bleue floutée** (`.photo-ball`, le bleu `#0f4c81`) déborde derrière
  chaque image. C'est elle qui justifie le rappel de bleu unique dans chaque
  visuel : les images doivent dialoguer avec ce halo, pas le contredire.
- **Aucun texte, aucun logo, aucune icône** : Laurent n'aime pas les icônes, et
  tout texte généré par IA sortira illisible et non traduisible.

**Après génération — mettre à jour les `alt` dans `index.html`**

```
l.1110  alt="Une candidate prépare, chez elle, plusieurs fois le même dossier de location"
l.1135  alt="Une propriétaire photographie elle-même son appartement vide pour l'annonce"
l.1166  alt="Un agent immobilier IPI et la propriétaire examinent ensemble la fenêtre lors d'une visite"
```

---

## Questions ouvertes (à trancher avec Laurent)

1. **Genre des personas.** J'ai mis une candidate (28 ans) et une propriétaire
   (55 ans) pour sortir du duo d'hommes en costume actuel. Laurent a-t-il un
   parti pris ? (À noter : image 3 met l'agent IPI en homme — inversable.)
2. **Quelle série ?** C'est la vraie question à poser en premier — elle décide de
   tout le reste. Le curseur va de « aucun visage » (B) à « que des visages » (D).
   Ma reco : **B**, avec **C** en alternative. Voir le comparatif ci-dessus.
3. **Le même appartement d'une image à l'autre** : c'est ma reco dans les quatre
   séries (unité forte, et gratuit à produire). Alternative : trois lieux
   distincts, plus varié mais plus décousu.
4. **Bruxelles reconnaissable ?** Je suis resté sur des indices discrets
   (moulures, châssis, toits flous). On peut pousser plus loin (façade, rue)
   si on veut ancrer le périmètre 19 communes visuellement.
5. **Budget shooting ?** La série D n'est honnêtement pas atteignable en 100 % IA.
   Si Laurent y tient, la question devient : est-ce qu'on met une demi-journée de
   photographe et un appartement prêté ? À poser explicitement, sinon on va
   itérer dans le vide.
