LegacyAC is a plugin designed to manage your gear swaps, using the legacy format used in Ashitacast for Ashita3.
This is done through an XML file, which should be placed in Ashita/Config/LegacyAC/
and named CharacterName_JOB.xml.  XMLs will be automatically loaded or unloaded whenever you change jobs,
or can be triggered through commands.  There are some included sample files and a list of valid variables.
Equipment is layered precast<action<midcast in one outgoing packet, which ensures that your precast will always lower
your casttime(or ranged time for rng) and your midcast will always be on in time(even on instant casts or rapid shot).

Commands - can use /legacyac or /la

/la load - Attempt to load Charname_JOB.xml.
/la load Filename.xml - Attempt to load Filename.xml
/la reload - Reload the active swap XML.
/la unload - Unload the active swap XML.

/la naked - Remove all gear.
/la set SetName [Duration] - Lock SetName on for Duration in seconds(5 if unspecified).
/la enable [Slot] - Enables gear swaps for the specified slot, or all slots if unspecified.
/la disable [Slot] - Disables gear swaps for the specified slot, or all slots if unspecified.

/la action [Target Index] [ma/ws/ja/ra] [action ID if not ra] - Directly sends an action packet through with appropriate swaps.
/la debug [Optional: On/Off] - Enables or disables debug prints of all equip swaps.  Will toggle if on/off isn't specified.

/la validate - Uses the packer plugin, which must also be loaded, to print an output of what items in your XML are not currently in your inventory/wardrobes.
/la gear - Uses the packer plugin, which must also be loaded, to automatically collect gear from your currently loaded xml.  Will not work with neither loaded.
/la preppack - Uses the porter addon, which must also be loaded, to accumulate items that your current XML does not use to be stored in porter moogle.
/la pack - Uses the porter addon, which must also be loaded, to store items that your current XML does not use on the porter moogle.
/la prepunpack - Uses the porter addon, which must also be loaded, to accumulate storage slips containing items your current XML uses.
/la unpack - Uses the porter addon, which must also be loaded, to use storage slips in your inventory to retrieve items your current XML uses.

/la help - Display help on commands.
/la help print - Display help on print commands.
/la help var - Display help on var commands.

/la var clear - Clear all user-defined variables.
/la var set [name] [value] - Set a variable to a specific value.
/la var inc [Name] [Optional: Amount] - Increase a variable.  Defaults to 1.
/la var dec [Name] [Optional: Amount] - Decrease a variable.  Defaults to 1.

/la print augs \"Item Name\" - Prints a code used to reference the augments on an item.
/la print uvars - Print current values of all user-defined variables.
/la print vars - Print current values of all built-in variables.
/la print set [setname] - Print a set.

/la addset Name - Add your currently equipped gear to your loaded XML under the specified set name.
/la newxml Name - Create a blank XML and load it(doesn't include rules, just gives you a blank template to add sets to).


=========== WARNING: NOT FOR RETAIL USE ============

/la override [inventory/safe/storage/temporary/locker/satchel/sack/case/wardrobe/safe2/wardrobe2/wardrobe3/wardrobe4]

This allows LegacyAC to try to equip items from bags other than the typical inventory and wardrobes.  You can also use it to disable bags from being used to equip by specifying a bag that is currently enabled.  This was a private server feature request; they are attempting to make other bags function as additional wardrobes.

 DO NOT ENABLE THIS ON RETAIL.  You will be booted to the title screen as soon as you attempt to equip an item that is not in inventory/wardrobes.  You may be banned or suspended for doing this, and it will not successfully equip the item.
 
=========== WARNING: NOT FOR RETAIL USE ============
