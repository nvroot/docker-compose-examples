# Penpot

<p align="left">
  <img src="../logo/penpot.svg" width="100" height="100">
</p>

| Name | Description |
|----------------|--------|
| **Used Image** |   penpotapp/frontend:latest   |
| **Description** |  —  |
| **Website** | —    |
| **Docs** |    —    |
| **Registry** |    https://hub.docker.com/r/penpotapp/frontend   |
| **Source&nbsp;Code&nbsp;** |   —  |
| **Port** |    8080, 6061   |
Secret key#
The PENPOT_SECRET_KEY envvar serves a master key from which other keys for subsystems (eg http sessions, or invitations) are derived.

To use it, we recommend using a truly randomly generated 512 bits base64 encoded string here. You can generate one with:
```
python3 -c "import secrets; print(secrets.token_urlsafe(64))"
```
And configure it:

PENPOT_SECRET_KEY: my-super-secure-key
