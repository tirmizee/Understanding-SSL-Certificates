.
    
    openssl genrsa

.
    
    openssl genrsa -aes256

.
    
    openssl genrsa -des3


##### ตรวจสอบใบรับรอง

    openssl x509 -in cert.pem -text
    
    openssl x509 -in cert.crt -noout -text 

### Reference

- https://sharif2008.wordpress.com/2017/08/27/difference-between-p12-pfx-vs-crt-cer-vs-pem-vs-der/
- https://docs.oracle.com/cd/E29585_01/PlatformServices.61x/security/src/tsec_ssl_jsp_pkcs12.html
- https://serverfault.com/questions/483465/import-of-pem-certificate-chain-and-key-to-java-keystore
