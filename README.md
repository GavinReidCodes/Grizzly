# Grizzly - Advanced 1.8-1.21 Anti-Cheat
## About
Grizzly is a modified version of Grim, made to serve as an alternative for those who can't afford Polar or Intave. The goal of this project is to detect and mitigate 99% of cheaters in a matter of seconds.

## Requirements and Supported Plugins
This anti-cheat supports Spigot based server softwares ranging from version 1.8.X to 1.21.X. If you are using ProtocolLib, ensure that the version is 5.0.0 or higher. 

## Features
### Movement Simulation Engine
Grizzly uses a movement simulation engine to mitigate almost every movement cheat. Here is how it works:

- Player sends a movement packet to the server.

- Grizzly uses the player's data to predict where the player will be next. This is done by simulating what the vanilla Minecraft movement code would do.

- The predicted position is then compared to the position in the movement packet. If they don't match up, they are likely using movement cheats of some sort.

### Lag Compensation System
This anti-cheat also has an entire lag compensation system, which is used for each check. Here is what we do exactly to achieve this:

- Grizzly creates a compressed version of the world using packets. This ensures that ghost blocks and block glitching along with other lag-related issues don't cause players to be falsely mitigated or punished.

- Grizzly also keeps track of the inventory to reduce lag-related false flags.

- Transaction packets are used to their full advantage in Grizzly, making sure that checks compensate players based on their latency.

### Cheat Mitigation System
Similar to Polar (and maybe Intave), Grizzly focuses on preventing cheats as opposed to banning or kicking players for (possibly) using them. By doing setbacks, reducing outgoing damage, damage speed and such, we can ensure that cheaters don't get an advantage while keeping bans or kicks to a minimum due to potential false flags.

### Cloud Checks
Grizzly runs some of it's checks in our backend. Here's why:

- It helps improve performance on your server slightly by doing intensive calculations on our backend.

- It also makes it harder for the checks to be bypassed while mainly keeping everything open-source.

