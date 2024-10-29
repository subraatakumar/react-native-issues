- uninstall all the previously installed ruby versions

- https://stackoverflow.com/questions/66644365/cocoapods-on-m1-apple-silicon-fails-with-ffi-wrong-architecture
  
```bash
rbenv install 3.1.2
rbenv global 3.1.2
rbenv rehash
gem install bundler
sudo arch -x86_64 gem install ffi
sudo arch -x86_64 gem install cocoapods
gem list | grep ffi
gem list | grep cocoapods
pod --version
```
