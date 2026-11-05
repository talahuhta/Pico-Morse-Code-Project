# Pico-Morse-Code-Project

RTOS pico morse code project

## EVERYTHING MUST BE DONE 3 DAYS BEFORE NOVEMBER 22nd
To/do:
- Email about project plan
- Write this week's diary (and check if there was meant to be one last week)
- Install VM and get pico running (Taneli) (this weekend)
- Clean up main
- Get Sam up to speed (EVERYONE MUST KNOW WHY WE MAKE THE DECISIONS WE MAKE AND WHAT THE IMPLEMENTATION IS AND HOW IT WORKS)
- Split up work
- determine helper function, global variables, and expand on implementation needed for tasks

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
### Main
- Init everything
- create tasks
- start scheduler
- handle task exceptions
- define interrupts
### Receiving from Workstation to Pico
#### Input Stage (Workstation)
- Pico does nothing
- Serial asks for input from user
- Once input entered:
  - Check validity (Exceptions give an error and ask for new input)
  - Translate
  - Switch to read (buzz to indicate change)
#### Reading Stage (Pico)
- Start displaying when button 2 is pressed (first character is space)
- Display morse code one symbol at a time
  - On the LED
- Button 2 will scroll to the next symbol
- Space denominates new char
- Once it reaches the end, it buzzes (pressing button 2 will restart message)
- Switch program state with Button 1
### Sending from Pico to Workstation
- Print to the Serial Monitor that the Pico is now ready to send
- Pico
  - Button 2 pressed
    - Check orientation and return corresponding symbol
    - Collect symbol in buffer
    - When receive 'space' translate char and print to serial
      - Translate function returns error if not real char
      - Empty symbol array = space
    - When Button 1 is pressed
      - Send final message
      - Switch state
  #### Send Message Format (Only if newline print):
  "Receiving from Pico"
  - "A"
  - "B"
  - " "
  - "C"
  - "Message "AB C""
## File structure
## Course deliverables
- Personal weekly diary
- Video
- In person meeting/presentation
- Returning device
