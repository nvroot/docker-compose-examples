
git clone https://github.com/langfuse/langfuse


For NEXTAUTH_SECRET and SALT use:

```
openssl rand -base64 32
```


For ENCRYPTION_KEY use: 
```
openssl rand -hex 32
```