# Editing Pokémon
This is a very simple documentation on how to edit the **pokemon.txt** file.

Here is an example of **Bulbasaur** as formatted for the **pokemon.txt** file.
```
[1]
Name = Bulbasaur
InternalName = BULBASAUR
PokedexNumber = 1
Type1 = GRASS
Type2 = POISON
BaseStats = 45,49,49,45,65,65
GenderRate = FemaleOneEighth
GrowthRate = Parabolic
BaseEXP = 64
EffortPoints = 0,0,0,0,1,0
Rareness = 45
Happiness = 70
Abilities = OVERGROW
HiddenAbility = CHLOROPHYLL
Moves = 1,TACKLE,3,GROWL,7,LEECHSEED,9,VINEWHIP,13,POISONPOWDER,13,SLEEPPOWDER,15,TAKEDOWN,19,RAZORLEAF,21,SWEETSCENT,25,GROWTH,27,DOUBLEEDGE,31,WORRYSEED,33,SYNTHESIS,37,SEEDBOMB
TutorMoves = ATTRACT,BIND,CONFIDE,CUT,DOUBLETEAM,ECHOEDVOICE,ENERGYBALL,FACADE,FRUSTRATION,GIGADRAIN,GRASSKNOT,GRASSPLEDGE,HIDDENPOWER,KNOCKOFF,LIGHTSCREEN,NATUREPOWER,PROTECT,REST,RETURN,ROCKSMASH,ROUND,SAFEGUARD,SEEDBOMB,SLEEPTALK,SLUDGEBOMB,SNORE,SOLARBEAM,STRENGTH,SUBSTITUTE,SUNNYDAY,SWAGGER,SWORDSDANCE,SYNTHESIS,TOXIC,VENOSHOCK,WORKUP,WORRYSEED
EggMoves = AMNESIA,CHARM,CURSE,ENDURE,GIGADRAIN,GRASSWHISTLE,GRASSYTERRAIN,INGRAIN,LEAFSTORM,MAGICALLEAF,NATUREPOWER,PETALDANCE,POWERWHIP,SKULLBASH,SLUDGE
Compatibility = Monster,Grass
StepsToHatch = 5120
Height = 0.7
Weight = 6.9
Color = Green
Shape = Quadruped
Habitat = Grassland
Kind = Seed
PokedexEntry = Bulbasaur can be seen napping in bright sunlight. There is a seed on its back. By soaking up the sun's rays, the seed grows progressively larger.
Generation = 1
BattlerPlayerX = -4
BattlerPlayerY = 0
BattlerEnemyX = -1
BattlerEnemyY = 26
BattlerShadowX = 0
BattlerShadowSize = 2
Evolutions = IVYSAUR,Level,16
```

