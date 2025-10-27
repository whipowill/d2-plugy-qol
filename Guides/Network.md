# D2QOL | Network

PlugY disables Battle.net options in the game as a protective measure against getting your CD keys banned.  The only remaining networking option for PlugY players is to host and join our own ``TCP/IP`` games.

The easiest way to get this working is to use [ZeroTier](https://docs.zerotier.com/zerotier/ztintro).  This method avoids the pitfalls of port forwarding and the other networking problems that often plague ``TCP/IP`` games.  All you have to do is install and connect to the ZeroTier network and everything will work, regardless of your router configuration.

## Setup

- Create A [ZeroTier](https://my.zerotier.com/) account.
	- Create a new network.
	- Note the network ID to give to your friends.
	- As your buddies join, click the wrench icon next to their IDs and mark ``Allow Ethernet Bridge``.
- Install [ZeroTier](https://www.zerotier.com/download/) on your computer.
	- Click ``Join Network``.
	- Join the network ID of the network you created w/ default checkbox options.
	- This adds you to a virtual LAN network where all the computers are connected.
	- Windows will give you a prompt about sharing over the network, approve that request.
		- If you screw this up you won't be able to host a game, but reconnecting to ZeroTier will fix it.
- Open up Diablo II.
	- Select ``Other Multiplayer``.
	- Select ``TCP/IP Game``.
	- Note the IP address.
	- Give your friends that IP address.
	- Create your game and wait for others to join.

## Requirements

- Players must be Softcore or Hardcore to match the host.
- Players must have access to the difficulty level of the host's game (Normal, Nightmare, Hell).
- Players must be running the same soft mods, specifically the ``C:\Games\Diablo II\Data\Global\Excel\`` folder.

## Issues

- You can inspect other players using MapHack by hovering your mouse over the player and hitting ``0``.