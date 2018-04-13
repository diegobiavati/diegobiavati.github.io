## 1. Melhores Gems ##
* [Github Changelog Generator](https://github.com/skywinder/github-changelog-generator) - *Automatically generate change log from your tags, issues, labels and pull requests on GitHub.*

## 2. Fontes de Gems ##
* [hothero/awesome-rails-gem](https://github.com/hothero/awesome-rails-gem) - *A collection of awesome Ruby Gems for Rails development.*

{% for repository in site.github.public_repositories %}
  * [{{ repository.name }}]({{ repository.html_url }})
{% endfor %}
