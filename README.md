# freeze_dry
Software to control a freeze drier.

Tasks
1) Outline components and develop initial software
   a) Controle Components
      1) Freezer
      2) Heater
      3) Pump
      4) Auto drain (future add on?)
   b) Inputs
      1) Room temperature sensor
      2) Tray temperature sensor
      3) Humidity sensor(s)?
   c) WiFi control
   d) Logging
   e) Android App?
2) Indentify hardware components and control mechanisms
   a) temp sensor brand/protocol
   b) relay should hopefully be controllable by 5v signal
3) Hardware to use
   a) Rasp. Pi with WiFi
     i) if nothing real-time needed this is a good choice; a base pi should be sufficient, perhaps a 3 or 4 for increased future features
   b) LCD (or just app/web interface to start?)
   c) Electronic valve for auto drain?
4) Choosing language
  a) C++
  b) Python
  
Analysis of HR FD
1) Believe it is using ARM from reviewing FW images, someone said they thought it was a Pi, but pictures I've seen look custom.
2) Need measurements internally, goal to  "replace" LCD and controller.  Relay and all other hardware to remain the same.  
3) States of freeze drying
   a) Freeze
   b) Freeze + loaded + drain closed 
      Once cold enough use can move to this state
   c) Freeze + vacuum
      Ensuring items are frozen and cold enough.  Does this use tray temperature sensors to know when we're ready?  
   d) drying
      How does machine determine we're dry enough?  Is it based on tray temperature?  Room temperature and formula?  Other sensors to give idea?  Pressure?
   e) extra drying
      When machine thinks we're done
