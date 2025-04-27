# Tiny Legends 1 Crazy Knight

## Controls (Configurable)
|Control|Bind(s)|Default Key(s)|
|-------|----|--------------|
|Movement|Horizontal + Vertical|WASD/Up Down Left Right Arrows|
|Look (Bow/Staff)|HorizontalLook + VerticalLook|N/A|
|Look (Bow/Staff) Alt|N/A|Mouse Movement|
|Attack|Attack|E/Mouse 0|
|Roll|Roll|R/Mouse 1|
|Skill|Skill|F/Mouse 2|
|Pause|Pause|Escape/Enter|
|Revive|Revive|Q|

## Decompilation

### Controls are implemented in UICrazyScene.cs  
They dont compile on Non-Standalone platforms because they override some of the on-screen ones.  
More comments on that in the script.  

### UI Inputs  
UI inputs for non standalone AND standalone platforms are implemented, yes.  
They are located in TUIInputManagerIOS.cs and TUIInputManagerWindows.cs  
For standalone platforms im currently swapping the IOS one with Windows one in TUIInputManager.cs

### AndroidFakeCall  
It was added because there was a LOT of android calls in source, which i didnt want to manage.  
Feel free to use it anywhere, except some stuff breaking or not working.

### Errors..? Bugs?
TUIFont.cs was bugging out so i had to implement fix for it in Awake() method.

TAudioManager.cs was breaking, had to do fix too. (line 29)

BGM audio has to be manualy set from 3D to 2D cuz yes.