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
  Manifest: 
  
</details>