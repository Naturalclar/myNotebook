# react-native 0.60 で、 react-native link が必要なくなって、楽になった話。

`react-native-vector-icons` や `react-native-gesture-handler` のような、Native ライブラリに依存しているパッケージ

## iOS

cocoa pods の導入

```
sudo gem install cocoapods
```

```sh
cd ios
pod install
```
