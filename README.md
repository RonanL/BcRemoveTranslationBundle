BC Remove Translation
===============

This bundle implements a solution to provide eZ Publish Platform / eZ Platform / Symfony commands to remove content location translations.


Version
=======

* The current version of BC Remove Translation is 0.1.1

* Last Major update: March 07, 2017


Copyright
=========

* BC Remove Translation is copyright 1999 - 2017 Brookins Consulting

* See: [COPYRIGHT.md](COPYRIGHT.md) for more information on the terms of the copyright and license


License
=======

BC Remove Translation is licensed under the GNU General Public License.

The complete license agreement is included in the [LICENSE](LICENSE.md) file.

BC Remove Translation is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 2 of the License or at your
option a later version.

BC Remove Translation is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

The GNU GPL gives you the right to use, modify and redistribute
BC Remove Translation under certain conditions. The GNU GPL license
is distributed with the software, see the file [LICENSE](LICENSE.md).

It is also available at [http://www.gnu.org/licenses/gpl.txt](http://www.gnu.org/licenses/gpl.txt)

You should have received a copy of the GNU General Public License
along with BC Remove Translation in in the [LICENSE](LICENSE.md) file.

If not, see [http://www.gnu.org/licenses/](http://www.gnu.org/licenses/).

Using BC Remove Translation under the terms of the GNU GPL is free (as in freedom).

For more information or questions please contact: license@brookinsconsulting.com


Requirements
============

The following requirements exists for using BC Remove Translation bundle:


### eZ Publish version

* Make sure you use eZ Publish version 5.x (required) or higher.

* Designed and tested with eZ Publish Community Project 2013.11


### PHP version

* Make sure you have PHP 5.x or higher.


Features
========

### Commands

This solution provides the following symfony commands

* Command: `bc:rt:remove-translation`

### Dependencies

* This solution depends on eZ Platform
* This solution depends on symfony/symfony

These dependencies are documented in greater detail within the bundle's composer.json file


Use case
========

This solution was created to provide content location translation removal.


Installation
============

### Bundle Installation via Composer

Run the following command from your project root to install the bundle:

    bash$ composer require brookinsconsulting/bcremovetranslationbundle dev-master;


### Bundle Activation

Within file `app/AppKernel.php` method `registerBundles` add the following into the `$bundles = array(` variable definition.

    // Brookins Consulting : BcGitHubStarsBundle Requirements
    new BrookinsConsulting\BcRemoveTranslationBundle\BcRemoveTranslationBundle(),


### Clear the caches

Clear Symfony caches (Required).

    php bin/console cache:clear;


Usage
=====

The solution is configured to work virtually by default once properly installed.

### Running the command

To remove content location translation run the following command and you will be prompted for required arguments

    php -d memory_limit=-1 bin/console bc:rt:remove-translation;

#### Running the remove-translation command with locationId shell arguments

For repeated usage of the same input you can run the script more quickly using shell arguments. Simply run

    php -d memory_limit=-1 bin/console bc:rt:remove-translation -v --locationId=2 --removeLanguage=eng-US;

Notice: That the command supports translation removal by locationId or contentId

#### Running the remove-translation command with contentId shell arguments

For repeated usage of the same input you can run the script more quickly using shell arguments. Simply run

    php -d memory_limit=-1 bin/console bc:rt:remove-translation -v --contentId=42 --removeLanguage=eng-US;


Testing
=====

The solution is configured to work once properly installed and configured.

Note: At the time of writing xss testing has not been implemented nor proper unit testing.


Troubleshooting
===============

### Read the FAQ

Some problems are more common than others. The most common ones are listed in the the [Resources/doc/FAQ.md](Resources/doc/FAQ.md)


### Support

If you have find any problems not handled by this document or the FAQ you can contact Brookins Consulting through the support system: [http://brookinsconsulting.com/contact](http://brookinsconsulting.com/contact)
