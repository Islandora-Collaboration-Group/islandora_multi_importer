# Islandora Multi-importer Installation Documentation

## Table of Contents

- [Summary](#summary)
- [Assumptions](#assumptions)
- [Prerequisites](#prerequisites)
  - [Environment](#environment)
  - [Dependencies](#dependencies)
- [Installation](#installation)
- [Configuration](#configuration)

## Summary
A comprehensive installation document for how to install Islandora Multi-importer.

## Assumptions
* For HackDoc: Using the Islandora Labs Vagrant!

## Prerequisites

### Environment

  * Follow instructions at [Islandora-Labs Vagrant Virtual Machine](https://github.com/Islandora-Labs/islandora_vagrant)
    * Edit ports if needed within the Vagrantfile
    * access via http://localhost:8000/
    * take a snapshot in case of need

### Dependencies

* **ssh in

  * **[Composer](https://getcomposer.org/download/)**

    * To install Composer:

      1. `php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"`

      2. `php -r "if (hash_file('SHA384', 'composer-setup.php') === '669656bab3166a7aff8a7506b8cb2d1c292f042046c5a994c43155c0be6190fa0355160742ab2e1c88d40d5be660b410') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"`

      3. `php composer-setup.php`

      4. `php -r "unlink('composer-setup.php');"`

      5. `sudo mv composer.phar /usr/local/bin/composer`

      6. To test if Composer is installed:
        * `which composer` returns `/usr/local/bin/composer`

        * `composer --version` returns `Composer version 1.4.2 2017-05-17 08:17:52` (*example*)

  * **Drush**
    * If using the Islandora Vagrant this tool is already installed

    * If Drush is not installed please use Composer to install
    `composer global require drush/drush:7.*` (*installs newest version of Drush 7.x*)

  * **Additional tools?**

## Installation

1. Access the Islandora environment via ssh

2. Navigate to the modules directory
   `cd /var/www/drupal/sites/all/modules`
3. Clone the IMI Github fork
   `git clone https://github.com/Islandora-Collaboration-Group/islandora_multi_importer.git` (use https instead of ssh)

4. Navigate to the newly cloned directory
`cd /var/www/drupal/sites/all/modules/islandora_multi_importer/`

5. Run Composer command
`composer install`

6. Enable the module
`drush en -u 1 -y islandora_multi_importer`

7. Navigate to section URL needed from Drupal site
http://localhost:8000/multi_importer

## Configuration
