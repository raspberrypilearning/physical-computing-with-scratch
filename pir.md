# Passive infrared motion sensor (PIR)

Humans and other animals emit heat all the time. 

A PIR sensor detects changes in the amount of IR radiation (heat) it receives. When there is a change, then a pulse is triggered. This means that a PIR sensor can detect when a human (or any animal) moves in front of it.

![pir](images/pir_module.png)

## Wiring a PIR sensor

The pulse emitted when a PIR detects motion needs to be amplified, and so it needs to be powered. There are three pins on the PIR; they should be labelled `Vcc`, `Gnd`, and `Out`. If these labels aren't clear, they are sometimes concealed beneath the Fresnel lens (the white cap), which you can temporarily remove to see the pin labels.

![wiring](images/pir_wiring.png)

1. As shown above, the `Vcc` pin needs attaching to a `5V` pin on the Raspberry Pi.
1. The `Gnd` pin on the PIR sensor can be attached to *any* ground pin on the Raspberry Pi.
1. Lastly, the `Out` pin needs to be connected to any of the GPIO pins.

## Coding a PIR sensor

1.  With your PIR circuit complete, you are now ready to use Scratch to sense motion. Launch the Scratch program by clicking on **Menu** followed by **Programming** and selecting **Scratch**.

 Our version of Scratch on Raspbian is extra special. It allows you to access and control the GPIO pins.

1.  Click on **control** in the top-left display. Drag the ![green flag](images/green_flag.png) block onto the scripts area.

1. Drag a `broadcast` block to your scripts area and attach it to the ![green flag](images/green_flag.png) block. Click on the drop-down menu on the broadcast block and select **new**.

    Type `config4in` in the message name box. This instruction will tell the Raspberry Pi to set GPIO pin 4 as an input.

![Config Pin 4](images/scratch_config4.png)

1. Press the green flag in the upper-right corner of the Scratch window. This executes the instruction to set GPIO pin 4 as an input.

1. Scratch uses the 'Sensing' blocks to check if there is any input on the GPIO pins. If there is an input, the value of the pin changes from `0` to `1`. As you connected the PIR sensor to GPIO pin 4 of the Pi, we need to monitor that. Click on the drop-down menu on the `sensor value` block and choose `gpio4`.

1. Tick the checkbox to the left of the block to display the pin value on screen.

  ![Scratch sensing blocks](images/sensing-blocks.png)

1. Test the PIR sensor by waving your hand in front of it. When it detects movement, the value on the screen should change from `0` to `1`.

1. If the value doesn't change, check that the correct pins are connected.

Back to [Physical computing with Scratch](worksheet.md)
