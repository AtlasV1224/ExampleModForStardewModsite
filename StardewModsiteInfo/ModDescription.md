# Example Mod
This is an example mod documenting and detailing the features of the Stardew Modsite, it also acts as reference and examples for the information that can be used to display the mod on the site accurately and to your liking.

these examples below of the information detail what can be used for the site are here for both reference and examples, you are freee to copy them into your mod's or mod page's readme and change the details to fit.

all the information is hidden in summary elements, these are drop down boxes that when given the class `stardew-modsite-summary` will be hidden on the modsite and used instead for variois things like human readable titles, short descriptioms, tagging, and more.

### Manifest
using the summary tags you can provide a path from the root of the repo or a URL to your mod's manifest, this will allow the fields in tbe manifest to be auto detected and used for various parts of the mod page. For example:
```
<details>
  <summary>Stardew Modsite Info</summary>
  
  Manifest: ExampleMod/manifest.json
  // or
  Manifest: https://github.com/AtlasV1224/ExampleModForStardewModsite/blob/main/ExampleMod%2Fmanifest.json
  
</details>
```
This will be used to derive the Mod display name ("(CP) Example Mod"), The Author ("AtlasV"), the pill with the latest version number ("1.26.1"), the short description used for the card on the home page (not the mod's main description), if its a content pack it will use the ContentPackFor field for filtering what mod it is for, and the dependancies for filtering also.
Any of these fields can be overridden byt using a similar summary block with the same field name, for istance:
```
<details>
  <summary>Stardew Modsite Info</summary>
  
  Manifest: ExampleMod/manifest.json
  // or
  Manifest: https://github.com/AtlasV1224/ExampleModForStardewModsite/blob/main/ExampleMod%2Fmanifest.json
  // with the overrides of
  Name: Example Mod
  // will keep all the other details like the description, version, author, and such the same, Except for the name which will now be displayed as "Example Mod" and not "(CP) Example Mod" on the mod page
  
</details>
```

### Tags
You can add tags for the for site for filtering purposes, these filters are likely to change in the future and so will be displayed as an up to date list on the website to copy and paste if needed, here is an example of the tags in a summary block, any unrecognised tags will be skipped.
```
<details>
  <summary>Stardew Modsite Info</summary>
  
  Tags:
  - Audio
    - [ ] Additions
    - [ ] Mechanics
  - Buildings
    - [ ] Additions
    - [ ] Mechanics
    - [ ] Recolor
  - Characters
    - [ ] Additions
    - [ ] Visual Modifications
    - [ ] Content Modifications
  - Farmer Clothing
    - [ ] Additions
    - [ ] Modifications
  - Crafting
    - [ ] Additions
    - [ ] Modifications
  - Crops 
    - [ ] Additions
    - [ ] Modifications
  - Dialogue
    - [ ] Additions
    - [ ] Modifications
  - Events 
    - [ ] Additions
    - [ ] Modifications
  - Collectables
    - [ ] Fish
    - [ ] Museum Donations
  - Maps
    - [ ] Additions
    - [ ] Modifications
  - Livestock
    - [ ] Additions
    - [ ] Visual Modifications
    - [ ] Content Modifications
  - Modding Tools
    - [ ] In Game
    - [ ] External
  - Translation
    - [ ] German
    - [ ] Spanish
    - [ ] French
    - [ ] Italian
    - [ ] Japanese
    - [ ] Korean
    - [ ] Hungarian
    - [ ] Portuguese
    - [ ] Russian
    - [ ] Turkish
    - [ ] Chinese
    - [ ] Other (Language without a language code)
  - [ ] Expansions
  - [ ] Cheats
  
  
</details>
```
To add a tag to a mod, add an "x" inside tbe square brackets, for example:
```
- Crops 
    - [ ] Additions
    - [ ] Modifications
```
would be 
```
- Crops 
    - [x] Additions
    - [ ] Modifications
```
for a mod that adds new crops. Any tags not needed can be removed. 

### Dependancies
The site will attempt to automatically find the right dependancies for mods from the manifest, however this may not be achievable for all mods, to curb this, you can provide direct links to the dependancies like so:
```
<details>
  <summary>Stardew Modsite Info</summary>
  
  Dependancies:
    "https://github.com/Pathoschild/StardewMods/tree/stable/ContentPatcher": Required
  
</details>
```
you can also define optional dependancies by replaceing the "Required" with "Optional"

### Optional Mods
Some mods pair well with others, or have extra additions or changes that are conditionally included, just like the dependancies, you can provide a list of optional mods that pair well, these wont be automatically derived and so require you to add them.
```
<details>
  <summary>Stardew Modsite Info</summary>
  
  Optional Mods:
    https://github.com/Mushymato/PeliQ
    https://github.com/spacechase0/StardewValleyMods/tree/develop/framework%2FGenericModConfigMenu
  
</details>
```

### Full Example
```
<details>
  <summary>Stardew Modsite Info</summary>
  
  Manifest: https://github.com/AtlasV1224/ExampleModForStardewModsite/blob/main/ExampleMod%2Fmanifest.json
  Name: Example Mod

  Tags:
  - Modding Tools
    - [x] External

  Dependancies:
    - "https://github.com/Pathoschild/StardewMods/tree/stable/ContentPatcher": Required
  
  Optional Mods:
    - https://github.com/Mushymato/PeliQ
    - https://github.com/spacechase0/StardewValleyMods/tree/develop/framework%2FGenericModConfigMenu
  
</details>
```
would look like
<details>
  <summary>Stardew Modsite Info</summary>
  
  Manifest: https://github.com/AtlasV1224/ExampleModForStardewModsite/blob/main/ExampleMod%2Fmanifest.json
  
  Name: Example Mod

  Tags:
  - Modding Tools
    - [x] External

  Dependancies:
  - "https://github.com/Pathoschild/StardewMods/tree/stable/ContentPatcher": Required
  
  Optional Mods:
  - https://github.com/Mushymato/PeliQ
  - https://github.com/spacechase0/StardewValleyMods/tree/develop/framework%2FGenericModConfigMenu
  
</details>