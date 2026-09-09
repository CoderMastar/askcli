# askcli

Minimal LLM CLI: stdin in, streamed answer out

Side project, maintained when I have time.

## Getting started

```bash
pip install -r requirements.txt
export OPENAI_API_KEY=sk-...
```

## How to use

```bash
chatsh explain this error < error.log
cat diff.patch | chatsh review this diff
```

## What it does

- Streams tokens as they arrive
- Reads the prompt from args or stdin
- Works with any OpenAI-compatible endpoint
- Model and system prompt via flags or env

## Project structure

```text
├── .github/
│   ├── workflows/
│   │   └── ci.yml
│   └── dependabot.yml
├── docs/
│   ├── configuration.md
│   ├── faq.md
│   ├── roadmap.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── tests/
│   └── test_smoke.py
├── .gitignore
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
├── chatsh.py
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```

## License

MIT licensed, see LICENSE.
