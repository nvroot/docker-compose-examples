# Passbolt

<p align="left">
  <img src="../logo/passbolt.svg" width="100" height="100">
</p>

| Name | Description |
|----------------|--------|
| **Used Image** |   passbolt/passbolt:latest-ce   |
| **Description** |  —  |
| **Website** | —    |
| **Docs** |    —    |
| **Registry** |    https://hub.docker.com/r/passbolt/passbolt   |
| **Source&nbsp;Code&nbsp;** |   —  |
| **Port** |    —   |
After installation run: 

```
docker exec passbolt su -m -c "bin/cake passbolt register_user -u your@email.com -f yourname -l surname -r admin" -s /bin/sh www-data
```
