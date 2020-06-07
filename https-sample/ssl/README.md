## How to create a certificate

Run below commands:

- openssl genrsa -out server.key 2048
- openssl req -sha256 -new -key server.key -out server.csr -subj '/CN=localhost/O=kdnakt.com/C=jp'
- openssl x509 -req -sha256 -days 36500 -in server.csr -signkey server.key -out server.crt -extfile san.config
