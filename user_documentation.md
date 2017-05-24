# islandora_multi_importer

## User Documentation 

### Prerequisites
In order to make this work, you will need:
* a csv file with these four fields, plus whatever other metadata you want to ingest. Recommendation: Use standard datastream field names for column titles in your csv.
  1. parent
  2. CMODEL
  3. obj_file
  4. sequence
* associated object file
* Twig template
  * [Here is information about Twig](https://twig.sensiolabs.org/)
  * [Here is an initial MODS template for Twig.](https://github.com/Islandora-Collaboration-Group/islandora_multi_importer/blob/installdoc/templates/base_mods_template.twig) Remove any unnecessary definitions.
  * Here are some sample Twig templates:

We also need to document DSID to CSV field mapping
