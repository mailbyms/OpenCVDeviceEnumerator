# Device Enumerator for OpenCV 

此项目包含一个 C++ 类，该类允许在 Windows 中使用 DirectShow 枚举设备，以便选择和获取在创建（例如）VideoCapture 对象以从相机抓取帧时需要与 OpenCV 一起使用的 ID。我决定把它放在“如何获取要在OpenCV中使用的设备的ID？”是一个不断出现的问题。OpenCV的维护者不会在库中包含此功能，因为它非常依赖于操作系统。
## 内容

该项目包含类本身（DeviceEnumerator.h 和 DeviceEnumerator.cpp），以及如何使用该类的示例（OpenCVDeviceEnumerator.cpp）。



## 附加说明

1. 注释了 DeviceEnumerator::getDevicesMap(const GUID deviceClass) 里的获取不到 devicePath 就 continue 的逻辑，在 thinkpad x13 上，话筒有名称但没有 devicePath
2. 项目在 windows 10，visual studio 2017 下编译运行。不需要单独安装 directshow sdk，已自带。



## License

MIT License

Copyright (c) 2018 David Gil de Gómez Pérez (Studiosi)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

