# XboxBigButton
A C# library and example project showing how to interface with the Xbox 360 Big Button Controllers ([Scene It?](https://en.wikipedia.org/wiki/Scene_It%3F) game controllers)

![The Scene It game kit](http://1.bp.blogspot.com/-lRn76FpzitM/Vh1W2TxJ7mI/AAAAAAAABaw/LVQ4r_PY4ZI/s1600/02.jpg "The Scene It game kit")

The project page can be found at [http://sverrirs.github.io/XboxBigButton/](http://sverrirs.github.io/XboxBigButton/)

<p align="center">
  <a href="https://www.paypal.me/sverrirs/1.5" target="_blank"><img border="0" src="https://www.paypalobjects.com/en_US/i/btn/x-click-but21.gif" alt="Like my work? You can donate to this project using PayPal" title="Like my work? You can donate to this project using PayPal"></a>
</p>

# Driver installer
A downloadable binary for the driver install (both 32 and 64 bit versions) can be found under *XboxBigButton_WinUsbDriver/binaries* folder. 
Note: These installers have not been tested with Win8 and newer so they might not work (due to the fact that Windows 8+ requires .inf files to be signed as well)

# Dependencies
* Uses the [WinUsb.NET](https://github.com/madwizard-thomas/winusbnet/) project 
* Requires the custom driver in the *XboxBigButton_WinUsbDriver* folder to be installed prior to running any of the code.

# Examples
```csharp
var _device = new XboxBigButtonDevice();
_device.ButtonStateChanged += _device_ButtonStateChanged;
_device.Connect();
```

After installing the included driver, the only think you need to do is to create an instance of the Device and connect it. Then your ButtonStateChanged event handler will receive a callback every time the user presses a button on any of the controllers attached.

Please refer to the included example App project for more usage examples.

# Further info
[My blog](http://hardkjarni.blogspot.co.uk/2015/10/how-to-use-xbox-360-big-button.html) goes into some details about the process of getting the custom driver to work.
