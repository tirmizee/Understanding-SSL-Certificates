##### Create a Server Certificate
    
    keytool -genkey -alias server-alias -keyalg RSA -keypass changeit -storepass changeit -keystore keystore.jks

    keytool -genkeypair -alias server-alias -keyalg RSA -keypass changeit -storepass changeit -keystore keystore.jks

##### Print Certificate
