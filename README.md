# opensift.github.io

Documentation site for [OpenSift](https://github.com/OpenSift/OpenSift).

Built with:
- Jekyll
- Just the Docs
- Markdown-first structure
- GitHub Pages

## Local development

1. Check Ruby:

```bash
ruby -v
```

2. Install dependencies:

```bash
bundle install
```

3. Run the docs site:

```bash
bundle exec jekyll serve
```

4. Open [http://localhost:4000](http://localhost:4000).

## Deploy

Push to `main`. GitHub Pages builds from root (`/`) in this repo.

## Docs structure

```text
/
├── _config.yml
├── Gemfile
├── index.md
├── docs/
│   ├── index.md
│   ├── quickstart.md
│   ├── ui.md
│   ├── ingestion.md
│   ├── providers.md
│   ├── security.md
│   ├── troubleshooting.md
│   └── roadmap.md
└── assets/
```

## License

MIT
