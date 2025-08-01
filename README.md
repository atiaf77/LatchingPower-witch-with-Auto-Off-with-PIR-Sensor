# LatchingPower-witch-with-Auto-Off-with-PIR-Sensor

📌 Overview
This project demonstrates a latching power switch circuit using a P-channel MOSFET.

The circuit turns ON when a push button is pressed and remains latched even after releasing the button.

It includes an Auto OFF feature, allowing a microcontroller (Arduino) to automatically cut off power after a specified time.

🛠️ Components
P-channel MOSFET (e.g., IRF9540)

NPN transistor (for latch control)

Push button

10kΩ and 100kΩ resistors

LED (for power status indication)

Arduino (for Auto OFF control)

Battery / Power source

⚡ Circuit Features
Manual Control: Push button toggles power ON.

Auto Power OFF: Arduino can send a LOW signal to cut power after a delay.

Low Power Consumption: MOSFET ensures minimal standby current.

Safe Power Switching: Ideal for battery-powered projects.

📝 How It Works
When the push button is pressed, the MOSFET gate is pulled low, turning the circuit ON.

A feedback path (via NPN transistor) keeps the MOSFET latched ON.

Arduino can pull the latch signal LOW to shut down the circuit automatically.

LED indicates when power is active.


💻 Arduino Code Example
cpp

const int latchPin = 5;

void setup() {
  pinMode(latchPin, OUTPUT);
  digitalWrite(latchPin, HIGH); // Keep power ON
  delay(10000);                 // Wait for 10 seconds
  digitalWrite(latchPin, LOW);  // Auto power OFF
}

void loop() {
  // You can re-enable power by setting latchPin HIGH again if needed
}
🚀 Usage
Assemble the circuit as shown in Tinkercad.

Upload the Arduino code to your microcontroller.

Press the button to power ON the device.

After the delay, Arduino cuts power automatically.

📜 License
This project is open-source and free to use under the MIT License.

