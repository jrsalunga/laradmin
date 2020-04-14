laravel-bootstrap-adminlte-starter-kit 
=============
[![build status](https://github.com/jrsalunga/laradmin/badges/master/build.svg)](https://github.com/jrsalunga/laradmin/commits/master)


Template for websites with basic functionality. It is based on next ideas:

- have common features already integrated and configured (tests,laravel-mix/webpack/babel,bower etc)
- simplify updates (via git merge from this project)
- extensive use of .env config (slightly more then original Laravel) 
- 'make' based macro-tool for often used commands 



Introduction
============

Just base functionality for other projects

Project includes already preconfigured resources:

- [Laravel 5.4](http://laravel.com/)  
- [AdminLte template](https://almsaeedstudio.com/) [Laravel Integration](https://github.com/acacha/adminlte-laravel) 
- [jrean/laravel-user-verification](https://github.com/jrean/laravel-user-verification)
- [oprudkyi/laravel-mail-logger](https://github.com/oprudkyi/laravel-mail-logger)
- Front-End:
	- [Bower](https://bower.io/)
	- [Bootstrap](http://getbootstrap.com/)
	- [Font Awesome](http://fontawesome.io/)
	- [jQuery](https://jquery.com/)
	- [DataTables](https://datatables.net/)
	- [Moment.js](http://momentjs.com/)
	- [Bootstrap 3 Date/Time Picker](https://github.com/Eonasdan/bootstrap-datetimepicker)
	- [js-error-alert](https://github.com/oprudkyi/js-error-alert)

- Testing (preconfigured for unit,functional and acceptance tests):
	- [Codeception](http://codeception.com/) - BDD-styled PHP testing framework atop of [PHPUnit](https://phpunit.de/)
	- [Codeception/PhpBuiltinServer](https://github.com/tiger-seo/PhpBuiltinServer) - Codeception extension to start and stop PHP built-in web server for your tests.
	- [Phantoman](https://github.com/grantlucas/phantoman) - The Codeception extension for automatically starting and stopping PhantomJS when running tests.
	- [codeception-events-scripting](https://github.com/oprudkyi/codeception-events-scripting) - The Codeception extension for automatically running shell scripts on Codeception events.
	- [MailCatcher](https://mailcatcher.me/) - catches mails and provides API for testing
	- [Codeception MailCatcher Module](https://github.com/captbaritone/codeception-mailcatcher-module)
	- [PhantomJS](http://phantomjs.org/) - a headless WebKit, used for acceptance testing
	- [Setup Test DB Command for Laravel](https://github.com/SocialEngine/setup-test-db)


Creation of new site based on starter kit
============

```sh
#clone original repository
git clone git@github.com:jrsalunga/laradmin.git my_project

#cd to project
cd my_project

#delete origin
git remote rm origin

#use your new repository as main source 
git remote add origin git@github.com:jrsalunga/laradmin.git

#keep original source for updates
git remote add starter-kit git@github.com:jrsalunga/laradmin.git

#push to your repository
git push -u origin master
```

Keeping your site in sync with starter kit
============

```sh
git fetch starter-kit
git merge starter-kit/master
git push
```

or 
```sh
make merge-starterkit
git push
```


Installation
============

If you are building from the first time out of the source repository, you will
need to generate the configure scripts. From the top directory, do:

    ./bootstrap.sh

Once the configure scripts are generated, 'make' system can be configured.
From the top directory, do:

    ./configure


Run ./configure --help to see other configuration options

Install configured dependencies - tools like composer/bower and components as defined in composer.json, bower.json, package.json :

	make install-dependencies

For automicity and performance of CI the repositories of composer/bower/npm are stored under .install-cache directory (pointed out via rc files)


