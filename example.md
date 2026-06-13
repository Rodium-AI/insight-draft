# RodiumAi insight — Markdown upload format
# English required. French optional. Keep *Section* markers exactly as shown.

*Title_EN*
Getting started with the RodiumAi API in 5 minutes

*Title_FR*
Démarrer avec l'API RodiumAi en 5 minutes

*Summary_EN*
Create a RodiumAi account, generate an API key, recharge RODI credits, and send your first chat completion to https://api.rodiumai.io/v1 with any catalogue model slug.

*Summary_FR*
Créez un compte RodiumAi, générez une clé API, rechargez des crédits RODI et envoyez votre première requête chat à https://api.rodiumai.io/v1 avec n'importe quel slug du catalogue.

*Tags*
getting-started, api, rodi, models, quickstart, developer-tools

*Content_EN*

## Why RodiumAi?

**RodiumAi** is a pay-as-you-go AI platform built for Africa. One API key, one wallet (**RODI** credits), and access to GPT, Claude, Gemini, DeepSeek, and dozens of other models through a single OpenAI-compatible endpoint.

No foreign bank card required. Recharge with Mobile Money from the [dashboard](https://rodiumai.io/dashboard/billing).

## Step 1: Create your account

1. Go to [rodiumai.io](https://rodiumai.io) and sign up (email, Google, or GitHub).
2. Open **Dashboard → API Keys** and create a key. Copy the full secret (`rd_sk_prod_…`). It is shown only once.

## Step 2: Recharge RODI

Open **Dashboard → Billing** and top up your wallet. You need a positive balance before inference requests succeed.

Browse models and pricing on [rodiumai.io/models](https://rodiumai.io/models).

## Step 3: Send your first request

```bash
curl -s https://api.rodiumai.io/v1/chat/completions \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "openai/gpt-5.4-mini",
    "messages": [{"role": "user", "content": "Say hello in one sentence."}]
  }'
```

Replace `YOUR_API_KEY` with your real key. Pick any slug from `GET /v1/models` or the models page.

## Step 4: Track usage

Every request appears in **Dashboard → Usage**. Filter by API key or model to understand spend.

## Next steps

- Read the [API documentation](https://rodiumai.io/docs)
- Try integrations: Continue.dev, OpenCode, Cursor (see [Insights](https://rodiumai.io/insights))
- Create one API key per project for cleaner tracking

*Content_FR*

## Pourquoi RodiumAi ?

**RodiumAi** est une plateforme IA pay-as-you-go pensée pour l'Afrique. Une clé API, un portefeuille (**RODI**), et l'accès à GPT, Claude, Gemini, DeepSeek et des dizaines d'autres modèles via un seul endpoint compatible OpenAI.

Pas de carte bancaire étrangère obligatoire. Rechargez via Mobile Money depuis le [dashboard](https://rodiumai.io/dashboard/billing).

## Étape 1 : Créer votre compte

1. Allez sur [rodiumai.io](https://rodiumai.io) et inscrivez-vous (email, Google ou GitHub).
2. Ouvrez **Dashboard → API Keys** et créez une clé. Copiez le secret complet (`rd_sk_prod_…`). Il n'est affiché qu'une fois.

## Étape 2 : Recharger des RODI

Ouvrez **Dashboard → Billing** et rechargez votre portefeuille. Un solde positif est nécessaire avant toute requête d'inférence.

Consultez modèles et tarifs sur [rodiumai.io/models](https://rodiumai.io/models).

## Étape 3 : Envoyer votre première requête

```bash
curl -s https://api.rodiumai.io/v1/chat/completions \
  -H "Authorization: Bearer VOTRE_CLE" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "openai/gpt-5.4-mini",
    "messages": [{"role": "user", "content": "Dis bonjour en une phrase."}]
  }'
```

Remplacez `VOTRE_CLE` par votre vraie clé. Choisissez n'importe quel slug via `GET /v1/models` ou la page modèles.

## Étape 4 : Suivre l'usage

Chaque requête apparaît dans **Dashboard → Usage**. Filtrez par clé API ou modèle pour suivre vos dépenses.

## Prochaines étapes

- Lire la [documentation API](https://rodiumai.io/docs)
- Tester les intégrations : Continue.dev, OpenCode, Cursor (voir [Insights](https://rodiumai.io/insights))
- Créer une clé API par projet pour un suivi plus propre
