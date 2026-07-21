# Octobox

<p align="left">
  <img src="../logo/octobox.svg" width="100" height="100">
</p>

| Name | Description |
|----------------|--------|
| **Used Image** |   octoboxio/octobox:latest   |
| **Description** |  —  |
| **Website** | —    |
| **Docs** |    —    |
| **Registry** |    https://hub.docker.com/r/octoboxio/octobox   |
| **Source&nbsp;Code&nbsp;** |   —  |
| **Port** |    —   |
To generate `OCTOBOX_ATTRIBUTE_ENCRYPTION_KEY`:
```
docker run --rm -it octoboxio/octobox:latest bin/rails secret | cut -c1-32
```
