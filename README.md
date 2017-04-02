# http2-node-test-server-push

 openssl genrsa -des3 -passout pass:x -out server.pass.key 2048
Then run this:

$ openssl rsa -passin pass:x -in server.pass.key -out server.key
Observe:

writing RSA key
Get rid of RSA:

$ rm server.pass.key
$ openssl req -new -key server.key -out server.csr
Answer questions:

Country Name (2 letter code) [AU]:US
State or Province Name (full name) [Some-State]:California
A challenge password []:
...
Finally run:

$ openssl x509 -req -sha256 -days 365 -in server.csr -signkey server.key -out server.crt
At the end, you should have three SSL files:

server.crt

server.csr

server.key


# npm start
