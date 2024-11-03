- Clear the CocoaPods cache

```bash
rm -rf ~/Library/Caches/CocoaPods
rm -rf Pods
rm -rf ~/Library/Developer/Xcode/DerivedData/*
pod deintegrate
pod setup
pod install
```

- Removing the Pods folder and reinstalling:

```bash
rm -rf Pods
rm Podfile.lock
pod install --repo-update
```
