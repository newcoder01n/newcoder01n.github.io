source "https://rubygems.org"

# GitHub Pages 官方依赖包（包含兼容版本的 Jekyll 及内置插件）
# 用 github-pages 而非直接指定 jekyll，可保证本地构建与 GitHub Pages 线上环境一致
gem "github-pages", group: :jekyll_plugins

# _config.yml 中用到的插件
group :jekyll_plugins do
  gem "jekyll-relative-links"
end

# Ruby 3.4 起 csv 不再是默认 gem，显式声明以消除警告
gem "csv"
# 消除 Faraday v2 retry 中间件警告
gem "faraday-retry"

# Windows / JRuby 下的时区数据依赖
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# 注：wdm（Windows 文件监听加速）在新版 Ruby 上编译困难，且仅 `jekyll serve`
# 的自动刷新需要、`jekyll build` 不需要，故不引入。serve 时会自动回退为轮询模式。
