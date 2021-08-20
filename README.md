# NetworkMonitor-Swift
Network Monitor for Swift Language

![macOS](https://img.shields.io/badge/macOS-10.14-yellow)
![iOS](https://img.shields.io/badge/iOS-12.0-green)
![licence](https://img.shields.io/badge/license-MIT-orange.svg)
![swift](https://img.shields.io/badge/swift-5.0-red.svg)

## Usage

Start the Network Monitor shared instance in `application:didFinishLaunchingWithOptions:` method in AppDelegate:

```swift
// Start shared instance
NetworkMonitor.shared.startMonitoring()
```

### Stop monitoring

```swift
// Stop shared instance
NetworkMonitor.shared.stopMonitoring()
```

### Check internet connection

```swift
let isConnected: Bool = NetworkMonitor.shared.isConnected
```

### Check connection type

```swift
let type: NetworkMonitor.ConnectionType? = NetworkMonitor.shared.connectionType
```

### Available connection types

```swift
public enum ConnectionType {
    case wifi
    case cellular
    case ethernet
}
```