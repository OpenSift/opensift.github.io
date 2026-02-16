source "https://rubygems.org"

# Ruby 3.4+ no longer includes csv as a default gem, but Jekyll expects it.
gem "csv"
gem "bigdecimal"
# Fix: Liquid 4.0.3 calls `tainted?` which breaks on modern Ruby. Pin to 4.0.4+.
gem "liquid", ">= 4.0.4"

# GitHub Pages pins Jekyll + dependencies to known-good versions
gem "github-pages", group: :jekyll_plugins

# Optional: removes "To use retry middleware with Faraday v2.0+, install `faraday-retry`"
gem "faraday-retry"

group :jekyll_plugins do
  # Required for remote_theme
  gem "jekyll-remote-theme"

  # Nice-to-have plugins (GitHub Pages supports these)
  gem "jekyll-sitemap"
  gem "jekyll-seo-tag"
end

# Windows users may need this (safe to keep even on macOS/Linux)
gem "wdm", ">= 0.1.1", "< 0.2.0" if Gem.win_platform?