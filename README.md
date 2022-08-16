# brushless:
 brushless control circuit using arduino

# Circle:
#### use controller, This controller is called ESC (Electronic Speed Controller). This controller’s main responsibility is to properly supply power to the BLDC motor wires so that the motor rotates in the correct direction

 1. The ESC controller needs a power supply with 12V and at least 5A current.  use a Li-Po battery ,The three phases (wires) of the BLDC motor must be connected to the three output wires of the ESC controller 
 
 2. The BEC (Battery Eliminator circuit) in the ESC controller will provide (regulate) a +5V DC voltage on its own so that it can be used directly to power the Arduino board
 
3. use a potentiometer connected to pin A0 of the Arduino board to control the motor’s speed 

# code:

>#include <Servo.h> //use the servo library to generate the PWM signal
Servo ESC; //name our servo object. In our case, it will be the name of ESC
void setup()
{
ESC.attach(9); //"attach" the ESC controller to pin 9 of the Arduino board
}
void loop()
{
int throttle = analogRead(A0); //read voltage from the potentiometer output
throttle = map(throttle, 0, 1023, 0, 180); //convert the values from the range 0-1023 from the ADC output into the range 0-180 because servomotors can only operate in the range 0-180
ESC.write(throttle); //generate PWM signal with necessary filling ratio
}

