# Taming EvoHome with Home Assistant
Home assistant code for taming an EvoHome controller in case of an hybrid heatpump. Evohome will send a much higer heatrequest to the heatpump controller, which will result in a boiler assist where this is not always necessary. 
 
Configuration contains:
- switch:
- climate:
- input_datetime:
  - evo_aangeroepen: used to limit the numer of calls to Evohome, to avoid being blocked. 
- input_number:
  - woonkamer_man_temp:
  - delta_woonkamer:

**'schedue automation'** contains the schedule for one EvoHome zone. In this schedule an outdoor thermometer is used as a device. For the scheme to work you should change it to an outdoor temperature sensor available in your own system. You can change the schedule by adding or removing setpoints and changing the delta_temperature variables. 

**'schedule automation v2'** This is the second version of the scheme. It mainly follows the EvoHome schedule, but mute the increases of the targeted temperature by using the delta variable. When the setpoint temperature is reached, 'real thermostat' returns the control to EvoHome. 

**'real thermostat'** automation contains the code to regulate the real thermostat for one EvoHome zone.
