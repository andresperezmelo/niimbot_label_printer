# NiimbotLabelPrinter

`NiimbotLabelPrinter` is a Flutter package that enables printing labels using Niimbot label printers. This package provides a simple interface to connect to a Niimbot printer via Bluetooth, manage connections, and send print data.

## Features

- Request Bluetooth permissions.
- Check if Bluetooth is enabled.
- Connect and disconnect from a Niimbot printer.
- Retrieve paired Bluetooth devices.
- Send print data to the printer.

## Installation

Add `niimbot_label_printer` to your `pubspec.yaml`:

```yaml
dependencies:
  niimbot_label_printer: ^0.0.1
```

## Usage

To use the `NiimbotLabelPrinter` plugin, follow these steps:

1. Request Bluetooth permissions:
```dart
final bool result = await NiimbotLabelPrinter.requestPermissionGrant();
```
2. Check if Bluetooth is enabled:
```dart
final bool result = await NiimbotLabelPrinter.bluetoothIsEnabled();
```
3. Connect to a Niimbot printer:
```dart
final bool result = await NiimbotLabelPrinter.connect(device);
```
4. Disconnect from a Niimbot printer:
```dart
final bool result = await NiimbotLabelPrinter.disconnect();
```
5. Retrieve paired Bluetooth devices:
```dart
final List<BluetoothDevice> devices = await NiimbotLabelPrinter.getPairedDevices();
```
6. Send print data to the printer:
```dart
final bool result = await NiimbotLabelPrinter.send(printData);
```
7. Desconnect from a Niimbot printer:
```dart
final bool result = await NiimbotLabelPrinter.disconnect();
```

## API Reference

### Methods

| Method                      | Description                                                   |
|-----------------------------|---------------------------------------------------------------|
| `getPlatformVersion()`       | Returns the platform version of the device.                   |
| `requestPermissionGrant()`   | Requests Bluetooth permission and checks if it's granted.     |
| `bluetoothIsEnabled()`       | Checks if Bluetooth is enabled on the device.                 |
| `isConnected()`              | Checks if the device is connected to a Niimbot printer.       |
| `getPairedDevices()`         | Returns a list of paired Bluetooth devices.                   |
| `connect(BluetoothDevice)`   | Connects to a specified Bluetooth device.                     |
| `disconnect()`               | Disconnects from the currently connected Bluetooth device.    |
| `send(PrintData)`            | Sends print data to the connected Niimbot printer.            |


### Class: PrintData

| Parameter      | Type       | Description                                                                   |
|----------------|------------|-------------------------------------------------------------------------------|
| `data`         | `List<int>`| A list of integers representing the raw print data.                           |
| `width`        | `int`      | The width of the label in pixels.                                             |
| `height`       | `int`      | The height of the label in pixels.                                            |
| `rotate`       | `bool`     | Indicates whether the label should be rotated before printing.                |
| `invertColor`  | `bool`     | Indicates whether the colors should be inverted before printing.              |


---
## Example

Here is an example of how the label looks:

![Example Label](https://github.com/andresperezmelo/niimbot_label_printer/raw/main/path_to_your_image.png)

---
## Created With

This package was created using the following technologies:

- [Flutter](https://flutter.dev)
- [Dart](https://dart.dev)
- [Kotlin](https://kotlinlang.org)

---

Created with ❤️ by [andresperezmelo](https://github.com/andresperezmelo)
