
To generate `OCTOBOX_ATTRIBUTE_ENCRYPTION_KEY`:
```
docker run --rm -it octoboxio/octobox:latest bin/rails secret | cut -c1-32
```