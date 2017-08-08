## Constructing a Scratch program

-  Locate the Scratch program by clicking on **Menu** followed by **Programming**, and selecting **Scratch**.

 ![](images/scratch-icon.png)

- The familiar Scratch interface will then load:

 ![](images/Scratch-interface.png "The Scratch Interface")

-  Click on **Control** in the top-left display. Drag the `when GreenFlag clicked` block onto the scripts area:

  ![greenflag](images/greenflag.png)

- Scratch uses **broadcast** blocks to communicate with the GPIO pins; the first broadcast you need is `gpioserveron` which activates the GPIO functionality:

  ![gpioserveron](images/gpioserveron.png)

- As your GPIO pin can be used as either input or output, you'll need to specify in which mode your pin is being used with the `config17out` broadcast:

  ![config17on](images/config17.png)

- From this point on, you can control your LED using two broadcasts: `gpio17high` to turn it on and `gpio17low` to turn it off. Using these two messages and some pauses, you can make an LED flash continuously:

  ![Flashing LED](images/led_flash.png)

