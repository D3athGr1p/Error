### Ubuntu 22.04
### Error : Process Restart request too quickly

- error: failed to run custom build command for librocksdb-sys v0.6.1+6.28.2 
- --- stderr  
- rocksdb/include/rocksdb/c.h:65:10: fatal error: 'stdarg.h' file not found  
- rocksdb/include/rocksdb/c.h:65:10: fatal error: 'stdarg.h' file not found, err: true  thread 'main' panicked at

### Solution :
```javascript
sudo apt update
sudo apt install build-essential

sudo apt install libclang-dev

sudo apt install libc6-dev
```