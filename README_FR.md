<div align="center">
  <img src="skills/kami/assets/images/logo.svg" width="120" />
  <h1>Kami</h1>
  <p><b>Un bon contenu mérite une belle typographie.</b></p>
  <p><a href="README.md">English</a> · <a href="README_CN.md">中文</a> · <a href="README_TW.md">繁體</a> · <a href="README_JA.md">日本語</a> · <a href="README_KR.md">한국어</a> · <a href="README_DE.md">Deutsch</a> · Français</p>
  <a href="https://github.com/tw93/kami/stargazers"><img src="https://img.shields.io/github/stars/tw93/kami?style=flat-square" alt="Stars"></a>
  <a href="https://github.com/tw93/kami/releases"><img src="https://img.shields.io/github/v/tag/tw93/kami?label=version&style=flat-square" alt="Version"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square" alt="License"></a>
  <a href="https://twitter.com/HiTw93"><img src="https://img.shields.io/badge/follow-Tw93-red?style=flat-square&logo=Twitter" alt="Twitter"></a>
</div>

## Pourquoi Kami

Kami apporte aux documents et pages web une typographie soignée et chaleureuse inspirée du papier. Créez des PDF élégants, des images haute résolution ou exportez vos présentations en diapositives PowerPoint modifiables.

Kami (紙, かみ) signifie « papier » en japonais. Il intègre huit modèles de documents, un système de landing pages et des règles de contrôle de contenu et de mise en page.

Fait partie d'une trilogie : [Kaku](https://github.com/tw93/Kaku) (書く) écrit le code, [Waza](https://github.com/tw93/Waza) (技) forge les habitudes, [Kami](https://github.com/tw93/Kami) (紙) livre les documents.

## Exemples

Exemples de PDF en plusieurs formats et langues. Cliquez sur un aperçu pour l'ouvrir.

<table>
<tr>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-musk-resume.pdf"><img src="site/assets/demos/demo-musk-resume.png" alt="CV de fondateur"></a>
    <br><b>CV</b> · Anglais
    <br><sub>CV de fondateur, 2 pages</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-kami-print.pdf"><img src="site/assets/demos/demo-kami-print.png" alt="Synthèse imprimable Kami"></a>
    <br><b>One-Pager</b> · 中文
    <br><sub>Présentation Kami · Version imprimable</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-tesla.pdf"><img src="site/assets/demos/demo-tesla.png" alt="Rapport d'analyse Tesla"></a>
    <br><b>Rapport financier</b> · 中文
    <br><sub>Analyse des résultats Tesla T1 2026</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-agent-slides.pdf"><img src="site/assets/demos/demo-agent-slides.png" alt="Diapositives de conférence" /></a>
    <br><b>Diapositives</b> · Anglais
    <br><sub>Présentation sur les agents, 8 pages</sub>
  </td>
</tr>
<tr>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-mole.pdf"><img src="site/assets/demos/demo-mole.png" alt="Présentation produit Mole"></a>
    <br><b>Fiche produit</b> · Anglais
    <br><sub>Présentation de Mole, 1 page</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-letter.pdf"><img src="site/assets/demos/demo-letter.png" alt="Lettre de recommandation"></a>
    <br><b>Lettre</b> · 中文
    <br><sub>Lettre de recommandation, 1 page</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-changelog.pdf"><img src="site/assets/demos/demo-changelog.png" alt="Notes de version Mole"></a>
    <br><b>Changelog</b> · Anglais
    <br><sub>Notes de version de Mole v1.7.1</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-kaku.pdf"><img src="site/assets/demos/demo-kaku.png" alt="Portfolio Kaku"></a>
    <br><b>Portfolio</b> · 日本語
    <br><sub>Portfolio du terminal Kaku, 7 pages</sub>
  </td>
</tr>
</table>

## Installation

**Claude Code, Codex, Cursor et autres agents**

```bash
npx skills add tw93/kami -a claude-code codex cursor -g -y
```

Ou demandez directement à votre agent :
> Installe Kami en lisant https://kami.tw93.fun/llms.txt

Une copie est installée dans `~/.agents/skills`, le répertoire partagé des skills. Claude Code y est relié par lien symbolique ; Codex, Cursor et les autres agents accèdent à Kami via `/kami`. Mise à jour avec `npx skills update -g -y`.

**Plugin hôte**, si vous préférez la commande de mise à jour native (espace de noms `/kami:kami` ; Claude Code v2.1.142 ou plus récent) :

