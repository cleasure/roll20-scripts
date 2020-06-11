# Macro Descriptions

Below is a short list of each macro, its function, and use case.

## Vision
The vision macro allows you to quickly alter the selected token's provided light radius, dim radius, multiplier, and if others can see the light.
##### Requirements
* TokenMod https://wiki.roll20.net/Script:Token_Mod
  * Used to expose interfaces for modifying token attributes
##### Use
* Add TokenMod to your games Script Library https://wiki.roll20.net/API:Use_Guide#The_Script_Editor
* Add the contents of vision.txt as a new macro
* Select a token and click the macro
* Select the desired vision type and click submit
##### Details
The macro will edit four fields on the target token: Light Radius, Start of Dim, All Players See Light, and Multiplier

![Light](https://i.imgur.com/Mo8sb3o.png)

In the above example a player holding a torch provides 20' of dim light followed by 20' of bright light.  This is represented by the total light radius being 40' and the transition from bright to dim begins at 20'.  Additionally the has sight checkbox causes the light to be seen by all characters.

With the above in mind there are currently six presets in the macro.
* None
  * This setting will reset all light to 0 and remove any multipliers.  Useful for when characters without any low light vision remove their light source.
* Torch 40/20
  * 40' of dim and 20' of bright visable to all players.
* Hooded Lanter (Lowered) 5/-5
  * 5' of dim visable to all players.
* Hooded Lanter (Open) 60/30
  * 60' of dim and 30' of bright visable to all players.
* Dark Vision 60/-5
  * 60' of dim and bright is doubled for the individual player.  
  * Darkvision is unique in that the player can see dim light within their radius as if it were bright, and darkness as if it were dim.  This effectively doubles their sight from any light producing objects.  To compensate for this we set light radius to 30 and dim light at -5 to cause all light to be dim, then we set the light multiplier to 2.  The multiplier will cause the dim light vision in darkness to be doubled to the appropriate 60' and will double the length of any bright light, effectively turning previous low light vision to bright.
* Devil Sight 120/0
  * 120' of bright visable to the individual player.
