
# Thrusters
There are 3 kinds of thrusters - glowstone, plasma, and ion.

## Thruster Types
### Glowstone
- Built literally with just a glowstone block.
- Worst thruster ovrerall, but use less power and space.
- Best for super small/cheap ships.
- Acceleration 0.2, speed 1.75

![Glowstone]

### Plasma
- Built with a redstone block and a redstone lamp behind it.
- The lamp should face away from your ship.
- Best for most ships.
- Very fast acceleration and almost as fast speed. 
- Acceleration 0.75, speed 2.0

![Plasma]

### Ion 
- Built with a sponge block and a sea lantern behind it.
- The lantern should face away from your ship.
- Best for largest ships
- High power demand, very low acceleration.
- Acceleration 0.05, speed 2.75

![Ion]

## Tips
- You cannot have any blocks behind thrusters or they don't work.
- Having walls of thrusters uses too much of your ship's power.

## Under the hood
The actual equation for thruster acceleration is:
`log(2 + totalAcceleration) / (log(mass) / log(thrusterAmount + 2))`

The function for speed is: 
```
Base Speed:
y = base speed
x = total thruster combined power
m = mass
F = 200
y = x^0.4 / m^0.3 * F

Max Speed:
a = max speed
p = starship power output
x = total thruster combined power
a = p/x

Actual BPS = min(a, y)
```

[Glowstone]: https://i.imgur.com/QtsjFnN.png
[Plasma]: https://i.imgur.com/da4g1Pr.png
[Ion]: https://i.imgur.com/zSYwLRE.png
