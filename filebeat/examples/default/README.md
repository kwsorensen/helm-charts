<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Default](#default)
  - [Usage](#usage)
  - [Testing](#testing)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Default

This example deploy Filebeat 8.0.0-SNAPSHOT using [default values][].


## Usage

* Deploy [Elasticsearch Helm chart][].

* Deploy Filebeat chart with the default values: `make install`

* You can now setup a port forward to query Filebeat indices:

  ```
  kubectl port-forward svc/elasticsearch-master 9200
  curl localhost:9200/_cat/indices
  ```


## Testing

You can also run [goss integration tests][] using `make test`


[elasticsearch helm chart]: https://github.com/elastic/helm-charts/tree/master/elasticsearch/examples/default/
[goss integration tests]: https://github.com/elastic/helm-charts/tree/master/filebeat/examples/default/test/goss.yaml
[default values]: https://github.com/elastic/helm-charts/tree/master/filebeat/values.yaml
