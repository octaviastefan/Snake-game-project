# Snake game project
This repository contains information about the development of an educational project for university, related to the subject of Introduction to Robotics.

<details>
  <summary> <h2>  Introduction </h2> </summary>
  
##
  
 
Through this project, I want to create a version of the famous Snake game, well-known, played, and loved by many generations, using basic ardunino uno kit and materials. 

The idea for this project came from the desire to develop my own version of the first game I ever played many years ago on a Nokia phone. Of course, this game will be created using the components and knowledge I currently have. It may not be perfect, but I find it interesting and useful, and I am sure it will evoke nostalgia and fond memories for quite a few people.
  
##
</details>


<details>
  <summary> <h2> General Description </h2> </summary>

  ##
  
This Snake Game on Arduino is a project that uses an 8x8 LED matrix to display the snake, an LCD screen to show game information like the score, and a joystick for controlling the snake's movement. The game also includes sound effects via a buzzer, and a menu system to navigate through different game options.


##
</details>


<details>
  <summary> <h2> Hardware Design </h2> </summary>

  ##
  
   ### 1. List of components: 
   
  
##
 
 -   Arduino Uno (the central microcontroller that controls the entire game)
 -   8x8 LED Matrix (displays the game grid for Snake. The LEDs represent the snake's body and the food.)
 -   Joystick (controls the snake's movement)
 -   Buzzer (for sound effects based on game actions)
 -   Potentiometer (LCD)
 -   LCD (Displays game-related information such as the score, game status, or instructions.)
 -   Jumper Cables
 -   Mini breadboard
 -   Breadboard   
 
                                                                         

##

 ### 2. Electrical schematic (Wokwi) :

 ![wowki](https://github.com/user-attachments/assets/c17f4c64-6075-4b8e-bb8e-cde8e42450f6)


 


 ##

 ##

 ### 3. Block diagram:
 ![schema_bloc](https://github.com/user-attachments/assets/0897c971-217f-4feb-9daf-7f930bafa78c)

 


 ##

 ##

 ### 4. Bill of Materials:


| *No.* | *Component*                 | *Quantity*    | *Description*                         |*Link/Datasheet* 
|-------|-----------------------------|---------------|---------------------------------------|----------------------------------------------------------------------------------|
| *1*   | Arduino Uno                 | 1             | Central microcontroller               | [Ardino Kit](#)                                                                         |
| *2*   | 8x8 LED Matrix (MAX7219)    | 1             | Controlled via MAX7219 (SPI protocol) | [MAX7219 Datasheet](https://www.analog.com/media/en/technical-documentation/data-sheets/MAX7219-MAX7221.pdf) |
| *3*   | Joystick                    | 1             | For snake movement control            | [Arduino Kit](#)                                                                         |
| *4*   | Buzzer                      | 1             | For sound effects                     | [Arduino Kit](#)                                                                         |
| *5*   | Potentiometer (LCD)         | 1             | Adjusts LCD screen contrast           | [Arduino Kit](#)                                                                         |
| *6*   | LCD 16x2 (NO I2C)           | 1             | Meniu display                         | [Arduino Kit](#)                                                                         |
| *7*   | Jumper Cables               | more than 20  | Electrical connections                | [Arduino Kit](#)                                                                         |
| *8*   | Breadboard                  | 1             | For prototyping                       | [Arduino Kit](#)                                                                         |
| *9*   | Mini breadboard             | 1             |Prototyping for small components       | [Arduino Kit](#)                                                                         |


##

##

### 5. Pin Connections Table

| *Component*                 | *Arduino Uno Pin*          | *Component Pin*         | *Description*                    |
|-------------------------------|-----------------------------|---------------------------|------------------------------------|
| *8x8 LED Matrix (MAX7219)*  | *D11*                     | *DIN*                   | Data Input (SPI communication)     |
|                               | *D13*                     | *CLK*                   | Clock Signal (SPI)                 |
|                               | *D12*                     | *CS*                    | Chip Select (SPI enable)           |
| *Joystick*                  | *A1*                      | *VRx*                   | Horizontal movement input          |
|                               | *A0*                      | *VRy*                   | Vertical movement input            |
|                               | *D4*                      | *SW*                    | Button press detection             |
| *Buzzer*                    | *D3*                      | *(+)*                   | PWM signal for sound generation    |
| *Potentiometer (Contrast)*  | *-*                       | *VO (LCD)*              | Adjusts LCD screen contrast        |
| *LCD 16x2 (without I2C)*    | *D5*                      | *RS*                    | Register Select                    |
|                               | *D6*                      | *EN*                    | Enable Pin                         |
|                               | *D7*                      | *D4*                    | Data Pin 4                         |
|                               | *D8*                      | *D5*                    | Data Pin 5                         |
|                               | *D9*                      | *D6*                    | Data Pin 6                         |
|                               | *D10*                      | *D7*                    | Data Pin 7                         |
| *Breadboard and Jumper Wires| **-*                       | *-*                     | Electrical connections             |

##

##

### 6. Physical circuit

![photo1](https://github.com/user-attachments/assets/21958f99-fcc6-423c-8963-dca23168e600)

![photo2](https://github.com/user-attachments/assets/96250cb1-8123-4d5a-a576-413d7310a64a)



##
</details>

<details>
  <summary> <h2> Software Design </h2> </summary>

  ##
  ### Development enviroment:
  
  I will use the PlatformIO IDE extension.
  ##
  ##
 ### The libraries used in the code :
  - LedControl.h
    
This library is used to control the 8x8 LED matrix connected through the MAX7219 driver.

Why did I use this library?

1.It simplifies managing LED matrices.

2.It provides functions like setLed() and setRow() to easily turn LEDs on or off.

3.It allows us to adjust brightness with setIntensity() and clear the display with clearDisplay().

 - LiquidCrystal.h

This library is used to control an LCD display.

Why did I use this library?

To display game information such as score and menu on an LCD.

 - Arduino.h
   
   The core library that provides essential functions for the project.

##
</details>

<details>
  <summary> <h2> Results </h2> </summary>

  ##
   
  
##
</details>

<details>
  <summary> <h2> Conclusions </h2> </summary>

  ##
   
  
##
</details>

<details>
  <summary> <h2> Resources </h2> </summary>
  
  ##

 
  
##
</details>
