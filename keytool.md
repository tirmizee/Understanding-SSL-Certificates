##### สร้าง Server Certificate
    
    ใช้คำสั่ง genkey ซึ่งคำเป็นคำสั่งจาก keytool เวอชันเก่า
    keytool -genkey -alias server-alias -keyalg RSA -keypass changeit -storepass changeit -keystore keystore.jks

    ใช้คำสั่ง genkey ซึ่งคำเป็นคำสั่งจาก keytool เวอชันเก่าใหม่
    keytool -genkeypair -alias server-alias -keyalg RSA -keypass changeit -storepass changeit -keystore keystore.jks

##### สำรวจเนื้อหาของ keystore

    keytool -list -v -keystore keystore.jks

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
    keytool -importkeystore -srckeystore keystore.jks -destkeystore keystore.p12 -deststoretype PKCS12 -srcalias server-alias -deststorepass zaq12wsx -destkeypass zaq12wsx
