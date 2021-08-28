# 05d Configuration Based Haptics

## What is Haptic Feedback?

Haptic Feedback is  a form of emulated physical feedback, sometimes also referred to as HD Rumble or 3D Touch. Haptic Feedback as present in the Steam Controller uses two Actuator Motors embedded under its twin Touchpads. These motors are used to create very deliberate Ultrasonic Sound pulses that can be used to give the user the sensation of feeling a physical object. While both the Switch Pro Controller and DualSense Controller have Haptic Motors neither of them currently has full support for Steam Inputs Haptics, mainly configuration adjustments. Therefore this guide will not address them.

Haptic Feedback was first added to the Steam Controller with the intention of allowing developers to create a more realistic sense of presence than traditional Rumble Motors. Another function is giving the player a more tactile sense for feedback from emulated inputs driven by the twin Touchpads present on the Steam Controller as well as the Steam Deck.

While at launch Steam's built-in controller configurator (now known as Steam Input) lacked much of the functionality necessary to make much use of user defined Haptics, the configurator in its present form now gives the user a lot more flexibility in terms of controlling haptics.
In this chapter we will be covering the basics of controlling Haptics in your Controller Configs.

## A Note for Developers

While you can include these tips in any of your official Game Configurations you upload, as a Developer if you are interested, I would recommend discussing with your team the possibility of added native Steam Input support. A native implementation would give you a much lower level of access to controlling the Haptics of many currently supported controllers as well as potentially more in the future. If you have any interest please see Valves official documentation Here.

## Creating User Defined Haptics

For this chapter please be aware, we will be talking about different strategies on how to use bindings in unconventional ways. The following is a small list on how these activators will be used in the context of user created Haptics and may not necessarily explain how they can be used for general Input Mapping, Please see previous chapters for descriptions based on general input.

### Empty Bindings

Empty Bindings in this context will be used to tell Steam Input to create certain haptic effects when the player makes specific movements without giving the game any inputs.

### Regular Presses

Regular Presses will fire Haptics in a manner consistent with presses on your average Controllers, the only change comes in while a Start Press is bound to the same Input as a Regular Press. In this situation the Start Press will always fire before Regular Presses as well as any other types of Activators.

### Soft Presses

Soft Presses will be used to tell Steam Input when we want our Haptics to actuate when a player physically crosses a certain threshold with their input method of choice.

When it comes to creating Haptics, Soft Presses are one of the most powerful tools. They can be used for instance on the Touchpad via an Outer Ring Binding to create a virtual ring that can be felt by the user. This virtual ring could be bound to an Action such as sprint or used with an Empty Binding so as to create no in-game Input.

*[ QuizzicalCube’s Notes: Another example would be to create virtual Trigger Stages. Binding a Soft Press at any point to a Trigger Soft Pull will allow us to in theory add as many virtual stages as we would like. That said because each Input Binding features three levels of Haptics we can have up to four unique feeling clicks per Steam Controller Trigger; three for the Steam Deck being it lacks a real physical click. ]*

### Release presses

Release Presses will be used for actuating our Haptics after the user physically releases the method of Input. We can also add Fire Start Delay as needed inorder to simulate physical movement from real devices.

### Chorded Presses

Chorded Presses can be used to either override bound Haptics or add different ones while a specific Input is held.

## Overview of Activator Haptic Characteristics

Something worth noting is that most types of Activators have slightly different Haptic characteristics. Although in theory we can take advantage of this to apply different strengths of Haptic Feedback this is more often than not unfeasible . 

Each Activator will still apply Inputs as intended, meaning for example although Soft Presses have a much stronger Haptic Feedback they are only available for Inputs Types that Steam Input deems to be Analog based. Even if we could use this for Touch Bindings as an example, Haptics can only be triggered while the Soft Press Threshold is met. Meaning that most Activators do not lend themselves well to this use case.

Here are all Presses grouped based on characteristics

* Regular Press / Choreded Press
* Release Press / Start Press
* Soft Press
* Long Press

*[ QuizzicalCube’s Notes: Because they are based on feeling, we encourage you to test them yourself. Making a description would be difficult and subjective. ]*

### Turbo Settings (or Hold to Repeat)

Turbos will allow us to tell Steam Input to repeat a command at a set rate while an Input is held, however any Haptics on our Binding will repeat as well. This will allow us to in effect pulse Haptics constantly at a fixed rate. By adding one or more Empty Bindings as a separate Activator plus an added Fire Start Delay we can pulse Haptics at even faster rates.

