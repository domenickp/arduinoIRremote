// https://github.com/Arduino-IRremote/Arduino-IRremote

#include <IRremote.hpp>  //including infrared remote header file

int IR_RECEIVE_PIN = 7;  // the pin where you connect the output pin of IR sensor

void setup() {
    Serial.begin(9600);
    IrReceiver.begin(IR_RECEIVE_PIN, ENABLE_LED_FEEDBACK); // Start the receiver
}

void loop() {
    if (IrReceiver.decode()) {
        Serial.println(" ");
        Serial.println(IrReceiver.decodedIRData.decodedRawData, HEX);
        IrReceiver.printIRResultShort(&Serial);
        Serial.println(" ");
        IrReceiver.resume();  // Restart the ISR state machine and Receive the next value
    }
}
