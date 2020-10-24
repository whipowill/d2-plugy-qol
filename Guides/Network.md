# D2QOL | Network

PlugY disables Battle.net options in the game as a protective measure against getting your CD keys banned.

The only remaining networking option for PlugY players is to host and join our own ``TCP/IP`` games.  To facilitate this, I've created a ZeroTier network that allows us to share a local network and easily join each others games.

## Setup

- Install [ZeroTier](https://www.zerotier.com/download/) on your computer.
- Click ``Join Network``.
	- Join the network ID ``a84ac5c10a96e28d`` w/ default checkbox options.
	- This adds you to a LAN where everyone has the same IP, except for the last sequence of digits: ``192.168.192.xxx``
	- Windows will give you a prompt about sharing over the network, approve that request.
		- If you screw this up you won't be able to host a game, but just disconnecting from ZeroTier and reconnecting will fix it.
- Open up Diablo II.
	- Select ``Other Multiplayer``.
	- Select ``TCP/IP Game``.
- If you are hosting:
	- Note the last set of digits of your IP address: ``192.168.192.xxx``
	- Give your friends that last set of numbers, which will be easily memorizable.
	- Create your game and wait for others to join.
- If you are joining:
	- Get the last set of digits from the host's IP address: ``192.168.192.xxx``
	- Connect the host's IP address.
	- Play the game and have fun!

## Issues

- Players must be Softcore or Hardcore to match the host.
- Players must have access to the difficulty level of the host's game (Normal, Nightmare, Hell).
- Players must be running the same mods.

## Tips

You can inspect other players using MapHack by hovering your mouse over the player and hitting ``0``, but at the moment this is causing an error.  I will update this guide when I figure out what the problem is.