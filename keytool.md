##### สร้าง Server Certificate
    
    ใช้คำสั่ง genkey ซึ่งคำเป็นคำสั่งจาก keytool เวอชันเก่า
    keytool -genkey -alias server-alias -keyalg RSA -keypass changeit -storepass changeit -keystore keystore.jks

    ใช้คำสั่ง genkey ซึ่งคำเป็นคำสั่งจาก keytool เวอชันเก่าใหม่
    keytool -genkeypair -alias server-alias -keyalg RSA -keypass changeit -storepass changeit -keystore keystore.jks

##### สำรวจเนื้อหาของ keystore

    keytool -list -v -keystore keystore.jks

##### Export certificate (public) จาก keystore.jks ไปยัง file


    keytool -export -alias server-alias -storepass changeit -file server.cer -keystore keystore.jks
    
    keytool -export -alias server-alias -storepass changeit -file server.det -keystore keystore.jks
     
    keytool -export -alias server-alias -storepass changeit -file server.crt -keystore keystore.jks

##### Print Certificate
