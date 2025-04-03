source "https://rubygems.org"

gem "minima", "~> 2.5"
gem "webrick"

# If you want to use GitHub Pages, remove the "gem "jekyll"" above and
# uncomment the line below. To upgrade, run `bundle update github-pages`.
# gem "jekyll", "~> 4.3.4"
gem "github-pages", group: :jekyll_plugins
gem "jekyll-include-cache", group: :jekyll_plugins

# If you have any plugins, put them here!
group :jekyll_plugins do
    gem 'jekyll'
    gem 'jekyll-feed'
    gem 'jekyll-sitemap'
    gem 'jekyll-redirect-from'
    gem 'jemoji'
    # gem 'webrick', '~> 1.8'
  end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]