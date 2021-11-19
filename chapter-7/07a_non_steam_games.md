# 07a: Adding Non Steam Games to Steam

In order for Steam’s controller configuration to work, the Steam Overlay needs to hook into the game. This means if you are launching a game from elsewhere, as is often the case with Non Steam games, Steam cannot hook the overlay.

The easiest solution in this case is to simply add the game to your Steam library so you can launch from Steam. This gives Steam the opportunity to hook into the game and provide its overlay, which for the most part will allow Steam's controller configuration to work with that game.

Adding a Non Steam game to Steam is actually rather simple:

* Click on “Add A Game” found in the lower left of the Steam clients window
* Select “Add A Non Steam Game”
* Steam will do a quick scan of programs you have installed
  * If the game you wish to add is not in that list, click on “Browse…” and navigate to where the game is installed
* Check the box next to each program you wish to add to Steam
* Once you have selected all the games or programs you wish to add to Steam, click on “Add Selected Programs”
* Those games or programs should now appear in your Steam library list.
  * If you later wish to remove a non Steam game from Steam, right click on it in your library, hover over “manage”, then select “remove non-Steam game from your library”

Now when you launch that game from Steam, Steam should hook its overlay into the game and thus allow you to use Steam’s controller configuration.

NOTE: If the game has implemented the Steam Input API (SIAPI) but you purchased the game elsewhere, the native configurations will not work and you will have to use the more basic configuration options. This is because SIAPI is a part of Steam and is therefore not present in non Steam versions of the game.
