# llm-presentation-automation

> Automated slide deck generation from raw documents using LLM-powered content extraction.

Turn long PDFs, meeting notes, or technical specs into polished presentation decks in seconds. Built as part of an internal tooling initiative to accelerate technical pre-sales and reporting.

## Features

- Multi-format input: PDF, DOCX, Markdown, raw text
- LLM-driven outline & key-point extraction 
- Structured slide generation (PPTX / Google Slides / Reveal.js)
- Custom templates and branding
- CLI + FastAPI service modes
- Configurable LLM backend (Mistral, Claude, local Ollama)

## Stack

- **Python 3.11**, Pydantic, FastAPI
- **LLM:** Mistral API / Claude / Ollama
- **Output:** python-pptx, Google Slides API
- **Parsing:** unstructured, PyMuPDF

## Quick Start

```bash
pip install -r requirements.txt
python -m presentation_gen --input docs/report.pdf --output deck.pptx
```

## API Mode

```bash
uvicorn app.main:app --reload
# POST /generate with multipart upload
```

## Roadmap

- [ ] Image generation for slides
- [ ] Speaker notes generation
- [ ] Multi-language support
- [ ] Live preview UI (React)

## License

MIT