```bash
# Claude Code (mise à jour : claude plugin update kami)
/plugin marketplace add tw93/kami
/plugin install kami@kami

# Codex (mise à jour : codex plugin marketplace upgrade kami, puis codex plugin add kami@kami)
codex plugin marketplace add tw93/kami
codex plugin add kami@kami
```

**Claude Desktop** : téléchargez l'archive officielle [kami.zip](https://github.com/tw93/kami/releases/latest/download/kami.zip) (et non le ZIP du code source GitHub), ouvrez Paramètres > Skills > « + » > Create skill et déposez l'archive. Pour mettre à jour, cliquez sur « ... » sur la carte du skill et choisissez Remplacer.

Les polices CJK volumineuses ne sont pas incluses dans le paquet : `skills/kami/scripts/ensure-fonts.sh` télécharge les polices chinoises ou coréennes manquantes dans le répertoire des polices de l'utilisateur.

Kami vérifie discrètement la disponibilité d'une nouvelle version au plus une fois par jour. Aucune donnée personnelle ou contenu de document n'est envoyé ; en mode hors ligne ou sans accès au cache local, la vérification est ignorée en silence.

## Utilisation

Le skill se déclenche automatiquement à partir de requêtes formulées en langage naturel, sans commande spéciale.

### Langues prises en charge

L'anglais et le chinois bénéficient du support le plus complet. Le japonais et le coréen utilisent des polices de substitution dédiées et des ajustements de mise en page, chaque document étant vérifié avant livraison :

| Langue | Niveau de prise en charge | Police serif par défaut |
| :--- | :--- | :--- |
| **Anglais** | Complet | Charter |
| **Chinois** (简体 / 繁體) | Complet | TsangerJinKai02 (仓耳今楷) |
| **Japonais** (日本語) | Polices de secours & vérification | YuMincho (游明朝) |
| **Coréen** (한국어) | Polices de secours & vérification | Source Han Serif K (본명조) |

Exemples de requêtes :

- Anglais : `make a one-pager for my startup` / `turn this research into a long doc` / `write a formal letter` / `make a portfolio of my projects` / `build me a resume` / `design a slide deck for my talk` / `build a landing page for my app`
- Chinois : `帮我做一份一页纸` / `帮我排版一份长文档` / `帮我写一封正式信件` / `帮我做一份作品集` / `帮我做一份简历` / `帮我做一套演讲幻灯片` / `帮我做一个产品落地页`
- Français : `Crée une fiche de synthèse pour mon projet` / `Mets en page cette recherche en document complet` / `Rédige une lettre officielle` / `Conçois un portfolio de mes projets` / `Crée un CV pour moi` / `Prépare des diapositives de présentation` / `Crée une landing page pour mon application`

**Profil de marque** (optionnel)

Créez `~/.config/kami/brand.md` pour conserver votre identité, vos couleurs et vos préférences d'écriture. Consultez [brand.example.md](skills/kami/references/brand.example.md) pour voir un modèle complet.

## Principes de conception

Les valeurs par défaut associent un fond parchemin chaleureux (`#f5f4ed`), des touches bleu encre (`#1B365D`) et des polices avec empattement (serif). La hiérarchie visuelle repose sur la taille des caractères et les espaces blancs.

