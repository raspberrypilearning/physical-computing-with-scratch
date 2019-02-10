## Responding to a button press

1. Now that your button is all set up and working, you can make it do something. You can start off by making it control a sprite.

1. Begin with a `forever` loop with an `if` block inside it. This will continually check the `if` condition and perform some action if the condition is met. The action in the example below will make the current sprite say "Hello!":

1. Finally, to make this work you need to add the condition, which is that we want the sprite to speak when the **gpio 21 is high**:

    ![Loop with condition](images/say-hello.png)

If everything is correct, your button should make the sprite speak.
