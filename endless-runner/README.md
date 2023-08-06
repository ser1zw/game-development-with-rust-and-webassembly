## 事前設定

```sh
export NODE_OPTIONS="--openssl-legacy-provider --dns-result-order=ipv4first"
```

- `--openssl-legacy-provider`: `npm start` の際のエラー対応

```
error:0308010C:digital envelope routines::unsupported
```

- `--dns-result-order=ipv4first`: `registry.npmjs.org` がIPv6に対応していないため、 `npm install` の際にIPv6が使われるとエラーになる問題の対応

```
47 verbose stack FetchError: request to https://registry.npmjs.org/npm failed, reason: connect ECONNREFUSED 2606:4700::6810:1f22:443
```

## 起動

```sh
npm start
```
