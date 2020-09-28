# DCAT Application profile for base registries in Europe (BRegDCAT-AP)	Catalog Description Editor

The DCAT Description Editor is a web form where public administrations can create and manage BRegDCAT-AP 2.0.1 descriptions of BRegDCAT-APs in a way that is technically robust, cost-efficient and collaborative in terms of end-user benefits. The tool also allows public administrations to visualise the descriptions in a human-readable way and to export them in an interoperable, machine-readable format conformant to the BRegDCAT-AP 2.0.1.


## Deployment

### Docker

This application has configured to launch a [docker](https://www.docker.com/) cointainer ready to use. This requires that you have [docker](https://www.docker.com/) and [docker-compose](https://docs.docker.com/compose/install/). To run:

    $ cd path_to_editor
    $ docker-compose up --build
    

### Local deployment 

This application is based on [drupal](https://www.drupal.com). This projects contains an installation and an initial database (dcat-editor-database.sql). Follow the [official documentation[(http://drupal.org/documentation)] to congfigure an Drupal projec 
