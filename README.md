# Understanding-SSL-Certificates

##### .PEM .CRT Format

<small>X.509 certificate encoded in text (base64 and encrypted)</small>

##### .DER Format

<small>DER is a binary encoding for X.509 certificates and private keys. DER files are most commonly seen in Java contexts. DER and CER and CRT files are basically synonymous, they can be used interchangeably by simply changing the extension.</small>

##### .p12 (PKCS12) Format

<small>มีทั่ง private/public ฝั่งอยู่. มั่กพบเจอในระบบของ windows</small>

### Reference

- https://gist.github.com/fntlnz/cf14feb5a46b2eda428e000157447309
- http://www.herongyang.com/PKI/Intermediate-CA-Import-Certificate-Back-to-KeyStore.html
- https://security.stackexchange.com/questions/3779/how-can-i-export-my-private-key-from-a-java-keytool-keystore
- https://docs.oracle.com/en/database/other-databases/nosql-database/18.3/security/import-key-pair-java-keystore.html#:~:text=To%20import%20an%20existing%20key%20pair%3A%201%20Build,and%20client%20truststore%20described%20in%20the%20previous%20section.
- https://www.digicert.com/kb/csr-ssl-installation/tomcat-keytool.htm
- https://www.misterpki.com/keytool-export-cert/
- https://www.thesslstore.com/knowledgebase/ssl-generate/csr-generation-guide-for-nginx-openssl/
- https://www.digicert.com/kb/ssl-certificate-installation-java.htm
