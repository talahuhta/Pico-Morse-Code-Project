# Pico-Morse-Code-Project

RTOS pico morse code project

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
