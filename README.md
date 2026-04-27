# Amazon Review Insights

AI-powered Amazon review analysis tool for AI agents. Recommended for use on OpenClaw.

## Features

- **Review Fetching** - Collect Amazon product reviews across 8 marketplace sites (US, CA, UK, DE, FR, IT, ES, JP)
- **AI-Powered Analysis** - Intelligent negative review detection and categorization
- **Issue Quantification** - Identify and quantify high-frequency problems
- **Hidden Feedback Discovery** - Uncover negative sentiments hidden in 5-star reviews
- **Trend Tracking** - Monitor review patterns over time
- **Incremental Updates** - Fetch latest reviews without duplicating existing data

## Installation

```bash
pip install -r requirements.txt
```

## Configuration

Set your API key via environment variable:

```bash
export CUSTOMER_INSIGHTS_API_KEY="your-api-key"
```

> Get your API key at [astrmap.com](https://www.astrmap.com/) - User Menu → API Keys

## Usage

```bash
# Check device status
python scripts/api_client.py --action check_device

# Create analysis task
python scripts/api_client.py --action create_task --asin "B09V3KXJPB" --site US

# Query results
python scripts/api_client.py --action get_ai_insights --task-id "TSK_xxx"
```

For detailed documentation, see [SKILL.md](SKILL.md).

## Supported Marketplaces

| Site | Language |
|------|----------|
| US | English |
| CA | English |
| UK | English |
| DE | German |
| FR | French |
| IT | Italian |
| ES | Spanish |
| JP | Japanese |

## License

MIT