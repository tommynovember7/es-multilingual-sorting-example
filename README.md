# ES Multilingual Sorting Example

## Getting Started

Build Elasticsearch images and create containers.

```shell
docker-compose build --force-rm --pull
```

```shell
docker-compose up --detach --force-recreate --remove-orphans
```

After executing `docker-compose up`, Please wait for kibana to start.
It might be helpful to see what's going on by viewing the log.

```shell
docker logs -f es-kibana
```

## Using Kibana

Once you've confirmed that kibana is up and running correctly,
open the dev tools at the following URL:

- [Dev Tools - Elastic](http://localhost:5601/app/dev_tools#/console)

`/sample/example-log.txt` might help you with easy use. You can copy and
paste that logs into the Kibana console and run them in order
from the top to see how they work.

You may find documents for experimental executions under the `/sample.`
directory. Feel free to run it and see how it works.

## Appendix

### Required plugins

`ICU` and `kuromoji` are officially supported plugins, but the 
Elasticsearch concatenation token filter is a community provided one: 

- [ICU Analysis Plugin](https://www.elastic.co/guide/en/elasticsearch/plugins/current/analysis-icu.html)
- [Japanese (kuromoji) Analysis Plugin](https://www.elastic.co/guide/en/elasticsearch/plugins/current/analysis-kuromoji.html)
- [Elasticsearch concatenation token filter](https://github.com/ryohashimoto/elasticsearch-concatenation-token-filter) (community plugin)
