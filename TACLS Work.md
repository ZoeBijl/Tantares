# TAC LS Work

Notes for TAC LS work.

## Parts that don’t have TAC LS by default (meaning, via TAC LS itself)


## MIR Parts

Station core and extensions that could use TAC LS resources.


MIR was almost continuously occupied for 9 years.
[Had 64 supply runs](https://www.history.nasa.gov/SP-4225/mir/mir.htm).
Should re-supply every quarter (9 / 64 = 0,14) or (426 / 4) 30 Kerbal days.
Which will be crap if you’re doing other missions.

Try to have supplies for a year.

- V-DOS-A (Core - Manned)
- V-DOS-B (Core - Manned)
- V-DOS-D (KVANT-1 - Manned)

## Progress Parts

- H-JT3 Habitation Module (Unmanned)
- H-E42 Control Block


## Forum post

I’m currently going through the list of parts to see what would make sense. I’ve assembled a bare bones MIR based on information from Wikipedia and the craft files by @CaptKordite. If I apply TAC’s base setting to all crewed parts this would get 22 days of life support for three kerbals; which is way to short if you want to time warp a mission to Duna for example (let alone any other body). So I’m trying to get it up to about a year / 426 days for the fully assembled MIR with four kerbals (for example: two scientist to science and two pilots in case you need to evacuate).

Given that V-DOS-A "Rotund" Crew Block is the main part of MIR it makes sense to me to equip this with fairly generous values. Values for V-DOS-A I’m testing with:

- Food: 452.8
- Water: 299.2
- Oxygen: 45867
- Waste: 41
- Waste Water: 380.60
- Carbon Dioxide: 39558.5

This is equal to: 4⨉ 1.25m Supplies Container, 2⨉ 1.25m Waste Container, 1⨉ 0.625m Waste Container. The mass of the supplies is automatically added to the V-DOS-A; which has a wet mass (food, water, oxygen included) of 3.295 tons (dry mass is 2.8 tons). This gives the MIR core 313 days with a crew of 4.

For the A-NXL Docking & Command Module (main part for the KVANT-2, Kristall, Spektre, and Priroda modules) the values are as follows:

- Food: 30.65
- Water: 20.25
- Oxygen: 3105.6
- Waste: 2.625
- Waste Water: 24.5
- Carbon Dioxide: 2545.85

This is equal to: .5⨉ 1.5m HexCan Supplies and .25⨉ 1.5m HexCan Waste. Again, the mass is automatically added to the A-NXL which now has a wet mass of 1.933 tons (dry mass is 1.9 tons).

With these two upgrades a completed MIR with four kerbals gives you around between 400 and 410 days of life support.

Since @Beale already made a config for USI (thanks for the comments in that) I’m looking to make a direct port of those values to see how well that works. Reason for my initial approach was to figure out TAC code and keep it stupid simple; having 4-5 parts to empty and refuel is a lot easier than having to go through all the different parts.
