# CONNECT ESP32 TO ARDUINO

### Programming Environments:
Arduino IDE: https://randomnerdtutorials.com/projects-esp32/

### Preparing the ESP32 Board in Arduino IDE:
Windows: https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-windows-instructions/
### Steps: 
1- Plug the ESP32 to your PC or laptob by using micro cable.\
2- Copy the following link : https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json \
3- Open arduino ide > file > preferences > paste the link from step 2 in "Additional Boards Manager URLS" > OK.\
4- Go to Tools > Board > Boards Manager > from the search bar write "esp32" > click on install.\
5- Go to Tools > Board >  select the name of your ESP32 board.\
6- Go to Tools > Port and select a COM port available.\
5- write the following code in arduion editor :

```js
/*
  Blink
*/

// ledPin refers to ESP32 GPIO 23
const int ledPin = 23;

// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin ledPin as an output.
  pinMode(ledPin, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(ledPin, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);                  // wait for a second
  digitalWrite(ledPin, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);                  // wait for a second
}
```
#### Important: always check the pinout for your specific board before building any circuit.
6- Press the upload button.
