 Home assistant code for taming an EvoHome controller in case of an hybrid heatpump. Evohome will send a much higer heatrequest to the heatpump controller, which will result in a boiler assist where this is not always necessary. 
Configuration cotains:
switch:
climate:
input_datetime:
  evo_aangeroepen:

input_number:
  woonkamer_man_temp:
  delta_woonkamer:
