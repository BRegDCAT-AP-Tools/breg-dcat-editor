# DCAT Application profile for base registries in Europe (BRegDCAT-AP)	Catalog Description Editor

The BRegDCAT-AP Description Editor is a web form where public administrations can create and manage BRegDCAT-AP 2.0.1 descriptions of BRegDCAT-APs in a way that is technically robust, cost-efficient and collaborative in terms of end-user benefits. The tool also allows public administrations to visualise the descriptions in a human-readable way and to export them in an interoperable, machine-readable format conformant to the BRegDCAT-AP 2.0.1.


## Deployment

### Docker

This application has configured to launch a [docker](https://www.docker.com/) cointainer ready to use. This requires that you have [docker](https://www.docker.com/) and [docker-compose](https://docs.docker.com/compose/install/). To run:

    $ cd path_to_editor
    $ docker-compose up --build
    
The application can be accessed on http://localhost:40080/

### Local deployment 

This application is based on [drupal](https://www.drupal.com). This projects contains an installation and an initial database (dcat-editor-database.sql). Follow the Drupal's [documentation](http://drupal.org/documentation) to configure an Drupal project.

To deploy the Public Service Description Editor locally, the administration will require PHP and Drupal environments installed on their webserver. The PHP version used is 5.6.15; the Drupal version is 7.42. Finally, a Virtuoso Triple store is needed to store the data created by the users.