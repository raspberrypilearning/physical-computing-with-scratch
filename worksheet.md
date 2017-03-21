# Physical computing with Scratch

## GPIO pins

One powerful feature of the Raspberry Pi is the row of GPIO pins along the top edge of the board. GPIO stands for General-Purpose Input/Output. These pins are a physical interface between the Raspberry Pi and the outside world. At the simplest level, you can think of them as switches that you can turn on or off (input) or that the Pi can turn on or off (output).

The GPIO pins allow the Raspberry Pi to control and monitor the outside world by being connected to electronic circuits. The Pi is able to control LEDs, turning them on or off, run motors, and many other things. It's also able to detect whether a switch has been pressed, the temperature, and light. We refer to this as physical computing.

There are 40 pins on the Raspberry Pi (26 pins on early models), and they provide various different functions.

If you have a RasPiO pin label, it can help to identify what each pin is used for. Make sure your pin label is placed with the keyring hole facing the USB ports, pointed outwards.

![](images/raspio-ports.jpg)

If you don't have a pin label, then this guide can help you to identify the pin numbers:

![](images/GPIO.png)

You'll see pins labelled as 3V3, 5V, GND and GP2, GP3, etc:

|   |   |   |
|---|---|---|
| 3V3 | 3.3 volts | Anything connected to these pins will always get 3.3V of power |
| 5V | 5 volts | Anything connected to these pins will always get 5V of power |
| GND | ground | Zero volts, used to complete a circuit |
| GP2 | GPIO pin 2 | These pins are for general-purpose use and can be configured as input or output pins |
| ID_SC/ID_SD/DNC | Special purpose pins ||

**WARNING**: If you follow the instructions, then playing about with the GPIO pins is safe and fun. Randomly plugging wires and power sources into your Pi, however, may destroy it, especially if using the 5V pins. Bad things can also happen if you try to connect things to your Pi that use a lot of power; LEDs are fine, motors are not. If you're worried about this, then you might want to consider using an add-on board such as the [Explorer HAT](https://shop.pimoroni.com/products/explorer-hat) until you're confident enough to use the GPIO directly.

## Lighting an LED

You can test whether your GPIO pins and LEDs are working by building the circuit below. You can use any resistor over about 50Ω.

1. The LED is connected directly to the **GND** pin and the **3V3** pin via the 330 Ohm resistor, and should light up.

1. Be sure to connect your LED the correct way round; the longer leg should be connected to the 3V3 pin:

![Test Circuit](images/led-3v3.png)

## Using a switchable pin

1. To control the LED, you'll need to adapt your circuit to use a switchable pin.

1. In the diagram below **pin 17** has been used, but you can use any numbered pin you wish.

![Test Circuit](images/led-gpio17.png)

## Constructing a Scratch program

1.  Locate the Scratch program by clicking on **Menu** followed by **Programming**, and selecting **Scratch**.

 ![](images/scratch-icon.png)

1. The familiar Scratch interface will then load:

 ![](images/Scratch-interface.png "The Scratch Interface")

1.  Click on **Control** in the top-left display. Drag the `when GreenFlag clicked` block onto the scripts area:

  ![greenflag](images/greenflag.png)

1. Scratch uses **broadcast** blocks to communicate with the GPIO pins; the first broadcast you need is `gpioserveron` which activates the GPIO functionality:

  ![gpioserveron](images/gpioserveron.png)

1. As your GPIO pin can be used as either input or output, you'll need to specify in which mode your pin is being used with the `config17out` broadcast:

  ![config17on](images/config17.png)

1. From this point on, you can control your LED using two broadcasts: `gpio17high` to turn it on and `gpio17low` to turn it off. Using these two messages and some pauses, you can make an LED flash continuously:

  ![Flashing LED](images/led_flash.png)

## Connecting a button

1. As well as controlling the physical world, you can react to it using an input device such as a button.

1. Connect your button to a breadboard, then connect one pin to a ground pin and the other to a numbered GPIO pin. In this example **pin 2** has been used:

![Button wiring](images/button.png)

## Configuring your button

1. Before Scratch can react to your button, it needs to be told which pin is configured as an input pin.

1. Assuming you have started a new Scratch file, you'll also need to start the GPIO server. The following code will configure pin 4 as an input:

  ![Configure Pin 2](images/config2.png)

1. Once you have built the code above, you need to click the green flag in order for it to run and for your pin to be set up.

1. Next, you need to go to the Sensing menu in Scratch:

  ![Sensing Menu](images/sensing.png)

1. From here you need to find the ![Slider Sensor](images/slider_sensor.png) block and click the triangle to reveal a menu. Select **gpio2** from the menu and click the tickbox to the left:

  ![Select sensor](images/sensing_select.png)

1. You should now see the current state of the pin in the stage area:

  ![Button state](images/button_watch.png)

1. Now when you press your button, the state should change from 1 to 0.

## Responding to a button press

1. Now that your button is all set up and working, you can make it do something. You can start off by making it control a sprite.

1. Begin with a `forever` loop with an `if` block inside it. This will continually check the `if` condition and perform some action if the condition is met. The action in the example below will make the current sprite say "Hello!":

    ![Loop with condition](images/conditional_loop.png)

1. Finally, to make this work you need to add the condition, which is that we want the sprite to speak when the **button value = 0**:

    ![Complete Code](images/button_code.png)

If everything is correct, your button should make the sprite speak.

## Controlling an LED with a button push

To finish off, you can combine your two programs so that the button can turn the LED on and off.

1. Adapt your script and use an `If Else` block so that it looks like the example below:

    ![Complete code](images/button_led.png)

1. Now when you push the button, the LED should light up.

## What next?

There are lots of other things you can control or monitor with your Raspberry Pi. Have a look at the worksheets below, to see how easily this can be done.

[Using an active buzzer](buzzer.md)  
[Making traffic lights](trafficlights.md)  
[Using a PIR sensor](pir.md)  


