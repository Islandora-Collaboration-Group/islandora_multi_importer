Islandora Multi-importer Installation Documentation

Table of Contents

Summary
Assumptions
Prerequisites
Environment
Dependencies
Installation
Configuration
Summary

The Islandora Multi-importer offer highly configurable batch import functionality through the Drupal GUI.

Assumptions

Prerequisites

Environment

Dependencies

To install Composer, follow this link: Composer

Then:

sudo mv composer.phar /usr/local/bin/composer

To test if Composer is installed:

which composer returns /usr/local/bin/composer

composer --version returns Composer version 1.4.2 2017-05-17 08:17:52 (example)

To test if you have Drush installed, command is

which drush

To see which version of Drush is installed, command is

drush st

If using the Islandora Vagrant, Drush is already installed

If Drush is not installed please use Composer to install composer global require drush/drush:7.* (installs newest version of Drush 7.x)

Installation

Install as usual, see this for further information.



### DCMNY admin documentation 

[Multi-Importer Admin Instructions for DCMNY Administrators] (https://docs.google.com/document/d/18oB6sX-8s6sIScgUf7RbkFFlJ52Y9k_f9FcsaWvDJ7s/edit?usp=sharing)

[Sample CSV (configured for multi-importer ingest)] (https://drive.google.com/file/d/0BzuVASmQStk8dWJ6UGt6bmphcGs/view?usp=sharing)

[DCMNY Metadata Spreadsheet (for use with multi-importer ingest)] (https://docs.google.com/spreadsheets/d/1fL9oO_x35tUx3wKSZ4a848ravc4Oh1Wjk5ykU3H1Ti8/edit?usp=sharing)

### Twig

[Sample Twig Templates (for use with multi-importer ingest)] (https://github.com/mnylc/dcmny/tree/master/twig)

[Twig Documentation] (http://twig.sensiolabs.org/documentation)


