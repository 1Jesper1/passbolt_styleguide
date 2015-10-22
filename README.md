	      ____                  __          ____
	     / __ \____  _____ ____/ /_  ____  / / /_
	    / /_/ / __ `/ ___/ ___/ __ \/ __ \/ / __/
	   / ____/ /_/ (__  |__  ) /_/ / /_/ / / /_
	  /_/    \__,_/____/____/_.___/\____/_/\__/

	The password management solution
	(c) 2012-2015 passbolt.com

Install
=========

Install grunt
```
	npm install -g grunt-cli
```

Install the needed modules defined in the grunt config
```
	npm install
```

Make sure Grunt watch for less changes and compile them into CSS
```
	grunt watch
```

Edit one LESS file to see if it works!


How to update the styleguide?
=========

We are using npm to manage the styleguide package in project using it.
Checkout npm documentation: https://docs.npmjs.com/developers

In a nutshell, once you are done changing, make sure you change the version
number in the package.json.

	{
	  "name": "passbolt-styleguide",
	  "version": "X.X.X",
	  [...]
	}

You need to commit your changes and tag the new version of the styleguide.
This is how npm knows a new version is available in the project using the package.

  git commit -am 'X.X.X'
  git tag -a X.X.X -m 'X.X.X'
  git push origin X.X.X
  git push
  
Then we publish it again with

  npm publish

in your project using the bower package you can then run:

  npm update

You should also have a grunt task to manage the copy/pasting in the right place such as

  grunt styleguide-deploy

