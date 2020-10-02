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

The requirements and service dependencies for the local environment are:

* PHP 5.6.
* Drupal 7.42.
* Virtuoso triple store.