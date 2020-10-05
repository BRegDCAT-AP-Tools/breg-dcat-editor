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

The tool is based on [Drupal](https://www.drupal.com), please see Drupal's [documentation](http://drupal.org/documentation) for more information.

The requirements and service dependencies for the local environment are:

* PHP 5.6.
* Drupal 7.42.
* Virtuoso triple store.
* MySQL.

The configuration of the **MySQL database** can be modified in `sites/default/settings.php`. It points to the `mysql` hostname of the container defined in the Compose file by default:

```
...

$databases = array (
  'default' => 
  array (
    'default' => 
    array (
      'database' => 'dcat-editor',
      'username' => 'root',
      'password' => 'root',
      'host' => 'mysql',
      'port' => '',
      'driver' => 'mysql',
      'prefix' => '',
    ),
  ),
);

...
```

Modifying the configuration of the **Virtuoso triple store** would require replacing all hardcoded references to the `virtuoso` hostname in:

* `sites/all/modules/export/export.module`

Once the Drupal application is up and running please make sure to also update the SPARQL endpoint in the following configuration pages:

* *ARC2 store settings*: `admin/config/services/arc2_store`
* *SPARQL Endpoints Registry*: `admin/structure/sparql_registry`