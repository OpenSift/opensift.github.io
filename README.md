# opensift.github.io
OpenSift Official Website

# OpenSift Docs

Documentation site for **OpenSift — a local-first AI study assistant**.

Built with:
- Jekyll
- Just the Docs
- Markdown-first structure
- Hosted on GitHub Pages

---

# 🚀 Local Development

## 1️⃣ Install Ruby (if needed)

Check:

```bash
ruby -v

If not installed:
	•	macOS: brew install ruby
	•	Ubuntu: sudo apt install ruby-full
	•	Windows: RubyInstaller

2️⃣ Install dependencies

From the repo root:

```
bundle install
```

3️⃣ Run locally

```
bundle exec jekyll serve
```

Then open:
```
http://localhost:4000/
```

The site will rebuild automatically when you edit Markdown files.


🌐 Deploy to GitHub Pages
	1.	Push to main
	2.	Go to:
	•	Settings → Pages
	3.	Select:
	•	Deploy from branch
	•	Branch: main
	•	Folder: / (root)

GitHub will automatically build and deploy.

📂 Structure

```text
/
├── _config.yml
├── Gemfile
├── index.md
├── docs/
│   ├── quickstart.md
│   ├── security.md
│   ├── ui.md
│   ├── providers.md
│   ├── ingestion.md
│   ├── troubleshooting.md
│   └── roadmap.md
└── assets/
```

🧠 Philosophy

OpenSift is:
	•	Local-first
	•	Security-conscious
	•	Designed for students overwhelmed by information
	•	Built around retrieval-grounded AI workflows

⸻

🛠 Contributing
	1.	Create a branch
	2.	Edit Markdown files
	3.	Submit a PR

⸻

📜 License

MIT

---