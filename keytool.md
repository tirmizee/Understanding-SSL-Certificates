##### Create a Server Certificate

-genkey same as -genkeypair 
    
    keytool -genkey -alias server-alias -keyalg RSA -keypass changeit -storepass changeit -keystore keystore.jks
