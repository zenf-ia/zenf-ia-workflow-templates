# ZENF IA - Workflow Templates

Templates de workflows d'automatisation IA pour TPE/PME, prets a deployer avec **n8n** et **Make**.

> Par [ZENF IA](https://zenf-ia.com) - Agence IA sur mesure, Paris

## Contenu

### n8n Templates

| Template | Description | Secteur |
|----------|-------------|---------|
| `n8n/rappel-rdv-whatsapp.json` | Rappel automatique de RDV via WhatsApp 24h avant | Sante, Services |
| `n8n/qualification-leads.json` | Qualification automatique des demandes entrantes | Tous secteurs |
| `n8n/suivi-client-email.json` | Suivi client automatise avec relances par email | Commerce, Services |
| `n8n/envoi-devis-auto.json` | Generation et envoi automatique de devis | TPE/PME |

### Make (Integromat) Templates

| Template | Description | Secteur |
|----------|-------------|---------|
| `make/sync-google-calendar-notion.json` | Synchronisation agenda Google <> Notion | Tous secteurs |
| `make/reponse-auto-messenger.json` | Reponse automatique aux messages Messenger | Commerce |
| `make/collecte-avis-clients.json` | Collecte automatique d'avis clients apres prestation | Services |

## Comment utiliser ces templates

### Pour n8n
1. Ouvrez votre instance n8n
2. Allez dans **Workflows** > **Import from File**
3. Selectionnez le fichier `.json` souhaite
4. Configurez vos credentials (cles API, tokens)
5. Activez le workflow

### Pour Make
1. Connectez-vous a Make.com
2. Creez un nouveau scenario
3. Importez le fichier `.json` via **Import Blueprint**
4. Connectez vos applications
5. Activez le scenario

## Variables a configurer

Chaque template necessite la configuration de vos propres credentials :

```
WHATSAPP_API_TOKEN=votre_token
OPENAI_API_KEY=votre_cle
GOOGLE_CALENDAR_ID=votre_calendar
NOTION_API_KEY=votre_cle_notion
SMTP_HOST=votre_smtp
```

> **Important** : Ne commitez jamais vos cles API. Utilisez des variables d'environnement.

## Architecture type d'un workflow ZENF IA

```
[Declencheur]        [Traitement IA]         [Action]
     |                     |                     |
 Webhook/Cron  -->  GPT-4o Analysis  -->  WhatsApp/Email
 Form Submit   -->  Classification   -->  CRM Update
 Message recu  -->  Extraction data  -->  Google Sheets
```

## Conformite RGPD

Tous nos templates sont concus pour respecter le RGPD :
- Aucune donnee personnelle stockee dans les workflows
- Les donnees transitent uniquement via des services heberges en UE
- Chaque template inclut un noeud de consentement si necessaire

## Besoin d'aide ?

Ces templates sont des points de depart. Pour un deploiement complet et personnalise :

- [Reserver un audit IA gratuit (30 min)](https://zcal.co/zenf-ia/60min)
- Email : contact@zenf-ia.com
- Tel : 06 59 25 79 09

## Licence

MIT License - Libre d'utilisation et de modification.

---

*Cree par [ZENF IA](https://zenf-ia.com) - Agence IA sur mesure pour TPE/PME, Paris*
