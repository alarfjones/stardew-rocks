# stardew-rocks

Stardew Rocks is a tool for Stardew Valley that sends saved games to a distributed queue of mod developers! 

Developers can watch that queue and do cool things with the saved files.

For example:
- write cool web apps showing what people are doing
- analyze the most efficient players
- host a Stardew Valley tourney: see who get a certain amount of resources faster without cheating!

# For Farmers

You can install the Stardew Rocks client and help the community!

 - [Download Stardew Rocks!](https://github.com/nictuku/stardew-rocks/releases/download/v0.3/stardew_rocks.exe)

Just download the .exe file and run it. Once running it will look a bit like this:

![Screenshot](client/screenshot.jpg)

Please leave this window open in the background while you're playing Stardew Valley. You can minimize it, but don't close it. 
This will allow mod developers to see whenever your save file changes. Hopefully they will build very cool stuff with that!


*WARNING*: _Stardew Rocks_ doesn't ever write to files on your computer, but there may be a risk of crashing StardewValley when it tries to save a game. That can make you lose a day of your SDV work. If that happens, please notify the _Stardew Rocks_ developers. We don't want it to happen to anybody else!

# For Developers

The ampq URL is: `amqp://guest:guest@amqp.stardew.rocks:5672/`

We currently publish the following exchanges:

 - "SaveGameInfo-1" receives raw uncompressed XML files with contributors' SaveGameInfo.
 - "OtherFiles-1" receives raw uncompressed XML files with the super-large file saves.
 
To show off what we can do, I've built a simple farm map generator that creates simple images whenever someone pushes a new game save. For example:

![Farm Map](subscriber/map-000000001.png)

For now it only shows wild plants vs planted ones. It will look prettier, eventually, I promise :-).
 
# Planned features

- Authentication of some fashion
- Prettier farm maps
- A slick website showing people's farms!