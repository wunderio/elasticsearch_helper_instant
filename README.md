# Elasticsearch Helper Instant

`elasticsearch_helper_instant` is a module that provides instant search functionality
based on [Elasticsearch Helper Content][elasticsearch_helper_content] module.

## Requirements

* Drupal 8 or Drupal 9
* [Elasticsearch Helper][elasticsearch_helper] module
* [Elasticsearch Helper Content][elasticsearch_helper_content] module

## Installation

Elasticsearch Helper Instant can be installed via the
[standard Drupal installation process](https://www.drupal.org/docs/extending-drupal/installing-drupal-modules).

## Configuration

* Install and enable [Elasticsearch Helper][elasticsearch_helper] module.
* Install and enable [Elasticsearch Helper Content][elasticsearch_helper_content] module
* Install and enable [Elasticsearch Helper Instant][elasticsearch_helper_instant]
  module.

## Usage

1. Install `Elasticsearch` search engine ([how-to][elasticsearch_download]).
2. Install [Elasticsearch Helper][elasticsearch_helper] module and configure it.
3. Install [Elasticsearch Helper Content][elasticsearch_helper_content] module
4. Install [Elasticsearch Helper Instant][elasticsearch_helper_instant] module.
5. Create indices using `drush` commands as follows:
    ```
    drush elasticsearch-helper-setup
    drush elasticsearch-helper-reindex
    drush queue-run elasticsearch_helper_indexing
    ```
6. Configure the `Search result highlighting input` display view mode of your
   relevant entities (a.ka. content types) to contain the desired data for search result output
   - By default `Search result highlighting input` display view mode used for search result output of an entity.

[elasticsearch_download]: https://www.elastic.co/downloads/elasticsearch
[elasticsearch_helper]: https://www.drupal.org/project/elasticsearch_helper
[elasticsearch_helper_content]: https://www.drupal.org/project/elasticsearch_helper_content
[elasticsearch_helper_instant]: https://www.drupal.org/project/elasticsearch_helper_instant
[elasticsearch_client]: https://github.com/elastic/elasticsearch-php
