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
##
### The laboratories used:
 - Lab 2: Interrupts. Timers
   
The game uses default timers to control the snake's movement update and to introduce precise delays.
The delay() functions and joystick reading (analogRead()) are synchronized with the game's execution times.

 -  Lab 3: PWM (Pulse Width Modulation)

The buzzer uses PWM to generate sounds at the beginning of the game, when eating food, and at the end of the game.
The tone() function uses PWM to control the frequency and duration of the sounds.

 -   Lab 4: ADC (Analog-to-Digital Converter)
    
 ADC is used to read the joystick's position.

 -    Lab 5: SPI (Serial Peripheral Interface)
    
 SPI is used to control the LED matrix.
##


</details>

<details>
  <summary> <h2> Results </h2> </summary>

  ##
   https://youtube.com/shorts/yoB0ctfPKP4?si=JwMzrzmz2Dtp2j4v
  
##
</details>

<details>
  <summary><h2> The functionality of the game </h2> </summary>
   1. Game Menu:
  
The game starts with a menu system displayed on the LCD screen.
The menu has 3 options:
- Start Game – Begin the Snake game.
- Leaderboard – View the top 5 player scores.
- Settings – Adjust game settings (e.g., sound ON/OFF).
- Joystick is used to navigate through the menu, and the button selects an option.
  
 2. Snake Movement:
  
The snake moves on the 8x8 LED matrix.
The joystick controls the direction:

- Up (Y-axis)
- Down (Y-axis)
- Left (X-axis)
- Right (X-axis)

 3. Food Generation:
    
- Random food appears on the matrix.

When the snake eats the food:
- The snake grows longer.
- The score increases by 1.
- A sound effect is played via the buzzer.
  
 4. Collision Detection:
  
The game ends if:
- The snake's head touches its own body.
- The snake moves off the matrix boundaries (handled by wrapping around the matrix).
  
 5. Score Display:
  
- The current score is shown on the LCD screen.
- The score updates in real-time as the snake eats food.
  
 6. Game Over & Restart:
    
When the snake dies:

- A sad face is displayed on the LED matrix.
- The game shows "Game Over!" on the LCD.
- The player can restart the game by pressing the joystick button.
  
 7. Sound Effects (Buzzer):
    
- Sound at game start.
- Sound when the snake eats food.
- Sound at game over.
  
 8. Leaderboard:

- After the game ends, the player's score is saved on a leaderboard.
- The leaderboard shows top 5 scores along with player names ("Player 1", "Player 2", etc.).
- If the current score is higher than one of the top scores, it replaces the lowest score.
  
 9. Smiley and Sad Faces:
     
- Smiley face appears on the LED matrix at the start of the game.
- Sad face appears when the game ends.
  
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

 https://github.com/Circuit-Digest/Components101/blob/main/MAX7219_Interfacing.ino
  
##
</details>
