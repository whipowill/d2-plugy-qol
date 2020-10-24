# D2QOL | Network

PlugY disables Battle.net options in the game as a protective measure against getting your CD keys banned.  The only remaining networking option for PlugY players is to host and join our own ``TCP/IP`` games.

To facilitate this, I've created a ZeroTier network for D2 players that allows us to share a local network and easily join each others games.  This method avoids the pitfalls of port forwarding and the other networking problems that often plague ``TCP/IP`` games.  All you have to do is install and connect to the ZeroTier network and everything will work, regardless of your router configuration.

## Setup

- Install [ZeroTier](https://www.zerotier.com/download/) on your computer.
- Click ``Join Network``.
	- Join the network ID ``a84ac5c10a96e28d`` w/ default checkbox options.
	- This adds you to a LAN where everyone has the same IP, except for the last sequence of digits: ``192.168.192.xxx``
	- Windows will give you a prompt about sharing over the network, approve that request.
		- If you screw this up you won't be able to host a game, but reconnecting to ZeroTier will fix it.
- Open up Diablo II.
	- Select ``Other Multiplayer``.
	- Select ``TCP/IP Game``.
- If you are hosting:
	- Note the last set of digits in your IP address: ``192.168.192.xxx``
	- Give your friends that last set of numbers, which will be easily memorizable.
	- Create your game and wait for others to join.
- If you are joining:
	- Get the last set of digits from the host's IP address: ``192.168.192.xxx``
	- Connect to the host's IP address.
	- Play the game and have fun!

## Requirements

- Players must be Softcore or Hardcore to match the host.
- Players must have access to the difficulty level of the host's game (Normal, Nightmare, Hell).
- Players must be running the same mods, specifically the ``data/`` folder.

## Issues

- You can inspect other players using MapHack by hovering your mouse over the player and hitting ``0``, but at the moment this is causing an fatal error.  I will update this guide when I figure out what the problem is.