- **Modèles.** Huit modèles de documents : Fiche synthétique (One-Pager), Document long, Lettre, Portfolio, CV, Diapositives, Rapport d'analyse et Journal des modifications (Changelog), ainsi qu'un système de landing page.
- **Schémas.** 18 types de diagrammes vectoriels SVG intégrés. Les diagrammes de séquence, de classes et entité-association peuvent être rédigés en syntaxe Mermaid : [beautiful-mermaid](https://github.com/lukilabs/beautiful-mermaid) génère le SVG et `skills/kami/scripts/mermaid_normalize.py` l'harmonise avec la palette de Kami.
- **Diapositives.** Trois moteurs de rendu : WeasyPrint HTML vers PDF par défaut, python-pptx pour des fichiers PowerPoint modifiables sur demande, et une variante Marp dans `skills/kami/assets/templates/marp/`.
- **Code source.** Coloration syntaxique via Pygments si la bibliothèque est installée ; sinon, le code s'affiche en monochrome clair et lisible.
- **Validation.** Des schémas de contenu valident la structure avant mise en page ; un contrôle de couverture s'assure qu'aucun point clé n'a été oublié.
- **Serveur MCP.** Un serveur léger (`skills/kami/scripts/mcp_server.py`) expose des outils de diagnostic, de rendu et de capture d'écran pour tout agent compatible MCP.
- **Impression.** Une variante papier blanc permet d'adapter n'importe quel document aux imprimantes de bureau sans fond parchemin, tout en conservant les teintes douces des encadrés.

Police par défaut selon la langue : chinois (TsangerJinKai02), japonais (YuMincho), coréen (Source Han Serif K), anglais/français (Charter).

Spécifications complètes : [design.md](skills/kami/references/design.md). Aide-mémoire : [CHEATSHEET.md](skills/kami/CHEATSHEET.md).

## Au-delà du document

Les mêmes principes s'appliquent aux pages d'accueil de produits et aux prompts de génération d'images.

<table>
<tr>
  <td align="center" width="25%" valign="top">
    <a href="https://kami.tw93.fun"><img src="site/assets/showcase/kami-landing.png" alt="Landing page Kami" height="150"></a>
    <br><b>Kami</b> · landing page
    <br><sub>Site officiel du design system</sub>
  </td>
  <td align="center" width="25%" valign="top">
    <a href="https://mole.fit"><img src="site/assets/showcase/mole-landing.png" alt="Landing page Mole" height="150"></a>
    <br><b>Mole</b> · landing page
    <br><sub>Utilitaire système macOS</sub>
  </td>
  <td align="center" width="25%" valign="top">
    <img src="site/assets/illustrations/travel-spatialvla.png" alt="Schéma d'architecture SpatialVLA" height="150">
    <br><b>Architecture</b> · Anglais
    <br><sub>Schéma redessiné SpatialVLA</sub>
  </td>
  <td align="center" width="25%" valign="top">
    <img src="site/assets/illustrations/travel-tesla-optimus.png" alt="Brevet Tesla Optimus" height="150">
    <br><b>Schéma brevet</b> · 中文
    <br><sub>Schéma du brevet Tesla Optimus</sub>
  </td>
</tr>
</table>

Les landing pages sont livrées prêtes à déployer en versions multilingues.

Exemple de prompt pour modèles d'images :

```text
Redraw this as a clean editorial diagram. Background: warm parchment (#f5f4ed), never pure white. One accent only, ink blue (#1B365D); everything else in warm gray with a yellow-brown undertone, no other colors. Thin single-line geometric strokes and simple flat icons. No gradients, no drop shadows, no 3D. Labels in a serif typeface. Generous whitespace, calm and composed, like a figure in a well-typeset report.
```

## Genèse

J'investis sur les marchés américains et je demande souvent à Claude de rédiger des synthèses d'analyse. Chaque document avait la même apparence terne par défaut : gris, uniforme, avec une structure différente à chaque session. Rien ne donnait envie de poursuivre la lecture. J'ai alors commencé à ajuster la typographie, les teintes et les espacements, règle après règle, jusqu'à obtenir des pages agréables à lire.

Plus tard, devant préparer une présentation sur les agents d'IA, je disposais déjà du contenu textuel sans vouloir reconstruire des diapositives de zéro. J'ai utilisé Claude Design pour concevoir la mise en page dans mon propre style. Cette démarche a vu naître les diagrammes SVG intégrés et une palette chaleureuse et cohérente. Ce système couvrant désormais l'ensemble de mes documents, j'ai réuni ces modèles et ces règles au sein de Kami.

## Soutien

1. La façon la plus directe de me soutenir est d'acheter [Mole for Mac](https://mole.fit), mon application de nettoyage pour Mac.
2. Si Kami vous a été utile, vous pouvez lui attribuer une étoile sur GitHub, [le recommander](https://twitter.com/intent/tweet?url=https://github.com/tw93/kami&text=Kami%20-%20A%20quiet%20design%20system%20for%20professional%20documents.) ou contribuer via une issue ou une PR.
3. J'ai deux chats, TangYuan et Coke. Si Kami embellit vos journées, vous pouvez leur offrir <a href="https://cats.tw93.fun?name=Kami" target="_blank">une friandise 🥩</a>.

<details>
<summary>Ceux qui ont déjà manifesté leur soutien 🐱</summary>
<br/>
<a href="https://cats.tw93.fun?name=Kami"><img src="https://cdn.jsdelivr.net/gh/tw93/sponsors@main/assets/sponsors.svg" width="1000" loading="lazy" /></a>
</details>

## Licence

Licence MIT pour le code et les modèles de Kami.

**Polices** : TsangerJinKai02 est gratuite pour un usage personnel uniquement ; un usage commercial requiert une licence auprès de [tsanger.cn](https://tsanger.cn). Charter, YuMincho, Source Han Serif K (OFL) et les polices de secours CJK sont intégrées au système ou sous licence libre.
