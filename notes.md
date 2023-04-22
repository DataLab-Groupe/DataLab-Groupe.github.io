# install new env
gem install bundler jekyll
bundle update
bundle exec jekyll serve

# build locally with internal links
JEKYLL_ENV=production bundle exec jekyll serve

