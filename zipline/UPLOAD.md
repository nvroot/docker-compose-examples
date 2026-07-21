### Uploading to a Self-Hosted Zipline

```sh
tar -czhvf archive.tar.gz ./
```

```sh
curl -X POST https://zip.site.com/api/upload \
     -H "Authorization: TOKEN" \
     -F "file=@app.tar.gz"
```
