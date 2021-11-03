# 06a01: Rating System for SIAPI Implementations in Games

This chapter will focus on developing a system to rate how well a developer has done implementing SIAPI into their games. This is NOT meant to disparage any developers, but rather encourage developers to check out what their peers are doing and improve their own work based on player feedback. While some SIAPI implementations are really in depth, others are simple. What matters most is the player experience, so this rating system will strive to be fair to both types of implementations.

As such, each game will start with the same score which will then be adjusted based on a number of factors.

Those factors will be divided into categories, to better organize how games will be rated.

## The Categories

* Is the game playable when SIAPI is being used? (auto lowest rating if “No” at any point, regardless of final percentage score; game should be completely playable with a controller using only the siapi config)
  * Across all major controllers?

* Action Sets, if being used: (main category, up to 33 points. If Action Sets are not being used then game is ineligible for Platinum or Diamond ratings despite final score.)
  * Are they clearly named/labelled so the player knows when they should be active and where to make customizations if they desire? (-1 point per)
  * Is there a Set for every game context? (-% of points)
  * Are there any frivolous Sets? (-% of points)
  * Does the auto swapping work correctly (doesn't fail to switch/gets stuck)? (auto 0 for this category)

* Bindable Actions: (main category, up to 33 points)
  * Are they clearly named/labelled so the player can easily read the configuration and know what to do if they want to make customizations? (-1 point per)
  * Have technical parity with other input systems? (-% of points based on Actions missing; typing in an in game chat window doesnt count as Steam does have an OSK for parity in that situation)
  * Are there any actions that are doubled up that aren’t intrinsically coupled? Ie “Reload/Use” as a single action instead of 2 separate “Reload” and “Use” actions(-x points per coupling, where x is number of actions in that couple)
[ Developers: Steam Input supports stacking multiple actions on one button using multiple activators! You can still create default controller configs that adhere to this ‘standard’ style of contextual use, but you need to make the actions separate so the player can rearrange them to their needs! ]
  * Any Actions work in other input systems, but don't work in SIAPI? (-% of points, based on how many work versus dont work)
  * Have redundant/deprecated Actions? (-% of points based on number of Actions)

* Bindable Input Styles: (main category, up to 34 points)
  * Are they clearly named/labelled so the player can easily read the configuration and know what to do if they want to make customizations? (-1 point per)
  * Is there an “absolute_mouse” style for touchpad or gyro users alongside the more traditional analog joystick styles? (-10 points if missing)
   * If not, is “mixed input” supported? See chapter 02c for more information on mixed input (+x points back, up to 8, based on mixed input rating)
  * Unnecessarily define things that should be bindable Actions (ie firing a gun) as trigger styles? (-1 per Style that should be an Action)
  * Any Styles that work in other input systems, but don't work in SIAPI? (-% of points, based on how many work versus dont work)

* Are there any other outstanding issues? (-x points to overall score, based on severity of its impact to the experience)
  * Are there frame rate issues when using SIAPI? -10
  * Are auto Action Layers being used? I know the Valve doc says that it's okay to use them in place of Sets on occasion, but doing so removes a powerful customization option from the player which is NOT good. -10 for me
   * This is admittedly subjective. It would be fine if steam input had multi-modeshifting IMO
  * Inputs are unnecessarily hard coded a certain way (IE Horizon Zero Dawn’s treatment of the steam controllers left touch pad) -10
  * Does the game display the proper controller glyphs for button prompts? This includes:
   * Controller type
   * Updating the prompts to match the config
   * issues related to mixed input not accounted for in the Input Styles category

* Are there any special features/game mechanics thanks to SIAPI? (+x points to the overall score, based on how awesome those features are)
  * IE: Motion Soothing BB in Death Stranding is to me a +5.
   * However if this interfered with using the gyro as a mouse (it doesn't, thankfully) then it would be neutral
  * CS:GO also has customized haptics per gun type. +5

## Once a final score has been reached, the game will be given a rating:

* Copper (69 or less)
  * This rating is reserved for implementations that are either unplayable when using SIAPI or lacking so much it's a poor experience. It would be amazing to see devs of these games have another go at it, and come back with something awesome. I believe in you devs!

* Silver (70 - 79)
  * This rating means the game is playable, but there are a number of issues. I would encourage devs of these games to keep going! You are on the right track, just have to make some adjustments.

* Gold (80 - 89)
  * This rating means the game plays really well with SIAPI, having only a few issues. Good job devs! After a celebration, please consider fixing the last few issues.

* Platinum (90 - 99 points)
  * This rating denotes games that have basically flawless SIAPI implementations. Very well done indeed! Devs with games at lower ratings take notes, and strive to reach this rating.

* Diamond (100 or more points)
  * This rating is for SIAPI implementations that are truly special. They are not only basically flawless as far as standard controls go, but they go above and beyond with special features that are only possible thanks to implementing SIAPI. Devs of these games should feel seriously accomplished.
