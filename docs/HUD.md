---
tags:
  - Class
---
# Class "HUD"
## Functions
### Assign·Player·HUDs () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### void AssignPlayerHUDs ( ) {: .copyable aria-label='Functions' }
Refreshes the HUD (e.g. Characters that have Parent specified no longer show their health in the main HUD).
___
### Flash·Charge·Bar () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### void FlashChargeBar ( [EntityPlayer](EntityPlayer.md) Player, [ActiveSlot](enums/ActiveSlot.md) ActiveSlot ) {: .copyable aria-label='Functions' }
Chargebar flashes as if item was actually charged.
___
### Invalidate·Active·Item () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### void InvalidateActiveItem ( [EntityPlayer](EntityPlayer.md) Player, [ActiveSlot](enums/ActiveSlot.md) ActiveSlot ) {: .copyable aria-label='Functions' }
___
### Invalidate·Crafting·Item () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### void InvalidateCraftingItem ( [EntityPlayer](EntityPlayer.md) Player ) {: .copyable aria-label='Functions' }
___
### Is·Visible () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### boolean IsVisible ( ) {: .copyable aria-label='Functions' }
Returns false if HUD is invisible and true otherwise.
___
### Show·Fortune·Text () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### void ShowFortuneText ( string MainString, string SecondaryString, ... ) {: .copyable aria-label='Functions' }
Allows to display fortune streak with text. Accepts unlimited amount of arguments.
___
### Show·Item·Text () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### void ShowItemText ( string MainString, string SecondaryString, boolean IsCurseDisplay = false ) {: .copyable aria-label='Functions' }

Displays "streak text". You can use this to simulate the player picking up an item without them actually picking anything up. The name of the method is misleading, as you can generate any arbitrary text - it does not necessarily have to do with an item.

This method is overloaded, meaning that you can use two different sets of parameters, depending on your needs. (See the subsequent section.)

For example:

```lua
local function showHelpText()
  local game = Game()
  local hud = game.GetHUD()

  hud:ShowItemText("Don't touch the spikes!", "It will drain your mana.")
end
```

___
### Show·Item·Text () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### void ShowItemText ( [EntityPlayer](EntityPlayer.md) Player, [ItemConfigItem](ItemConfig_Item.md) Item) {: .copyable aria-label='Functions' }

Displays "streak text". You can use this to simulate the player picking up an item without them actually picking anything up.

This method is overloaded, meaning that you can use two different sets of parameters, depending on your needs. (See the previous section.)

For example:

```lua
local function showSadOnionText()
  local game = Game()
  local hud = game.GetHUD()
  local itemConfig = Isaac.GetItemConfig()

  local player = Isaac.GetPlayer()
  local itemConfigItem = itemConfig:GetCollectible(CollectibleType.COLLECTIBLE_SAD_ONION)
  hud:ShowItemText(player, itemConfigItem)
end
```

___
### Set·Visible () {: aria-label='Functions' }
[ ](#){: .rep .tooltip .badge }
#### void SetVisible ( boolean Visible = false ) {: .copyable aria-label='Functions' }
Turns the HUD on or off.
