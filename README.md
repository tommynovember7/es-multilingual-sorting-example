# ES Multilingual Sorting Example

It is assumed to run on Elasticsearch ver. 2.4. You might want to use some
HTTP client, for instance, [Postman](https://www.postman.com/),
[Insomnia](https://insomnia.rest/), Curl command or so.

## Getting Started

Build Elasticsearch images and create containers.

```shell
docker-compose build --force-rm --pull
```

```shell
docker-compose up --detach --force-recreate --remove-orphans
```

After executing `docker-compose up`, Please wait for the cluster to start.
It might be helpful to see what's going on by viewing the log.

```shell
docker logs -f es01
```

## Appendix

### Required plugins

`ICU` and `kuromoji` are officially supported plugins, but the 
`Elasticsearch concatenation token filter` is a community provided one:

- [ICU Analysis Plugin](https://www.elastic.co/guide/en/elasticsearch/plugins/2.3/analysis-icu.html)
- [Japanese (kuromoji) Analysis Plugin](https://www.elastic.co/guide/en/elasticsearch/plugins/2.3/analysis-kuromoji.html)
