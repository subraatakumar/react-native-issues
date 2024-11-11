- Clear the CocoaPods cache

```bash
rm -rf ~/Library/Caches/CocoaPods
rm -rf Pods
rm podfile.lock
rm -rf ~/Library/Developer/Xcode/DerivedData/*
pod deintegrate
pod cache clean --all
pod setup
pod install
```

- Removing the Pods folder and reinstalling:

```bash
rm -rf Pods
rm Podfile.lock
pod install --repo-update
```


- Check Header Search Paths in Xcode

  - Open your project in Xcode.
  - Navigate to the project settings.
  - Go to Build Settings.
  - Look for Header Search Paths and ensure it includes

```bash
$(SRCROOT)/../node_modules/react-native/React
$(SRCROOT)/../node_modules/react-native.
```

- [official link for fix](https://github.com/facebook/react-native/commit/8721ee0a6b10e5bc8a5a95809aaa7b25dd5a6043)

```bash
-- (NSArray<RCTModuleData *> *)_initializeModules:(NSArray<id<RCTBridgeModule>> *)modules
+- (NSArray<RCTModuleData *> *)_initializeModules:(NSArray<Class> *)modules
                               withDispatchGroup:(dispatch_group_t)dispatchGroup
                                lazilyDiscovered:(BOOL)lazilyDiscovered
```

- gyp ERR! not ok

```bash
brew install python
brew install gcc
sudo npm config set python $(which python)
```

after this check on command line `python --version`: It should display the python version number.
- if still problem persist, check `.python-version` of your project root.
