## Constructing a Scratch 2 program

1.  Locate the Scratch 2 program by clicking on **Menu** followed by **Programming**, and selecting **Scratch 2**, remember to use version 2, not version 1.

 ![](images/scratch-icon.png)

1. The familiar Scratch interface will then load:

 ![](images/Scratch-interface.png "The Scratch Interface")

1. We need to setup Scratch to use the GPIO pins. Click on **More Blocks** in the top right display and click on **Add an Extension**.

![](images/add-an-extension.png)

1. Select Pi GPIO and click on.  

![](images/pi-gpio.png)

1. You will see two new blocks appear, we will be using these to control and sense the GPIO pins.

![](images/new-blocks.png)

1.  Click on **Events** in the top-right (Scripts tab) display. Drag the `when GreenFlag clicked` block onto the scripts area:

  ![greenflag](images/greenflag.png)

1. From this point on, you can control your LED using the two new blocks: `set gpio 17 to output high` to turn it on and `set gpio 17 to output low` to turn it off. Using these two messages and some pauses, you can make an LED flash continuously:

  ![Flashing LED](images/led_flash.png)
