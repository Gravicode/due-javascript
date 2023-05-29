Javascript
======

* * *

![Javascript](https://cdn-icons-png.flaticon.com/512/5968/5968292.png)

The Javascript DUE library allows for the use of full standard Javascript to access physical-computing.

[](#setup)Setup
---------------

This page assumes the user is already familiar with Javascript and there is a development machine that is already setup to build and run Javascript programs. No changes are needed there but we are using Microsoft Visual Studio Code as a personal preference.

##### Tip

If this is the first time you use your device, start by visiting the [Hardware](https://duelink.com/hardware/intro.html) page and load your device with the appropriate firmware. The [Console](https://duelink.com/software/console.html) is also a great place to start.

Start a new project with a simple line of code to test out the project is running

    print("Hello DUE!")
    

We now need to copy the DUE Javascript library [JS LIB](https://github.com/Gravicode/due-javascript/). The library is also available on the [downloads](https://duelink.com/software/downloads.html) page if needed.

##### Tip

The DUE Javascript library requires serial port access.

[](#blinky)Blinky!
------------------

Our first program will blink the on-board LED 20 times, where it comes on for 200ms and then it is off for 800ms.

##### Note
Init device and choose com port with this method

    this.comPort = new SerialInterface();
    comPort.Connect();

the init the driver and display some text.

    if (!this.dev)
            this.dev = new DUELinkController(this.comPort);
    # Flash the LED 20 times (on for 200ms and off for 800ms)
    dev.Led.Set(200,800,20);
    console.log("Bye DUE!");
    

[](#Javascript-api)Javascript API
-------------------------

The provided API mirrors DUE Script's [**Core library**](https://duelink.com/software/due-script/corelib/corelib.html). Referencing those APIs is a good place to learn about the available functionality and available arguments.

Javascript API

DUE Script Equivalent

Description

Analog.Read()

[ARead()](https://duelink.com/software/due-script/corelib/analog.html)

Reads analog pin

Analog.Write()

[AWrite()](https://duelink.com/software/due-script/corelib/analog.html)

Reads analog pin

Button.Enable()

[BtnEnable()](https://duelink.com/software/due-script/corelib/button.html)

Sets up a button to be used

Button.WasPressed()

[BtnDown()](https://duelink.com/software/due-script/corelib/button.html)

Detects if button is was pressed

Button.IsReleased()

[BtnDown()](https://duelink.com/software/due-script/corelib/button.html)

Detects if button is released

DeviceConfig.IsEdge()

[Version()](https://duelink.com/software/due-script/corelib/systemfunctions.html)

Checks for specific hardware

DeviceConfig.IsFlea()

[Version()](https://duelink.com/software/due-script/corelib/systemfunctions.html)

Checks for specific hardware

DeviceConfig.IsPico()

[Version()](https://duelink.com/software/due-script/corelib/systemfunctions.html)

Checks for specific hardware

DeviceConfig.IsPulse()

[Version()](https://duelink.com/software/due-script/corelib/systemfunctions.html)

Checks for specific hardware

DeviceConfig.MaxPinIO()

NA

Returns # available GPIOs

DeviceConfig.MaxPinAnalog()

NA

Returns # available Analog pins

Digital.Read()

[DRead()](https://duelink.com/software/due-script/corelib/digital.html)

Reads digital pin

Digital.Write()

[DWrite()](https://duelink.com/software/due-script/corelib/digital.html)

Writes to digital pin

Display.Clear()

[LcdClear()](https://duelink.com/software/due-script/corelib/lcd.html)

Clears the display black or white

Display.CreateImage()

[LcdConfig()](https://duelink.com/software/due-script/corelib/lcd.html)

Set display configuration

Display.Configuration()

[LcdConfig()](https://duelink.com/software/due-script/corelib/lcd.html)

Set display configuration

Display.DrawBuffer()

[LcdStream()](https://duelink.com/software/due-script/corelib/lcd.html)

Updates the entire display, using stream, with automatic Show()

Display.DrawBufferBytes()

[LcdStream()](https://duelink.com/software/due-script/corelib/lcd.html)

Updates the entire display, using stream, with automatic Show()

Display.DrawCircle()

[LcdCircle()](https://duelink.com/software/due-script/corelib/lcd.html)

Draws a circle on the display

Display.DrawFillRect()

[LcdFill()](https://duelink.com/software/due-script/corelib/lcd.html)

Draws a filled rectangle on the display

Display.DrawImage()

[LcdImg()](https://duelink.com/software/due-script/corelib/lcd.html)

Draws an image using an array

Display.DrawImageBytes()

[LcdImg()](https://duelink.com/software/due-script/corelib/lcd.html)

Draws an image using bytes

Display.DrawImageScale()

[LcdImg()](https://duelink.com/software/due-script/corelib/lcd.html)

Works same as DrawImage() adds scaling

Display.DrawLine()

[LcdLine()](https://duelink.com/software/due-script/corelib/lcd.html)

Draws a line on the display

Display.DrawRectangle()

[LcdRect()](https://duelink.com/software/due-script/corelib/lcd.html)

Draws a rectangle on the display

Display.DrawText()

[LcdText()](https://duelink.com/software/due-script/corelib/lcd.html)

Draws a text on the display

Display.DrawTextScale()

[LcdTextS()](https://duelink.com/software/due-script/corelib/lcd.html)

Draws scaled text on the display

Display.SetPixel()

[LcdPixel()](https://duelink.com/software/due-script/corelib/lcd.html)

Draws pixel on the display

Display.Show()

[LcdShow()](https://duelink.com/software/due-script/corelib/lcd.html)

Sends the display buffer

Distance.Read()

[Distance()](https://duelink.com/software/due-script/corelib/distance.html)

Used to read distance sensors

Frequency.Write()

[Freq()](https://duelink.com/software/due-script/corelib/frequency.html)

Hardware generated PWM signal

I2c.Write()

[I2cStream()](https://duelink.com/software/due-script/corelib/i2c.html)

I2C write, using stream

I2c.Read()

[I2cStream()](https://duelink.com/software/due-script/corelib/i2c.html)

I2C read, using stream

I2c.WriteRead()

[I2cStream()](https://duelink.com/software/due-script/corelib/i2c.html)

I2C write/read, using stream

Infrared.Enable()

[IrEnable()](https://duelink.com/software/due-script/corelib/infrared.html)

Enables pin for IR signal capture

Infrared.Read()

[IrRead()](https://duelink.com/software/due-script/corelib/infrared.html)

Reads value from IR enabled pin

Led.Set()

[LED()](https://duelink.com/software/due-script/corelib/led.html)

Controls the on-board LED

Neo.Clear()

[NeoClear()](https://duelink.com/software/due-script/corelib/neopixel.html)

Clears all LED's in memory

Neo.SetColor()

[NeoSet()](https://duelink.com/software/due-script/corelib/neopixel.html)

Set's a specific LED to a color

Neo.Show()

[NeoShow()](https://duelink.com/software/due-script/corelib/neopixel.html)

Transfers the internal pattern to LEDs

Neo.SetMultiple()

[NeoStream()](https://duelink.com/software/due-script/corelib/neopixel.html)

Updates all LEDs, using streams, with automatic `Show()`

Led.Set()

[LED()](https://duelink.com/software/due-script/corelib/led.html)

Controls the on-board LED

ServoMoto.Set()

[ServoSet()](https://duelink.com/software/due-script/corelib/servo.html)

Sets servo motor connected to a pin

Sound.Play()

[Sound()](https://duelink.com/software/due-script/corelib/sound.html)

Sets buzzer sound on supported hardware

Sound.Stop()

[Sound()](https://duelink.com/software/due-script/corelib/sound.html)

Stops buzzer sound on supported hardware

Spi.Configuration()

[SpiCfg()](https://duelink.com/software/due-script/corelib/spi.html)

Configures SPI bus

Spi.Palette()

[Palette()](https://duelink.com/software/due-script/corelib/spi.html)

Sets the desired color for a palette

Spi.Read()

[SpiByte()](https://duelink.com/software/due-script/corelib/spi.html)

Reads SPI byte

Spi.Write()

[SpiByte()](https://duelink.com/software/due-script/corelib/spi.html)

Sends SPI byte

Spi.Write4bpp()

[Spi4Bpp()](https://duelink.com/software/due-script/corelib/spi.html)

Streams and converts data from 4BPP to 16BPP

Spi.WriteRead()

[SpiStream()](https://duelink.com/software/due-script/corelib/spi.html)

Write & Read SPI bytes

System.Beep()

[Beep()](https://duelink.com/software/due-script/corelib/beep.html)

Uses any pin to generate a tone

System.GetTickMicroseconds()

[TickUs()](https://duelink.com/software/due-script/corelib/systemfunctions.html)

Returns system time in microseconds

System.GetTickMilliseconds()

[TickMs()](https://duelink.com/software/due-script/corelib/systemfunctions.html)

Returns system time in milliseconds

System.Reset()

[Reset()](https://duelink.com/software/due-script/corelib/systemfunctions.html)

Resets the board

Touch.Read()

[TouchRead()](https://duelink.com/software/due-script/corelib/touch.html)

Initialize a pin for touch

Uart.BytesToRead()

[UartCount()](https://duelink.com/software/due-script/corelib/uart.html)

How many bytes buffered and ready to read

Uart.Enable()

[UartInit()](https://duelink.com/software/due-script/corelib/uart.html)

Initialize UART

Uart.Read()

[UartRead()](https://duelink.com/software/due-script/corelib/uart.html)

Read UART data

Uart.Write()

[UartWrite()](https://duelink.com/software/due-script/corelib/uart.html)

Write UART data

Version()

[Version()](https://duelink.com/software/due-script/corelib/systemfunctions.html)

Returns the current DUE firmware version

##### Note

For convenience, the Pin Enum includes, ButtonA, ButtonB and Led. For example: `dev.Digital.Write(dev.Pin.Led, True)`

[](#due-script-control)DUE Script Control
-----------------------------------------

These methods allow developers to control DUE Scripts right from within .NET

Method

Description

Script.Execute()

Executes the single line of code immediately

Script.IsRunning()

Checks if DUE Script is running

Script.Load()

Loads the line into internal buffer

Script.New()

Clears the program stored in flash

Script.Read()

Read the program stored in flash and return as string

Script.Record()

Sends the internal buffer to the device, overwriting any previous programs

Script.Run()

Runs the program stored in flash

This example will load a simple program line by line and then record it.

    dev.Script.Load("c = 10")
    dev.Script.Load("@Blink");
    dev.Script.Load("Led(100,100,c)")
    dev.Script.Record()
    

This is an example to execute a single line(immediate mode). This does not modify the application stored in flash.

    dev.Script.Execute("LED(200,200,10)")
    

You can also access a previously recorder program using goto (to label) or by calling a function that has a return. This example calls the recorded program above.

    dev.Script.Execute("c=5:goto Blink")