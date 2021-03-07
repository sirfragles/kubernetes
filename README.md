# kubernetes

# Configure TLS with Self-Signed certificates

openssl req -newkey rsa:4096 -x509 -sha256 -days 3650 -nodes -out ams.crt -keyout ams.key

kubectl create secret tls antmedia-cert --key="ams.key" --cert="ams.crt"
