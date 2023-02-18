# springboot-https

### To create Keystore file see below

```bash
┌─[praveen@Praveens-MacBook-Air] - [~] - [4845]
└─[$] keytool -genkey -alias praveen-test -storetype JKS -keyalg RSA -keysize 2048 -validity 365 -keystore praveen-test.jks
Enter keystore password:  
Re-enter new password: 
What is your first and last name?
  [Unknown]:  Praveen Raja
What is the name of your organizational unit?
  [Unknown]:  ORG
What is the name of your organization?
  [Unknown]:  ORG
What is the name of your City or Locality?
  [Unknown]:  Coimbatore
What is the name of your State or Province?
  [Unknown]:  Tamilnadu
What is the two-letter country code for this unit?
  [Unknown]:  IN
Is CN=Praveen Raja, OU=ORG, O=ORG, L=Coimbatore, ST=Tamilnadu, C=IN correct?
  [no]:  yes

Generating 2,048 bit RSA key pair and self-signed certificate (SHA256withRSA) with a validity of 365 days
	for: CN=Praveen Raja, OU=ORG, O=ORG, L=Coimbatore, ST=Tamilnadu, C=IN
Enter key password for <praveen-test>
	(RETURN if same as keystore password):  

Warning:
The JKS keystore uses a proprietary format. It is recommended to migrate to PKCS12 which is an industry standard format using "keytool -importkeystore -srckeystore praveen-test.jks -destkeystore praveen-test.jks -deststoretype pkcs12".
```
```bash
┌─[praveen@Praveens-MacBook-Air] - [~] - [4847]
└─[$] keytool -importkeystore -srckeystore praveen-test.jks -destkeystore praveen-test.jks -deststoretype pkcs12
Enter source keystore password:  
Entry for alias praveen-test successfully imported.
Import command completed:  1 entries successfully imported, 0 entries failed or cancelled

Warning:
Migrated "praveen-test.jks" to PKCS12. The JKS keystore is backed up as "praveen-test.jks.old".
```
