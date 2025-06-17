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




