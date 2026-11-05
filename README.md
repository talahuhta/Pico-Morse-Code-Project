# Pico-Morse-Code-Project

RTOS pico morse code project

## EVERYTHING MUST BE DONE 3 DAYS BEFORE NOVEMBER 22nd
To/do:
- Determine specific functions needed
- Email about project plan
- Write this week's diary (and check if there was meant to be one last week)
- Install VM and get pico running (Taneli) (this weekend)
- Clean up main
- Get Sam up to speed (EVERYONE MUST KNOW WHY WE MAKE THE DECISIONS WE MAKE AND WHAT THE IMPLEMENTATION IS AND HOW IT WORKS)
- Split up work
- Determine code structure (What libraries, what are helper functions, what goes to main, what are the states, what are the tasks, what are gonna be global variables)

## Project Implementation
### Input (Pico)
- Assign rotations to inputs
- send inputs with button 2
- button 1 to switch modes
- in read mode use button 2 for scrolling (optional beep when done)
- clear cache upon switching states (for memory reasons)
### Input (Workstation)
- Input letters
- Function to translate into morse code
- Type into serial monitor and 'enter' to send
- limit input max length
- handle all exceptions before sending to pico and display an error to the user
### Output (Pico)
- LCD & LED display morse code
- LED long blink=dash, short blink=dot, no blink=space
- LCD (.,-,||  =  dot,dash,space)
- scroll through with button 2
- end word with beep noise
### Output (Workstation)
- Received code translated to letters
- Displayed on serial monitor in user friendly way

### Other project tasks
## Guidelines
## Code Structure
## File structure
## Course deliverables
- Personal weekly diary
- Video
- In person meeting/presentation
- Returning device
