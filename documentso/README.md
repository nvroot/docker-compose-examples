### **Generate Private Key**

Generate a private key using OpenSSL by running the following command:

```
openssl genrsa -out private.key 2048
```

This command generates a 2048-bit RSA key.

### **Generate Self-Signed Certificate**

Using the private key, generate a self-signed certificate by running the following command:

```
openssl req -new -x509 -key private.key -out certificate.crt -days 365
```

You will be prompted to enter some information, such as the certificate's Common Name (CN). Ensure that you provide the correct details. The `—days` parameter specifies the certificate's validity period.

### **Create `p12` Certificate**

Combine the private key and the self-signed certificate to create a `.p12` certificate. Use the following command:
```
openssl pkcs12 -export -out certificate.p12 -inkey private.key -in certificate.crt -legacy
```