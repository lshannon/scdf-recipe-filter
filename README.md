# scdf-recipe-filter

```shell

stream create --name filtertest --definition "http | filter --expression=payload=='good' | log" --deploy

```

```shell

http post --target http://localhost:9000 --data "good"

```
