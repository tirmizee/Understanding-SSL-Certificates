##### Create a Server Certificate
    
    keytool -genkey -alias server-alias -keyalg RSA -keypass changeit -storepass changeit -keystore keystore.jks

    keytool -genkeypair -alias server-alias -keyalg RSA -keypass changeit -storepass changeit -keystore keystore.jks

##### Export certificate(public) from keystore.jks

    keytool -export -alias server-alias -storepass changeit -file server.cer -keystore keystore.jks
    
    keytool -export -alias server-alias -storepass changeit -file server.det -keystore keystore.jks
     
    keytool -export -alias server-alias -storepass changeit -file server.crt -keystore keystore.jks

##### Print Certificate
