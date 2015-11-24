Agenda:

=== Virtual Identity ===

* Chrome: Setting > People > Add Person...
* Create Google Account
* Change Picture > Web Camera
* Register to Gravatar, Activate account via Gmail, Add new image

=== GitHub ===

* https://github.com/join
* Create account, Activete via Gmail
* Create repository, initialise with README.md
* Create Milestone v0.0.1: Setup cloud development environment
* Customise labels, add "feature" and "documentation", remove redundant
* Create issue: v0.0.1 setup git repository, add README.md and license. 
* Add label, assign to milestone, assign to user.
* Add comment :+1:. Close issue.
* Create issue: setup web ide

=== Cloud 9 ===

* https://c9.io/
* Sign up with GitHub (few words about OAuth)
* Create new workspace
* Goto GitHub and close an issue
* Create issue: add .gitignore file
* Setup git message editor: git config --global core.editor "vim"
* Add .gitignore file and commit it with "chore(git) Close #3" message

* Goto GitHub, show message is closed. Add comment with @fediltest0
* Switch user in Chrome, goto GitHub, see message in inbox
* Goto Gmail, reply with mail :+1:
* Return to GitHub, see reply is added to chat

=== Package & Dependency Management ===

* https://www.npmjs.com/
* Goto GitHub, create an issue
> npm init
* Close issue with commit message

=== Editor Config ===

* Create issue on GitHub
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.editorconfig
* Close issue with commit message

=== Grunt ===

* Create an issue on GitHub
* http://gruntjs.com/
> npm install grunt --save-dev
* Create Gruntfile.js
* Goto load-grunt-initconfig page and follow the guide
* Create .initconfig/pkg.js
> grunt (Done, without errors)
* Close issue with commit

=== JS Static Checks ===

* Create issue
* Search for JSCS in npmjs.org
* Follow instructions
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.jscsrc
> cd .initconfig
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.initconfig/jscs.js
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.initconfig/jshint.js
> cd ..
> grunt
* Show how to fail static code checks, then fix
* Close issue with commit

=== Git Pre-Commit Hook ===

* Create issue
> npm install pre-commit --save-dev
* Change package.json test task value to "grunt"
* Close issue with commit

=== Travis CI ===

* Create issue
* https://travis-ci.org/
* Signup with GitHub
* Add repo
* Close issue with commit
* Push and see build fails
* Reopen issue, open bug
* before_install: npm install -g grunt-cli
* Commit and push, see build is green

=== Badges ===

* Create issue
* Add build and dependency badges to README.md
* Close issue with commit

=== Bower ===

* Create issue
> bower init
* Create grunt initconfig
  curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.initconfig/bower.js
  curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.initconfig/clear.js
* Create .bowerrc
  {"directory": "src/app/lib/"}
* Update .gitignore
  src/app/lib
* Update .travis.yml
  bower
* Update Gruntfile.js
  add dependencies task
> npm install grunt-bower-task --save-dev
> npm install grunt-contrib-clean --save-dev
* Close issue with commit (add [ci skip])

=== Code ===

* Create issue
> cd src
> svn export https://github.com/fediltest0/meetup/trunk/src/app
* Close issue with commit

=== Unit Tests ===

* Create issue
> npm install jasmine-core phantomjs karma karma-jasmine karma-phantomjs-launcher grunt-karma --save-dev
> cd .initconfig
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.initconfig/karma.js
> cd ..
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/karma.conf.js
* Remove coverage from karma.conf.js
* Update Gruntfile.js
> grunt karma
* Close issue with commit

=== Code Coverage ===

* Create issue
* https://coveralls.io/
* Signin with GitHub
* Add badge to README.md
> cd .initconfig
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.initconfig/coveralls.js
> cd ..
> npm install karma-coverage grunt-karma-coveralls --save-dev
* Update Gruntfile.js
> grunt test
* Close issue with commit
* Goto Coveralls to see coverage
* Goto GitHub to see coverage

=== Compilation ===

* Create issue
> cd .initconfig
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.initconfig/copy.js
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.initconfig/rename.js
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.initconfig/replace.js
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.initconfig/processhtml.js
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.initconfig/uglify.js
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.initconfig/cssmin.js
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.initconfig/htmlmin.js
> cd ..
> npm install --save-dev grunt-contrib-copy grunt-contrib-rename grunt-replace grunt-processhtml grunt-contrib-uglify grunt-contrib-cssmin grunt-contrib-htmlmin
* Update Gruntfile.js
* Close issue with commit

=== Integration Testing ===

* Create issue
* https://saucelabs.com/
* Register to trial
> cd test/app
> svn export https://github.com/fediltest0/meetup/trunk/test/app/e2e
> cd ../..
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/protractor.conf.js
> cd .initconfig
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.initconfig/protractor.js
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.initconfig/http-server.js
> cd ..
> npm install protractor grunt-protractor-runner grunt-http-server --save-dev
* Goto Travis CI > Settings
* Set SAUCE_USERNAME and SAUCE_ACCESS_KEY environment variables
* Goto Saucelabs to get access key
* Update Gruntfile.js
* Update .travis.yml
* Close issue with commit

=== Documentation ===

* Create issue
> cd src
> svn export https://github.com/fediltest0/meetup/trunk/src/docs
> cd ../.initconfig
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.initconfig/ngdocs.js
> cd ..
> npm install --save-dev grunt-ngdocs
* Update Gruntfile.js 
* Close issue with commit

=== Deployment ===

* Create issue
> cd .initconfig
> curl -O https://raw.githubusercontent.com/fediltest0/meetup/master/.initconfig/gh-pages.js
> cd ..
> npm install --save-dev grunt-gh-pages
* Edit Gruntfile.js (add deploy task)
* Edit gh-pages.js (update repository)
* Generate personal access token on GitHub
* Add GH_TOKEN environment variable on Travis CI
* Close issue with commit

=== Collaboration & Code Review ===

* Create issue
* https://www.review.ninja/
* Signin > add one of your own repositories
* Close issue with commit
* Fork repository with other user
	> curl -O https://raw.githubusercontent.com/fediltest1/meetup/master/.initconfig/conventionalChangelog.js
	> npm install grunt-conventional-changelog --save-dev
	* Update Gruntfile.js
* Create pull request
* See status in GitHub
* See pull request in Review Ninja
* Add ReviewNinjs badge to README.md
* Review PR, merge, delete brunch

=== Create Release ===

* Create relase on GitHub
* Add changelog content as description
