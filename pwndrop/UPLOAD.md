### 1. Uploading to a Self-Hosted PWNDrop
```sh
tar -czhvf archive.tar.gz ./
```

```sh
curl -T project_export.tar.gz https://p.site.cc/webdav/ \
  -u "admin:your_password"\
  --http1.1
```
