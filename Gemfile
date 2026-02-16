source "https://rubygems.org"

# GitHub Pages pins Jekyll + dependencies to known-good versions
gem "github-pages", group: :jekyll_plugins

# Just the Docs theme
gem "just-the-docs"

group :jekyll_plugins do
  # Automatically generates a sitemap.xml
  gem "jekyll-sitemap"

  # Adds SEO tags (optional, but nice for a public docs site)
  gem "jekyll-seo-tag"
end

# Windows users may need this (safe to keep even on macOS/Linux)
gem "wdm", ">= 0.1.1", "< 0.2.0" if Gem.win_platform?