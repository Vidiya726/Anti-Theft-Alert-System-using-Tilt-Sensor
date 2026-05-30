# Anti-Theft-Alert-System-using-Tilt-Sensor

## Aim: To measure the tilt Sensor using SW200D with Arduino UNO Board/ESP-32 using Tinker CAD.

## Hardware / Software Tools required:
	PC/ Laptop with Internet connection
  Tinker CAD tool (Online)
	Arduino UNO Board/ESP-32
	Tilt sensor(SW200D)

## Circuit Diagram:
 
## Theory :
 The Arduino Uno is powered by the ATmega328P, an 8-bit microcontroller that runs at 16 MHz. It has 32 KB of flash memory, 2 KB of SRAM, and 1 KB of EEPROM. The board has 14 digital I/O pins (of which 6 can be used as PWM outputs) and 6 analog input pins. These pins allow the board to interface with various sensors, actuators, and other devices.The Arduino Uno can be powered via a USB connection or an external power supply. The board has a built-in voltage regulator to manage power from 7 to 12 volts.
The board is programmable using the Arduino IDE (Integrated Development Environment), which supports a simplified version of C/C++. The code, known as a "sketch," is uploaded to the board via a USB connection. The Uno has a USB-B port, which is used for communication with a computer. The USB connection also powers the board when connected. The board includes a reset button that restarts the microcontroller, useful during programming and troubleshooting. The In-Circuit Serial Programming (ICSP) header allows for low-level programming of the microcontroller or firmware updates. The Uno has a built-in LED on pin 13, commonly used for simple tests and debugging.


## Procedure:
### Step 1: Set Up the Tinkercad Environment

1. **Log in to Tinkercad**
   - Open Tinkercad in your web browser.
   - Log in to your account.

2. **Create a New Circuit**
   - In the Tinkercad dashboard, click **Circuits**.
   - Select **Create New Circuit**.

### Step 2: Add Components to the Circuit

1. **Arduino Uno**
   - Drag an Arduino Uno board from the components panel onto the workspace.

2. **SW200D Sensor**
   - Search for the SW200D sensor in the components panel.
   - Drag it into the workspace.

3. **Breadboard**
   - Drag a small breadboard into the workspace to help with wiring connections.

4. **Resistor (Optional)**
   - A resistor may not be necessary for this simple setup.
   - You may include one for more accurate readings.

5. **Wires**
   - Use wires to connect the components.

### Step 3: Connect the Tilt Sensor (SW200D) to Arduino

#### Sensor Connections

- **SW200D Vout (Middle Pin)** → Arduino Digital Pin **D2**
- **SW200D GND (One Side Pin)** → Breadboard **GND Rail**
- **SW200D VCC (Other Side Pin)** → Breadboard **5V Rail**

#### Breadboard Wiring

- Connect the **Vout (Middle Pin)** of the SW200D sensor to Arduino digital pin **D2**.
- Connect one side pin of the sensor to the breadboard **GND rail**.
- Connect the other side pin of the sensor to the breadboard **5V rail**.

### Step 4: Write the Arduino Code

1. Click the **Code** button at the top of the Tinkercad workspace.

2. Ensure the editor is in **Text Mode**.

3. Enter the Arduino code for the SW200D sensor.

### Step 5: Simulate the Circuit

1. Click **Start Simulation** to run the circuit and code.

2. Open the **Serial Monitor** to observe the sensor output.

### Step 6: Troubleshoot and Refine

1. Verify that all wiring connections are correct.

2. Modify the code if necessary to improve accuracy or change the output format.

### Step 7: Save Your Work

1. Click **Stop Simulation** to end the simulation.

2. Click **Save** to store the circuit design and code for future use.

## Code:
```
int ledPin = 13;
int inPin = 7;

void setup()
{
    Serial.begin(9600);

    pinMode(ledPin, OUTPUT);
    pinMode(inPin, INPUT);
}

void loop()
{
    int val = digitalRead(inPin);

    if (val == 0)
    {
        digitalWrite(ledPin, HIGH);
    }
    else
    {
        digitalWrite(ledPin, LOW);
    }
}
```
## Output:
<img width="1035" height="761" alt="Screenshot 2026-05-30 135245" src="https://github.com/user-attachments/assets/59ecf89d-ed7f-40a9-8c60-1888827d7895" />

## Result:
Thus measure the Tilt Sensor using SW200D with Arduino UNO Board/ESP-32 using Tinker CAD has been Verified Successfully.

