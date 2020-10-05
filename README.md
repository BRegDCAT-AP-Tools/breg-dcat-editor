# BREG-DCAT Editor

This repository contains the BRegDCAT-AP v2 _Editor_ proof-of-concept implementation. It allows public administrations to:

* Create and edit BRegDCAT-AP v2 entities (e.g. agents, catalogs) that are part of Base Registry datasets. Entities are persisted in a Virtuoso triple store.
* Visualise Base Registry datasets in a human-readable way.
* Export these datasets in an interoperable, machine-readable format conformant to the BRegDCAT-AP v2 specification.

## Deployment

### Docker

A self-contained [docker-compose](https://docs.docker.com/compose/install/) configuration file is provided to ease the deployment process:

    $ cd path_to_editor
    $ docker-compose up --build
    
The application can be then accessed on http://localhost:40080/

### Local deployment 

The tool is based on [Drupal](https://www.drupal.com). This projects contains an installation guide and an initial database dump (`dcat-editor-database.sql`). Follow Drupal's [documentation](http://drupal.org/documentation) to configure a Drupal project.


To deploy the Public Service Description Editor locally, the administration will require PHP and Drupal environments installed on their webserver. The PHP version used is 5.6.15; the Drupal version is 7.42. Finally, a Virtuoso Triple store is needed to store the data created by the users.


The requirements and service dependencies for the local environment are:

* PHP 5.6.
* Drupal 7.42.
* Virtuoso triple store.

This projects contains an installation guide and an initial database dump (`dcat-mapping-database.sql`) only valid for Drupal deployment. In this database has some configurations thahth must be modified to work in other enviroments:

* ARC2 store settings -> admin/config/services/arc2_store at Drupal configuration
* SPARQL Endpoints Registry -> admin/structure/sparql_registry at Drupal configuration

## Virtuoso

Virtuoso endpoints is hardcoded in "export" module in /sites/all/modules/ folder. Review this URL and adapt to your instalation.
