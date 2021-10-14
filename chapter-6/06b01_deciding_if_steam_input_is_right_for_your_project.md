# 06b01 Deciding if Steam Input is Right for Your Project

This chapter is not meant to downplay the value of Mixed Input to a side grade to Native Steam Input. Ideally developers would implement both to their projects. Failing that however we do suggest using the Input System that best suits your game.

Both approaches have value and if done incorrectly each one has massive caveats. The best advice we can say is regardless of how you choose to tackle making an enjoyable experience on Steam Hardware, please ensure that you're putting in the effort to make your handling of Input excellent.

Ultimately if you want your game to be a good experience on Steam Hardware and other Gyro-based types of controllers it is recommended to have support for either Mixed Input or Native Steam Input assuming your game can utilize or take advantage of either of them.

## How To Tell What Approach I Should Take With My Input System

Steam Input is a fairly robust Input API designed for a more modern era of gaming than that of XInput. Included in Steam Input are tools to allow for support for most current Controllers, control over low level Haptic functions in Controllers that support it, and automatic control over rendered Glyphs on a Controller or even Configuration level along with many other features. Although there is alot Steam Input can do for your project there are a few key reasons it may not fit well with your project.


- **A)** Small teams may not have the time or resources to invest in a good implementation of Steam Input. For Indies and budget titles it may be more reasonable to instead optimise your project to work well with Mixed Input and attempt to add niceties like support for Steam Hardware Glyphs and official configurations.

- **B)** Your game is too basic to make good use of a full implementation. Ultimately your team may decide to use a more simple API if your game is in a genre that truly only requires simple Button Configurations such as Platfromers and therefore only use a very small number of Inputs. If you decide not to add full native Steam Input, we’d suggest adding partial support instead to take advantage of features like automatic glyph switching, without the need to add and test complete support for the Steam Input API.

- **C)** You don't plan on targeting Steam as a platform, or don't plan on targeting Steam as the only platform. Steam Input API support is only available through the Steamworks SDK, which naturally means other launchers or game console targets will not be able to make use of that code. Teams distributing games through multiple channels may (understandably) not view the extra effort as worthwhile and may prefer to keep different builds of the game as similar as possible. 


If you fall under any of these categories, you may want to focus on shipping your game with more robust support for traditional Controllers whilst ensuring great support for Mixed Input (when applicable). 

Also be sure to consider the importance of having ample control configuration opportunities from within the game itself and why it may be a good idea to include an option for locking to controller prompts to your desired Input type.

## Other Common API Options if Steam Input Is Not Right for My Project

If you’ve confirmed your project should not focus on a native implementation of Steam Input, you will need to find an Input API that does fit your project best. Please keep in mind, we are not Game Developers, with that said here are some brief descriptions of popular APIs and how they may interact with Steam Input.

### DirectInput

While DirectInput has support for controllers other than Xbox, it lacks support for many new features that we’re not present at the time of its creation. When using DirectInput players may have trouble with certain controllers out of the box and Steam Input is not compatible. DirectInput is by all means a deprecated API, and while it can be valuable for backwards compatibility, it should never be used in modern games as the sole method of Controller Input.

### XInput

XInput although it helped usher in a new era for Gamepads on PC, it is also well past its usefulness. XInput lacks support for any features found outside of the original Xbox 360 Controller, this includes those found in newer Xbox Controllers. XInput was most used in the late 2000’s due to its ease of porting from native Xbox 360 code.

Support is nonexistent for most non-Xbox Controllers, and while your players can use a Wrapper or Input Translation, it is advisable to use a more modern API for your new projects. It should be noted however, Steam Input does have legacy support for XInput.

### Unity’s & Unreal Engine’s Input Systems

While both handle Input slightly differently, in the interest of this write-up both accomplish the same goal. Both of these Game Engines have very simple and user friendly methods of adding support for many common controllers. 

While these are very easy to implement with and will add the necessary API calls to support non-Xbox Gamepads, neither natively support custom controller functions such as gyro support without third-party plugins. They also do not natively support Steam Controllers, but can be compatible with Steam Input’s legacy mode.

### Simple DirectMedia Layer 2.0 (SDL2)

