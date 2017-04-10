
# Travis-ci

## install travis cli on mac

* see [travis.rb](https://github.com/travis-ci/travis.rb#installation)

    brew install ruby
    gem update --system
    gem install travis -v 1.8.8 --no-rdoc --no-ri
    travis version

## Deploying to Maven Repositories from Tavis CI

* see: [Deploying to Maven Repositories from Tavis CI](https://vzurczak.wordpress.com/2014/09/23/deploying-to-maven-repositories-from-tavis-ci/)

## Publishing a Maven Site to GitHub Pages with Travis-CI

* see: [Publishing a Maven Site to GitHub Pages with Travis-CI](https://blog.lanyonm.org/articles/2015/12/19/publish-maven-site-github-pages-travis-ci.html)


    travis encrypt GITHUB_GIT_SERVICE_TOKEN="${GITHUB_GIT_SERVICE_TOKEN}" --add env.global

## Environment variables

see: [Environment variables](https://docs.travis-ci.com/user/environment-variables/)

## Note

    env:
      global:
      # adapt with gitlab-ci
      - CI_BUILD_REF_NAME=$TRAVIS_BRANCH
      # or delete /etc/mavenrc
      - MAVEN_SKIP_RC=true
