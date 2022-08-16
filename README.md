# brushless:
 brushless control circuit using arduino

## Circle:
use controller, This controller is called ESC (Electronic Speed Controller). This controller’s main responsibility is to properly supply power to the BLDC motor wires so that the motor rotates in the correct direction

 The ESC controller needs a power supply with 12V and at least 5A current.  use a Li-Po battery ,The three phases (wires) of the BLDC motor must be connected to the three output wires of the ESC controller 
 
 The BEC (Battery Eliminator circuit) in the ESC controller will provide (regulate) a +5V DC voltage on its own so that it can be used directly to power the Arduino board
 
use a potentiometer connected to pin A0 of the Arduino board to control the motor’s speed 
