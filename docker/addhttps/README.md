# Install Mkcert  ##
> [!NOTE]
> required for https url
 1. Install the required packages
```
apt-get install wget libnss3-tools
```
2. Download the latest version of Mkcert from Github.
 ```
wget https://github.com/FiloSottile/mkcert/releases/download/v1.4.3/mkcert-v1.4.3-linux-amd64
```
3. Move the downloaded binary to the system path.
```
mv mkcert-v1.4.3-linux-amd64 /usr/bin/mkcert
```
```
chmod +x /usr/bin/mkcert
```
4. Generate Local CA.
```
mkcert -install
```
5. Generate a Certificate for Local Website.
   ```
   mkcert local.m2docker localhost 127.0.0.1 ::1
   ```
6. Copy certificates in the folder .docker/ssl and rename them as cert.pem cert-key.pem 
