##### สร้าง Server Certificate
    
    ใช้คำสั่ง genkey ซึ่งคำเป็นคำสั่งจาก keytool เวอชันเก่า
    keytool -genkey -alias server-alias -keyalg RSA -keypass changeit -storepass changeit -keystore keystore.jks -storetype JKS

    ใช้คำสั่ง genkey ซึ่งคำเป็นคำสั่งจาก keytool เวอชันเก่าใหม่
    keytool -genkeypair -alias server-alias -keyalg RSA -keypass changeit -storepass changeit -keystore keystore.jks -storetype JKS

    ใช้คำสั่ง genkey
    keytool -genkey -alias server -keyalg RSA -keysize 2048 -keystore 192_168_0_56.jks -dname "CN=192.168.0.56,OU=test, O=test, L=test, ST=test, C=TH" -storetype JKS

##### สำรวจเนื้อหาของ keystore

    keytool -list -v -keystore keystore.jks

##### ส่งออก csr จาก keystore.jks 

     keytool -certreq -alias server -file 192_168_0_56.csr -keystore 192_168_0_56.jks

##### ส่งออก certificate (public) จาก keystore.jks ไปยัง file

    export certificate เป็นยังไฟล์นามสกุล .cer
    keytool -export -alias server-alias -storepass changeit -file server.cer -keystore keystore.jks
    
    export certificate เป็นยังไฟล์นามสกุล .der
    keytool -export -alias server-alias -storepass changeit -file server.der -keystore keystore.jks
     
    export certificate เป็นยังไฟล์นามสกุล .crt
    keytool -export -alias server-alias -storepass changeit -file server.crt -keystore keystore.jks

    export certificate ในรูปแบบ "Base 64 encoding" โดยใช้คำสั่ง -rfc
    keytool -export -alias server-alias -storepass changeit -file server.crt -keystore keystore.jks -rfc

##### ส่งออก key/privatekey จาก keystore.jks ไปยัง file

    แปลงจาก JKS เป็น PKCS12
    keytool -importkeystore -srckeystore keystore.jks -destkeystore keystore.p12 -deststoretype PKCS12 
    -srcalias server-alias -deststorepass zaq12wsx -destkeypass zaq12wsx
    
    ใช้ openssl เพื่อ export PKCS12 ไปยัง .pem file
    openssl pkcs12 -in keystore.p12  -nodes -nocerts -out key.pem

### Reference

- https://www.digicert.com/easy-csr/keytool.htm
