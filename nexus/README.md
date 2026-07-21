

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