## Connecting a button

As well as controlling the physical world, you can react to it using an input device such as a button.

--- task ---
Connect your button to a breadboard, then connect one pin to a ground pin and the other to a numbered GPIO pin. In this example **pin 2** has been used:

![Button wiring](images/button.png)
--- /task ---

--- task ---
Test that your button is working using this simple script

```blocks3
when button (2 v) is [pressed v] ::hat extension
say [hello] for (2) secs
```
--- /task ---

--- task ---
Press the button and the sprite should say `hello`.
--- /task ---

--- task ---
Can you use the extension to control an LED using a button?

--- hints --- --- hint ---
When the button is pressed, the LED should come on.
When the button is released, the LED should turn off.
--- /hint --- --- hint ---

Here are the blocks you will need to use

```blocks3
when button (2 v) is [pressed v] ::hat extension

when button (2 v) is [released v] ::hat extension

turn LED (17 v) [off v] ::extension

turn LED (17 v) [on v] ::extension
```

--- /hint --- --- hint ---
Here are the completed scripts

```blocks3
when button (2 v) is [pressed v] ::hat extension
turn LED (17 v) [on v] ::extension

when button (2 v) is [released v] ::hat extension
turn LED (17 v) [off v] ::extension
```

--- /hint --- --- /hints ---
--- /task ---
