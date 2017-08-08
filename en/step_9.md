## Responding to a button press

- Now that your button is all set up and working, you can make it do something. You can start off by making it control a sprite.

- Begin with a `forever` loop with an `if` block inside it. This will continually check the `if` condition and perform some action if the condition is met. The action in the example below will make the current sprite say "Hello!":

    ![Loop with condition](images/conditional_loop.png)

- Finally, to make this work you need to add the condition, which is that we want the sprite to speak when the **button value = 0**:

    ![Complete Code](images/button_code.png)

If everything is correct, your button should make the sprite speak.

