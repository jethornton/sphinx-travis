======
GitHub
======

In the upper-right corner of any page, click your profile photo, then click
Settings >  Developer settings > Personal access tokens.

Generate new token with the name ``GH_TOKEN`` and give it pull push permissions
by clicking on repo.

Generate and copy the token key.

Create a gh-pages branch

For each repository click on Settings and in GitHub Pages set the source to
gh-pages branch.

In the base directory create a `.travis.yml` file with the following contents.
Don't forget the leading dot on the file name!
::

	language: python

	install:
	- pip install sphinx sphinx_rtd_theme mock

	script:
	- sphinx-build -Wv docs/source docs/html

	deploy:
	# publish docs on push
	- provider: pages
		skip_cleanup: true
		keep-history: false
		github_token: $GH_TOKEN
		local_dir: docs/html
		on:
			branch: master

Make sure your default branch is named master.
