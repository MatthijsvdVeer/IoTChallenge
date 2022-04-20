# The IoT Challenge!
Welcome code, you've been tasked by the client with creating the world's best internet connected calculator! In school they said you would never have full-time access to a calculator, but here it is! That'll show them.

## What are you building?
The calculator you're building is quite special. Instead of punching in numbers on the device, the calculator will receive commands for the cloud asking for results. These requests come straight from the main Azure IoT Hub and your calculator needs to respond to them quickly!

IoT Hub will communicate with your calculator in two different ways, Device Twin Desired Properties and Direct Methods.

## Desired Properties
The device twin desired properties will indicate what 'mode' your calculator is in. It can be any of the following modes:
- add (add the numbers together)
- multiply (multiply the numbers)
- min (find the lowest number)
- max (find the highest number)

## Direct Methods
When a direct method comes in, it will always contain a payload with a JSON body containing an array of numbers. The mode that was set in the Device Twin indicates the operation that needs to be done. When you have calculated the result, send back the answer in the following format:
```json
{
  "answer": 42
}
```

## Building The Calculator
You've been granted an ESP32 for development purposes. The client knows you're not the world's greatest embedded developer, so please go ahead and build the calculator using .NET nanoFramework. There are some good resources to get started here:
- [Get started with Visual Studio][1]
- [IoT Hub Library for NanoFramework][3]

You can connect to the Azure IoT Hub using a device ID and SAS key. Contact the organiser to get hold of these credentials.

## More Calculations, More Points!
There is a central scoreboard, that shows who's completed the most calculations. It's not a contest (we promise)

## Misc
You might need to manually install drivers on your Windows machine, this isn't always the case. [USB UART Drivers][2]

Using Visual Studio and icons are missing? Quit Visual Studio entirely and run
```devenv /updateConfiguration```

[1]: https://docs.nanoframework.net/content/getting-started-guides/getting-started-managed.html?WT.mc_id=IoT-MVP-5004034
[2]: https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers
[3]: https://github.com/nanoframework/nanoFramework.Azure.Devices
