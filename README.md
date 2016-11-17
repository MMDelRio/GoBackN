# GoBackN
Error control with protocol Go Back N

This program use UDP segment as an underlying unreliable channel and put your protocol data unit (including header and payload) in the payload of the UDP segment. 
To simulate the packet loss use pseudo random number to control that.
  First the program ask the user to input a number between [0, 99]. This number means the percentage of packet losses will happen in the transmission. 
  Then each time before your send your protocol data unit, your program will generate a pseudo random number in the range [0, 99] with the random seed set to the current system time. If the random number generated is less than the user input number then the current protocol data unit won’t be sent to simulate a packet loss. 
This protocol doesn’t consider error-detection and error-correction.
