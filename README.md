# scdf-recipe-filter

```shell

stream create --name filtertest --definition "http | filter --expression=payload=='good' | log" --deploy

expression="#jsonPath(payload,'$.name') matches '\d*'

filter --expression="!payload.description.equals('invalid order')"

```

```shell

http post --target http://localhost:9000 --data "good"

```
