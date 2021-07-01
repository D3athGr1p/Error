### Error :  ‘recursive_mutex’ is not a member of ‘std’ using Recursive Mutex = Annotated Mixin<std::recursive_mutex>;

Or

### Error : ‘mutex’ is not a member of ‘std’

Or

### Error : 'mutex' is not a member of 'std' in MinGW 5.3.0

##### Solution

```javascript

Set the default mingw32 g++ compiler option to posix.

x64
update-alternatives --config x86_64-w64-mingw32-g++

or

x32
update-alternatives --config i686-w64-mingw32-g++

Reference : https://github.com/PIVX-Project/PIVX/issues/1019

```