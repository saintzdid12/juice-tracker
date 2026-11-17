<!-- juicetracker:begin -->
# Build JuiceTracker

Download **Wireless-Battery-Dark-Menus-source.zip** from the [release](https://github.com/saintzdid12/JuiceTracker/releases/tag/desktop-widget-v1). This asset contains the application source and build scripts. GitHub's automatically generated source links contain this downloads repository's documentation.

## Build with MinGW-w64

1. Extract the source ZIP and open a terminal in the folder containing **build.bat**.
2. Put **g++** and **windres** from a 64-bit MinGW-w64 toolchain on your PATH.
3. Run **build.bat**. It writes **WirelessBattery.exe** in the same folder. From an MSYS2 MinGW shell with Make installed, you can run **make** instead.
4. Run **make test** in an MSYS2 MinGW shell to run the included Rapoo and Logitech driver tests.

## Toolchain used for the release

The release EXE was built with [LLVM MinGW 20261020, x86-64 UCRT](https://github.com/mstorsjo/llvm-mingw/releases/tag/20261020). Its WinRT headers contain a duplicate boolean specialization. With this toolchain, add **-D____FIReference_1_boolean_INTERFACE_DEFINED__** to the **g++** compile-and-link command in the extracted **build.bat**, then run it. The release EXE uses a descriptive filename.
<!-- juicetracker:end -->
