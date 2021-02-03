## Passive infrared motion sensor (PIR)

Humans and other animals emit heat all the time. 

A PIR sensor detects changes in the amount of IR radiation (heat) it receives. When there is a change, then a pulse is triggered. This means that a PIR sensor can detect when a human (or any animal) moves in front of it.

![pir](images/pir_module.png)

The pulse emitted when a PIR detects motion needs to be amplified, and so it needs to be powered. There are three pins on the PIR; they should be labeled `Vcc`, `Gnd`, and `Out`. If these labels aren't clear, they are sometimes concealed beneath the Fresnel lens (the white cap), which you can temporarily remove to see the pin labels.

--- task ---
Wire up your PIR sensor to your Raspberry Pi

![wiring](images/pir_wiring.png)

As shown above, the `Vcc` pin needs attaching to a `5V` pin on the Raspberry Pi.
The `Gnd` pin on the PIR sensor can be attached to *any* ground pin on the Raspberry Pi.
Lastly, the `Out` pin needs to be connected to any of the GPIO pins.
--- /task ---

--- task ---
The PIR acts a little like a button. Add the following code, so that the sprite can detect any motion in your area.

```blocks3
when flag clicked
set gpio (17 v) to input [pulled low] ::extension

when gpio (17 v) is [high v] ::hat extension
say [you moved]

when gpio (17 v) is [low v] ::hat extension
say [you're still]
```
--- /task ---

If your PIR doesn't seem to work, then you might like to try tuning it a little.

[[[generic-electronics-tune-pir]]]
