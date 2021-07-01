#### Error :
```javaScript
undefined reference to 'SHA256_Init' 
undefined reference to 'SHA256_Update'
undefined reference to 'SHA256_Final'

Getting error in crypto/SHA256_Init crypto/SHA256_Final 
                 crypto/SHA256_Update not found or undefined.
```
#### Solution :

```javascript
Edit configure.ac file
Add line AC_CHECK_LIB(crypto, CRYPTO_malloc,,) to the file.

Reference link: 
https://github.com/archiecobbs/mtree-port/commit/e11b06521a3accb6b15b85972ddf771b108b4897

```