SDL2 is more like a device library that also has its own set of API calls. With SDL2 developers get a large set of features for most modern and many legacy Controllers. Although SDL2 may not be the easiest to implement, it is one of the most forward thinking options in terms of taking advantage of as many controllers as possible.

SDL2 is one of the best choices in terms of raw Controller compatibility, and is a close cousin to Steam Input, but is not well equipped to take advantage of native gyro mapping with Steam Input. While it does allow these features with other Controllers, for Steam Input a focus on Mixed Input is still advised. 

## Achieving Mixed Input in Your Games

### What Players Expect From a Game Optimized for Mixed Input

The player should never have any issues caused specifically by Mixed Inputs. Things to look out for specifically would be frame rate issues, stuttering, and whether or not either type of input operates as it should. *E.g.* It is not uncommon to see Mouse limited to joystick values with games that allow for Mixed Input.

When configuring how automatic glyph switching should take place, Valve officially recommends that Mouse values themselves do not change the icon type. Instead it is recommended to use Mouse Click Input to swap the icon type back to Mouse and Keyboard.

Decoupling Aim Assist from GamePad use is preferred for both user accessibility and necessary when using Mixed Input. While Aim Assist can become necessary when using Traditional GamePads, once you introduce near Mouse levels of precision, it is often seen to get in the way rather than help. We recommend introducing Aim Assist as an optional feature in the settings and encourage users to choose what best works for them. In single player games we suggest making the choice available regardless of Input Device.

To bridge the issue of how to fairly match players you know are using Mixed Inputs, for the time being we recommend simply matching these players with Mouse and Keyboard users. In most cases this should be fine. A Gyroscope in the hands of a seasoned player is often at the very least able to keep pace with Mouse players and in most case scenarios it is considered a toss-up whether or not Analog Input for movement is considered an advantage.

In the future once there are far more Gyroscope users it would be ideal to group them together, but for the time being there simply isn't enough popularity to support an entirely separate matchmaking group.

Devs should consider adding an option within their games to allow for a specific type of glyph to be used at all times. This is very beneficial in specific case scenarios such as a player using a DualShock 4 with Mouse Input.

Considering all Steam Controller users are most likely to be using Mixed Inputs more so than any other form of Controller, it would certainly be appreciated to include an option for Steam Hardware Glyphs. To mesh well with other recommendations we've made you can add these as an in-game option in addition to other common types of Controllers.

### Things to Consider When Optimizing for Mixed Input

- This is also an accessibility issue
    - You have no idea anything about your players, outside the fact they will be playing your game. Although big companies in the industry have been taking baby steps towards addressing this issue. The biggest push you can make as a Developer is by understanding and supporting any custom Input setups you can. More often than not those who game with many forms of physical disabilities use custom gear made with them in mind.

- You as a Developer should never make any assumptions about controls based on  the type Input received
    - Your Actions Ingame should be handled in such a way that your Game should have no problems with an unexpected Input Type at any time.
    - Your game should always allow for Ingame remapping for any possible Inputs and ideally also change Glyphs to account for this.
    - Because Steam Input is built into Steam it is quickly becoming widely used, and many players may not understand they have the option to disable it. I reiterate in no manner should you assume all XInput based Steam Input will only be Steam Hardware.

- You shouldn’t neglect Keyboard & Mouse Input
    - Even off the subject of Mixed Input, Keyboard & Mouse is the most widely used form of Input your game will see.
    -If Mouse Input is lacking Mixed Input will suffer at least as equally.
    -Every Gamepad Radial Menu should also be mappable as a Keyboard action.

- More often than not the process of supporting Mixed Input is fairly easy
    - Some of the most ideal Mixed Input games have been made having no idea their Input Systems would ever be used in this way.
    - Making custom Controller Configurations to bundle with your game on Steam is often a job that can be done in one playthrough. This could be done by any member of your team either during off time or during QA Testing.
    -Custom Mappings can be shipped at any time for any of your games on Steam for any number of supported Controllers. You can go as in depth as you’d like, however I’d recommend not uploading any of Steam’s recommended Templates without making sure it works well with your game as this is frowned upon by the community. That said please feel free to search our articles for any tips and best practices you can use when making a Configuration to publish with your game, it is never too late to add one. 
