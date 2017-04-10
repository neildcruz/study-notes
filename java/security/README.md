# Security and Keys


## Useful commands

Create a PPK pair using the keytool utility

```language
keytool -genkeypair -alias jwt_key -keyalg RSA -keysize 2048 -keystore keystore.jks -v

where 

alias : alias of the key in the keystore
keyalg : algorithm for encryption
v: verbose

```

Export the public key from the generated keypair using keytool

`keytool -export -keystore keystore.jks -alias jwt_key -file public.cer` 


Convert the public key from the keypair in the DER format using openssl

`openssl x509 -inform der -in public.cer -pubkey` 




