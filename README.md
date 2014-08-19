# skim-blob-store

Blob store that will read from a remote blob store and cache it to a local one.

```
npm install skim-blob-store
```

## Usage

``` js
var skim = require('skim-blob-store')

var blobs = skim(localBlobStore, remoteBlobStore)

blobs.createReadStream({key: 'some-key', name: 'some blbo name'})
  .pipe(process.stdout)
```

In the above example if `some-key` is already in localBlobStore it will
just be read from that one. If not it will try and copy it from remoteBlobStore

## License

MIT