# noCORE
A noCORE - the smallest possible ARDUINO core to use ARDUINO Shell with ATmega 328. 
No useless pheripheral code. Just only to start and some defines. 
Can be useful when you want to communicate with your ATmega via registers but want to use ARDUINO with its compiler and bootloader (they are rather good).
Can be a good joke for your friend which does not want to learn the uc architecture and write or copy sketches with all its retarded shit.
Just delete everything from \hardware\arduino\avr\cores\arduino and put there my files.

Now you can only write this:
    DDRD |= (1 << PB5);
    PORTD &= ~(1 << PB5);
But not:  
    pinMode (LED, OUTPUT);                            

And this for blinking:
     PORTD |= (1 << PB5);    
     _delay_ms(500);     
     PORTD &= ~(1 << PB5); 
     _delay_ms(500);   
   
 Advice - learn how to operate correct, incorrect can be without you)))
