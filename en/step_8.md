## Configuring your button

- Before Scratch can react to your button, it needs to be told which pin is configured as an input pin.

- Assuming you have started a new Scratch file, you'll also need to start the GPIO server. The following code will configure pin 2 as an input:

  ![Configure Pin 2](images/config2.png)

- Once you have built the code above, you need to click the green flag in order for it to run and for your pin to be set up.

- Next, you need to go to the Sensing menu in Scratch:

  ![Sensing Menu](images/sensing.png)

- From here you need to find the ![Slider Sensor](images/slider_sensor.png) block and click the triangle to reveal a menu. Select **gpio2** from the menu and click the tickbox to the left:

  ![Select sensor](images/sensing_select.png)

- You should now see the current state of the pin in the stage area:

  ![Button state](images/button_watch.png)

- Now when you press your button, the state should change from 1 to 0.
