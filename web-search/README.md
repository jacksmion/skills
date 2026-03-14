# Web Search Skill

A Claude Code skill for performing web searches using Baidu search engine via the `baidusearch` Python library.

## Overview

This skill enables Claude Code to search the web and retrieve current information from the internet. It's particularly useful for:
- Finding up-to-date information not in training data
- Researching current events
- Looking up technical documentation
- Gathering real-time data

## Installation

1. Install the required dependency:

```bash
pip install baidusearch
```

2. Ensure the skill file is in your Claude Code skills directory.

## Usage

Once installed as a skill, Claude Code will automatically use it when you ask to:
- "Search the web for..."
- "Look up information about..."
- "Find current data on..."
- "Research..."

### Manual Usage

You can also run the search script directly:

```bash
python scripts/search.py "your search query"
```

## Example Usage

```
User: Search for the latest Python 3.13 features
Claude: [Uses web-search skill to find current information]
```

## Output Format

Search results are returned as structured JSON containing:

| Field    | Description                           |
|----------|---------------------------------------|
| title    | The page title                        |
| url      | The page URL                          |
| abstract | Brief description/summary             |
| rank     | Search result ranking position        |

## Requirements

- Python 3.6+
- baidusearch library

## Notes

- Uses Baidu search engine (works well for both Chinese and English queries)
- Based on web scraping - may be affected by site structure changes
- Returns organic search results only

## License

MIT
