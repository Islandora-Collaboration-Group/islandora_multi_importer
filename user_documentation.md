# islandora_multi_importer

## User Documentation 

### Prerequisites
In order to make this work, you will need:
* a csv file
* associated object file
* Twig template
  
  
####csv file
The csv file must have these four fields, plus whatever other metadata you want to ingest. Recommendation: Use standard datastream field names for column titles in your csv.
  1. parent: parent of object
  2. CMODEL: Content model of associated object
  3. obj_file: File name of object associated with record to be ingested
  4. sequence:ingest sequence for object

####object file
If the object file is a zip file, it must be at the top level of the archive.

####Twig template
  * [Here is information about Twig](https://twig.sensiolabs.org/)
  * [Here is an initial MODS template for Twig.](https://github.com/Islandora-Collaboration-Group/islandora_multi_importer/blob/installdoc/templates/base_mods_template.twig) Remove any unnecessary definitions.
  * Here are some sample Twig templates:
  
  
###  
  
  

We also need to document DSID to CSV field mapping
