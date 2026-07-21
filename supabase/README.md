# Supabase

<p align="left">
  <img src="../logo/supabase.svg" width="100" height="100">
</p>

| Name | Description |
|----------------|--------|
| **Used Image** |   kong:2.8.1   |
| **Description** |  —  |
| **Website** | https://supabase.com    |
| **Docs** |    https://supabase.com/docs    |
| **Registry** |    https://hub.docker.com/r/supabase/supabase   |
| **Source&nbsp;Code&nbsp;** |   https://github.com/supabase/supabase  |
| **Port** |    3000   |
Doesn't works, problem with supabase-vector

1) Copy:
```
git clone --filter=blob:none --no-checkout https://github.com/supabase/supabase
cd supabase
git sparse-checkout set --cone docker && git checkout master
```

2) Rename Docker to Supabase:
```
mv docker/ supabase/
```
3) Backup `.env.example` and `docker-compose.yml`
```
cp .env.example .env
cp docker-compose.yml docker-compose.backup.yaml
```
4) Setup Minio (Get bucket, region, access-key, secret-key)
5) Add to storage on docker-compose:
```
STORAGE_BACKEND: s3
REGION: us-west
AWS_DEFAULT_REGION: us-west
GLOBAL_S3_BUCKET: bucketname
GLOBAL_S3_ENDPOINT: https://s3.minio.site
GLOBAL_S3_PROTOCOL: https
GLOBAL_S3_FORCE_PATH_STYLE: true
AWS_ACCESS_KEY_ID: minio-access-key
AWS_SECRET_ACCESS_KEY: minio-secret-key
```
6) Change credentials on `.env`
https://supabase.com/docs/guides/self-hosting/docker#generate-api-keys
