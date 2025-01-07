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
  
The Snake game is probably the most intuitive and easy to play game in the world. Basically, the snake must eat as much food as possible without hitting itself. At the beginning of the game, as well as the first level, the snake starts small. As it eats, it grows, and along with it, the score increases. Naturally, the game also becomes more challenging.

<< TO BE CONTINUED >>

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
 
 ![bloc](https://github.com/user-attachments/assets/887bbad6-df21-460f-b99d-891bc86f7299)


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
