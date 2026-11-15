# frozen_string_literal: true

source "https://rubygems.org"

# The site is built by GitHub Actions (.github/workflows/jekyll.yml), not by the
# legacy GitHub Pages builder, so we use plain Jekyll 4 and only the plugins we
# actually need. Keep this list minimal: every gem here is attack surface that
# Dependabot will report on.
gem "jekyll", "~> 4.4"

group :jekyll_plugins do
  gem "jekyll-seo-tag", "~> 2.8"
  gem "jekyll-sitemap", "~> 1.4"
end

# Needed for `jekyll serve` on Ruby >= 3.0 (local preview only).
gem "webrick", "~> 1.9"
