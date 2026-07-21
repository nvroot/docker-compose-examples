# Nexus

<p align="left">
  <img src="../logo/nexus.svg" width="100" height="100">
</p>

| Name | Description |
|----------------|--------|
| **Used Image** |   sonatype/nexus3   |
| **Description** |  —  |
| **Website** | —    |
| **Docs** |    —    |
| **Registry** |    https://hub.docker.com/r/sonatype/nexus3   |
| **Source&nbsp;Code&nbsp;** |   —  |
| **Port** |    8081   |
Admin credentials:

admin:admin123

https://help.sonatype.com/en/re-encryption-in-nexus-repository.html

curl -X 'PUT' \
  'https://<your-instance-url>/service/rest/v1/secrets/encryption/re-encrypt' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -H 'NX-ANTI-CSRF-TOKEN: <any-token>' \
  -H 'X-Nexus-UI: true' \
  -d '{
  "secretKeyId": "string",
  "notifyEmail": "string"
}'
