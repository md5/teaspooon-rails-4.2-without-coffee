```console
$ rails _4.2.10_ new teaspoon-rails-4-2-without-coffee --skip-spring --skip-coffee
$ cd teaspoon-rails-4-2-without-coffee
$ sed -i '' -e 'g/coffee-rails/d' Gemfile
$ echo "gem 'teaspoon', '~> 1.1', groups: [:development, :test], git: 'git@github.com:md5/teaspoon.git', branch: 'fix-precompile-paths'"
$ echo "gem 'teaspoon-jasmine', '~> 2.3', groups: [:development, :test], git: 'git@github.com:md5/teaspoon.git', branch: 'fix-precompile-paths'"
$ bundle install
$ bundle exec rails generate teaspoon:install
$ echo 'describe("Coffee failure", function() { it("fails"); })' > spec/javascripts/coffee_failure_spec.js
$ bundle exec rake teaspoon
```
