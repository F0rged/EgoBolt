# EgoBolt
Ego Battery Adapter for Jetson Bolt Pro

Background:
I have always liked the idea of going for family bike rides.  Unfortunately, my daughter (8 years old) was never very enthusastic about the idea and was generally quite resistant to the idea whenever the suggestion would come up.
I thought, maybe if I could build her an electric bike, she might be more ethusiastic.
Unfortunately, there don't seem to be many kid-friendly e-bikes out there.
Except for one: the jetson bolt Pro.
I picked up a used one in good shape for about $250CAD, and it worked well.
But of course, the battery is nearing the end of its life and the charge doesnt last as long as it should.
Therefore, a new battery is required.
Meanwhile, I have amassed an array of Ego tools over the years, each of which included its own 56V battery.
These should be a good fit for an ebike.  All that should be needed is to drop the voltage, add a fuse, and a low voltage protection circuit.
The Ego 4ah or higher should be roughly equivalent to the factory bolt battery in terms of watt hours.

Bolt Pro Factory Battery Specifications:
Based on some googling, I came to the conclusion that the factory battery has the below properties:
Power: 36V / 6AH = 214wh
Continuous Discharge: 20 Amp
Max Charge Current: 3 Amp
Connector Type: Razor Factory 4 Pin

Ego Battery Cell Specifications:
Count: 14 (in series)
Type: 18650
-	12ah: Samsung 30Q (3000mah nominal discharge)
Nominal Voltage: 3.7
Max Voltage: 4.15
Max Current: 20A (may be higher for bigger batteries, but 20A to be safe)
Power:
-	2.5ah = 126wh
-	4.0 ah = 202wh
-	5.0 ah = 252wh
-	7.5 ah = 378wh

Ego Battery Pack Voltage:
Nominal:56V
(4v x 14s = 56v)
Max: 58.8V
(4.2 x 14s = 58.8V)

Ego Battery Terminals:
+ = Positive
T = Temperature
D = Data
- = Negative


Battery Adapter Device Requirements:
-	On/Off Switch 
(to protect from potential parasitic battery drain)
-	Low Voltage Cutoff @ 43.5V
(must be enforced by the tool. The battery doesn’t have this built in.)
-	Replaceable Fuse @ 20A
- DC-DC Converter (Drop 52v down to 36v)

Approach:
Since each tool also came with an extra charger that I dont need, I thought the simplest approach (at least for now) would be to just adapt a spare charger into the case for my new DC-DC inverter.
The device just needs to drop the voltage down from teh Ego 52-56V to the 36V that the bolt expects.
Then we just need a low voltage cut off (to protect the battery from being over-discharged) and a fuse.

Bill of Materials (BOM):
- (1) DC-DC Converter
DROK CNC DC Buck Converter with Meter, 6-70V to 0-60V 20A 1200W
Model FBA200707
https://www.amazon.ca/dp/B0CNVWC66L?ref_=pe_125682630_1045605200_t_fed_asin_title&th=1
- (1) Low Voltage Cutoff circuit
  MgcSTEM Low Voltage Disconnect and Charging Discharging Protection 2 IN 1 40A DC 5V-60V Low Voltage Cutoff with LCD Display Low Voltage Protector Disconnect Switch Module Charging Discharging Protection Board
Model 7f97e121-c03e-4f22-97e6-13224b8cd3e9
https://www.amazon.ca/dp/B0C2VMGCZR?ref_=pe_125682630_1045605200_t_fed_asin_title
- (1) Fuse (20a)
- (1) Button (to power on DC-DC converter)
- (1) Switch (Power On/Off - to stop the DCDC converter when you get off the bike.)
- (1) Charger Case
- (1) Locking Mechanism (3d printed)
- (1) Electronics mount/tray (3d printed)
- (2) Springs for locking mechanism
