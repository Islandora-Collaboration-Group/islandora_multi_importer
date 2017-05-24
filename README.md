# Islandora Multi-importer Installation Documentation

## Table of Contents

- [Summary](#summary)
- [Requirements](#requirements)
- [Prerequisites](#prerequisites)
  - [Environment](#environment)
  - [Dependencies](#dependencies)
- [Installation](#installation)
- [Configuration](#configuration)

## Summary
The Islandora Multi-importer offer highly configurable batch import with .csv files through the Drupal GUI. The IMI relies on Twig templates in order to transform the data in your .csv to MODS. Associated object files can be ingested via zip files, http/s addresses, or your public/tmp folders on your Drupal server.

## Requirements

* Islandora
* Drush
* Composer

For more information on building Twig templates see the [Twig Documentation](http://twig.sensiolabs.org/documentation)

Here is an initial MODS template for Twig. Remove any unnecessary definitions.

### Dependencies

  * **To install Composer, follow the instructions at this link: [Composer](https://getcomposer.org/download/)**
  
    Then:

      1. `sudo mv composer.phar /usr/local/bin/composer`

      2. To test if Composer is installed:
        * `which composer` returns `/usr/local/bin/composer`

        * `composer --version` returns `Composer version 1.4.2 2017-05-17 08:17:52` (*example*)

## Installation

Install as usual, see [this](https://www.drupal.org/docs/7/extending-drupal-7/installing-contributed-modules) for further information.

Once you've cloned this repo, you will need to navigate to the newly cloned directory 
and run:

        * composer install

### DCMNY admin documentation 

[Multi-Importer Admin Instructions for DCMNY Administrators](https://docs.google.com/document/d/18oB6sX-8s6sIScgUf7RbkFFlJ52Y9k_f9FcsaWvDJ7s/edit?usp=sharing)

[Sample CSV (configured for multi-importer ingest)](https://drive.google.com/file/d/0BzuVASmQStk8dWJ6UGt6bmphcGs/view?usp=sharing)

[DCMNY Metadata Spreadsheet (for use with multi-importer ingest)] (https://docs.google.com/spreadsheets/d/1fL9oO_x35tUx3wKSZ4a848ravc4Oh1Wjk5ykU3H1Ti8/edit?usp=sharing)

### Twig

[Sample Twig Templates (for use with multi-importer ingest)](https://github.com/mnylc/dcmny/tree/master/twig)

[Twig Documentation](http://twig.sensiolabs.org/documentation)


