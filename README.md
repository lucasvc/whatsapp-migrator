# [WhatsApp crypt12 decryption tool](http://www.digitalinternals.com/security/decrypt-whatsapp-crypt12-database-messages/559/)

A Java tool to decrypt WhatsApp crypt12 files.

## Introduction

A Java tool to decrypt WhatsApp crypt12 files using a modified cryptography API library (based on Spongy Castle). 
 
## Requirements

* Linux. Tested on Ubuntu Linux 16.04.
* OpenJDK (not Oracle) version of Java. 

## Steps to Decrypt

To decrpt, do the following:
* Clone the repo.
```
$ git clone https://gitlab.com/digitalinternals/whatsapp-crypt12.git
$ cd whatsapp-crypt12
```
* Compile crypt12.java. 
```
$ javac -classpath "lib/whatsapp_spongycastle.jar:." crypt12.java
```
* Copy `key` and `msgstore.db.crypt12` files to the same repo directory
```
$ cp /path/to/file/key .
$ cp /path/to/file/msgstore.db.crypt12 .
```
* Decrypt using: 
```
java -cp "lib/whatsapp_spongycastle.jar:." crypt12
````

## Limitations

* This will not work on Oracle Java as it require JCE provider libraries to be signed.

## Creator

WhatsApp crypt12 decryption tool was created by and is maintained by **[Mohamed Ibrahim](http://www.digitalinternals.com/)**.

* https://twitter.com/ibrahimayoob
* https://gitlab.com/ibrahim

## Copyright and License

Copyright 2008-2016 Digital Internals. Code released under the [MIT](https://gitlab.com/digitalinternals/crypt12/blob/master/LICENSE) license.

