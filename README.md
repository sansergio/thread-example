# thread-example
Thread example for the DSCAE class at ITESO

* __myHeater_BR__ folder contains a Border Router based project. It simulates a fish tank heater. When a target temperature is set, it turns on its heater (Prints a "Heater On" message on the console) until the set temperature is reached then turns Off the heater (Prints a "Heater Off" message on the console). If the temperature drops bellow the set then it turns On the heater again and starts over. The Heater uses Thread to read the fish tank's water temperature from a Thread enabled temperature sensor. Coap properties which can be read/written:
    * /settemp - Trigger temperature, if the value gets set to 0 it turns off the temperature sampling and water heater.


* __myTempSensor_REED__ folder contains a Router eligible device based project. It simulates a fish tank's temperature sensor connected to a Thread network. Coap properties which can be read/written:
    * /temp - Measured temperature, it is calculated (simulated) every second, the temperature goes from 10C to 40C in 30 seconds and then back to 10C in the same time.

__Note:__ Use the "setdest" command on the Heater's shell to set the Unique local address (ULA) of the temp sensor as the destination address for CoAP commands.