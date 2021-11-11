```sh
docker run \
    -v $(pwd):/var/loadtest \
    --net host \
    -it \
    direvius/yandex-tank
```

```sh
curl 'http://xxx.xxx.xxx.xxx/graphql' \
  -H 'content-type: application/json' \
  --data-raw $'{"query":"query Query($sessionId: String\u0021) {\\n  order(sessionId: $sessionId) {\\n    id\\n    completed\\n    created\\n    sessionId\\n    number\\n    items {\\n      id\\n      quantity\\n      product {\\n        id\\n        title\\n        description\\n        shopId\\n      }\\n    }\\n  }\\n}\\n","variables":{"sessionId":"qwernull"},"operationName":"Query"}' \
  --compressed
```