Below is a list of what each value is and how to modify them accordingly.
| Part | Required | Value |
| :---- | :---- | :--- |
| [ID Number] | Yes | This is the Pokémon's Numeric ID. This is not the Pokédex Number. This also represents where the next Pokémon begins. |
| Name | Yes | The name of the Pokémon as seen by the player. |
| InternalName | Yes | This must be different for each species. Also known as the ID, this is how the scripts refer to the species. Typically this is the same as the species name, but written in all capital letters and with no spaces or symbols. In the scripts. The ID is never seen by the player |
| PokedexNumber | Yes | The National Dex number of the Pokémon. |
| Type1 | Yes | The first type of the Pokémon. |
| Type2 | No | The second type of the Pokémon. |
| BaseStats | Yes | A list of pokemon stats seperated by commas.<br>This is in order of:<ol><li>HP</li><li>Attack</li><li>Defense</li><li>Speed</li><li>Sp. Attack</li><li>Sp. Defense</li> |
| GenderRate | Yes | The likelihood of a Pokémon of the species being a certain gender.<br>Must be one of the following:<ul><li>AlwaysMale</li><li>AlwaysFemale</li><li>FemaleOneEighth</li><li>Female25Percent</li><li>Female50Percent</li><li>Female75Percent</li><li>FemaleSevenEighths</li><li>Genderless</li></ul> |
| GrowthRate | Yes | The rate at which a Pokémon of the species gains levels (i.e. how much Experience is needed to level up). Must be one of the following:<ul><li>Fast</li><li>Medium (aka. Medium Fast)</li><li>Slow</li><li>Parabolic (aka. Medium Slow)</li><li>Erratic</li><li>Fluctuating</li></ul>
| BaseEXP | Yes | The base amount of Experience gained from defeating a Pokémon of the species. It must be a whole number that is 1 or higher.<br><br>This base amount is used in a calculation to determine the actual number of Exp. points awarded for defeating a Pokémon of the species. |
| EffortPoints | Yes | The number of EVs gained by defeating a Pokémon of the species. Is six comma-separated values, corresponding to the order that main stats are defined. By default, the order is:<ol><li>HP</li><li>Attack</li><li>Defense</li><li>Speed</li><li>Sp. Attack</li><li>Sp. Defense</li> |
| Rareness | Yes | The catch rate of the species. It can be 0 or higher (typically the highest is 255). The higher the number, the more likely a capture (0 means it cannot be caught by anything except a Master Ball). |
| Happiness | Yes | The amount of happiness a newly caught Pokémon of the species will have. It can be 0 or higher, although it is typically 70. The game treats 255 as the highest attainable happiness. |
| Abilities | Yes | The IDs of one or two abilities that the species can have. If there are two abilities, separate them with a comma. |
| HiddenAbility| No | The IDs of any number of additional abilities that the species can have. If there are multiple abilities here, they are separated by commas.<br><br>Pokémon cannot have any Hidden Ability naturally, and must be specially given one. |
| Moves | No | The moves that all Pokémon of the species learn as they level up. This line consists of comma-separated level/move pairs which are themselves comma-separated,<br><br>i.e. `level,move,level,move,level,move....`<br><br>Each pair contains the level at which the Pokémon will learn the move, followed by the ID of the move it will learn.
| TutorMoves | No | A comma-separated list of the IDs of moves that a Pokémon of the species can be taught by a HM, TM, TR or Move Tutor. If a move is not listed here, it cannot be taught by those methods, even if the move appears in its Moves or EggMoves properties.	|
| EggMoves | No | A comma-separated list of the IDs of moves that a Pokémon of the species can only learn as an egg (obtained through breeding). Only species that can be in eggs should have this line (typically only unevolved species). |
| Compatability | Yes | The egg group(s) that the species belongs to. If there are multiple egg groups here, they are separated by commas. The default available egg group are:<ul><li>Monster</li><li>Water1</li><li>Water2</li><li>Water3</li><li>Bug</li><li>Flying</li><li>Field</li><li>Fairy</li><li>Grass</li><li>Humanlike</li><li>Mineral</li><li>Amorphous</li><li>Ditto</li><li>Dragon</li><li>Undiscovered</li></ul>"Water1" is for sea creatures, "Water2" is for fish, and "Water3" is for shellfish. "Ditto" should contain only Ditto, as a species in that group can breed with any other breedable Pokémon. If any egg group is "Undiscovered", the species cannot breed. |
| StepsToHatch | No | The number of steps it takes to hatch an egg of the species. It can be 1 or higher. Note that this is not the number of egg cycles for the species, but the actual number of steps. Only species that can be in eggs should have this line (typically only unevolved species). |
| Height | Yes | The height of the species in meters, to one decimal place. Use a period for the decimal point, and do not use commas for thousands.<br>The Pokédex will automatically show this height in feet/inches if the game recognises that the player is in the USA. This is only cosmetic; the rest of the scripts still perform calculations using the meters value defined. |
| Weight | Yes | The weight of the species in kilograms, to one decimal place. Use a period for the decimal point, and do not use commas for thousands.<br>The Pokédex will automatically show this weight in pounds if the game recognises that the player is in the USA. This is only cosmetic; the rest of the scripts still perform calculations using the kilograms value defined. |
| Color | Yes | The main body color of the species. The default available body colors are:<ul><li>Black</li><li>Blue</li><li>Brown</li><li>Gray</li><li>Green</li><li>Pink</li><li>Purple</li><li>Red</li><li>White</li><li>Yellow</li></ul>| 
| Shape | Yes | The body shape of the species. The Pokédex can search for Pokémon of particular shapes. The default available body shapes are:<ul><li>Head</li><li>Serpentine</li><li>Finned</li><li>HeadArms</li><li>HeadBase</li><li>BipedalTail</li><li>HeadLegs</li><li>Quadruped</li><li>Winged</li><li>Multiped</li><li>MultiBody</li><li>Bipedal</li><li>MultiWinged</li><li>Insectoid</li></ul> |
| Habitat | Yes | The kind of location that the species can typically be found in. The default available habitats are:<ul><li>None</li><li>Cave</li><li>Forest</li><li>Grassland</li><li>Mountain</li><li>Rare</li><li>RoughTerrain</li><li>Sea</li><li>Urban</li><li>WatersEdge</li></ul>"Rare" can be taken to mean "unknown" here.<br><br>This information is currently unused but may be used in the future. |
| Kind | Yes | The species' category, which is displayed in the Pokédex. For example, Bulbasaur is the Seed Pokémon. The word "Pokémon" is automatically added to the end, so only "Seed" needs to be here.	|
| FormName | No | If this does not exist, then its form name as shown in the Pokédex's Forms page will be "Male"/"Female" if the species is gendered. If the species is genderless, its form name will instead be "Genderless" (if this is the only form for the species) or "One Form" (if the species also has other forms). |
| PokedexEntry | Yes | The description of the Pokémon in the Pokédex. |
| Generation | Yes | A number representing the generation of Pokémon games in which this species first appeared. This information is unused currently. |
| WildItemCommon<br>WildItemUncommon<br>WildItemRare | No | The IDs of items that a wild Pokémon of the species may be found holding. Each line can only have one item.<br><br>The chances of holding the item are 50%, 5% and 1% respectively. If all three are the same item, then the chance of holding it is 100% instead. |
| BattlerPlayerX<br>BattlerPlayerY | Yes | Affects the positioning of the back sprite of the species in battle. A higher number means the back sprite is placed further right/lower down in the screen. Can be positive or negative. |
| BattlerEnemyX<br>BattlerEnemyY | Yes | Affects the positioning of the front sprite of the species in battle. A higher number means the front sprite is placed further right/lower down in the screen. Can be positive or negative. |
| BattlerAltitude | Yes | Affects the positioning of the front sprite of the species in battle relative to its base. A higher number means the front sprite is placed further up the screen. Can only be positive or 0.<br><br>This property is typically unused because BattlerEnemyY can do the same thing. |
| BattlerShadowX | Yes | Affects the horizontal positioning of the shadow beneath the front sprite of the species in battle. A higher number means the shadow is placed further right on the screen. Can be positive or negative. |
| BattlerShadowSize	| Yes | A number that determines which shadow graphic to place underneath the front sprite of the species in battle. It can be 0 or higher. By default, there are three possible shadow graphics, ranging from 1 (smallest) to 3 (largest). |
| Evolutions | No | The evolution paths the species can take. For each possible evolution of the species, there are three parts:<ol><li>The ID of the species it evolves into.</li><li>The method of evolution. Examples are below.</li><li>A parameter used by the evolution method. Depending on the method, this could be NULL or a number or the ID of a move/item/ability/species/type/etc.</li></ol>Below is the example list of evolution methods:<ul><li>Level</li><li>LevelFemale</li><li>LevelMale</li><li>Happiness</li><li>Beauty</li><li>HasMove</li><li>Location</li><li>Item</li><li>Trade</li><li>Time</li></ul>If there are multiple evolution paths, they are separated by commas. The three parts of each evolution path are also separated by commas. Be careful to include the correct number of commas when writing an evolution path whose method doesn't use a parameter. |
| Incense | No | The ID of an item that needs to be held by a parent when breeding in order for the egg to be this species. If neither parent is holding the required item, the egg will be the next evolved species instead.<br><br>The only species that should have this line are ones which cannot breed, but which evolve into a species that can. That is, the species should be a "baby" species. Not all baby species need this line. |
