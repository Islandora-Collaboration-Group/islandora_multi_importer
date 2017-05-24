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
A comprehensive installation document for how to install and run Islandora Multi-importer..

## Assumptions
* For HackDoc: Using the Islandora Labs Vagrant!

## Prerequisites

### Environment

  * Follow instructions at [Islandora-Labs Vagrant Virtual Machine](https://github.com/Islandora-Labs/islandora_vagrant)
    * Edit ports if needed within the Vagrantfile
    * access via http://localhost:8000/
    * take a snapshot in case of need
    * ssh


### Dependencies


  * **To install Composer, follow this link: [Composer](https://getcomposer.org/download/)**
  
    Then:

      1. `sudo mv composer.phar /usr/local/bin/composer`

      2. To test if Composer is installed:
        * `which composer` returns `/usr/local/bin/composer`

        * `composer --version` returns `Composer version 1.4.2 2017-05-17 08:17:52` (*example*)

  * **To test if you have Drush installed, command is**
  
    which drush
  
  * **To see which version of Drush is installed, command is**
  
    drush st
  
  
    * If using the Islandora Vagrant, Drush is already installed

    * If Drush is not installed please use Composer to install
    `composer global require drush/drush:7.*` (*installs newest version of Drush 7.x*)


Various parts will install. If they install correctly, you will see (100%) at the end of each line. Composer might suggest installing several other tools, but don't.


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

## Using the IMI



### Prerequisites

  **In order to make this work, you will need**:
  
  
  * a csv file with these four fields:
    1. parent
    2. CMODEL
    3. obj_file
    4. sequence
    * Recommendation: Use standard datastream field names for column titles in your csv
  * associated object file
  * Twig template
    * [Here is information about Twig](https://twig.sensiolabs.org/)
    * [Here is an initial MODS template for Twig](/templates/base_mods_template.twig). Remove any unnecessary definitions.
    * Here are some sample Twig templates:
    * http://YourURL/multi-importer is where we get the IMI module
  

Wednesday:
look through Pat's Google doc: https://docs.google.com/a/commonmediainc.com/document/d/1RKDeW2tZWPULMg7IM0x5ZioBQsa1wjA6VveQAx3YZ-s/edit?usp=sharing

Document DSID to CSV field mapping

Jessika will bring updated short csv file.

