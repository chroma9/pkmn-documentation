# Editing Types
This is a very simple documentation on how to edit the **types.txt** file.

Here is an example of two of the ways Types can be written:
```
[17]
Name = Dark
InternalName = DARK
IsSpecialType = true
Weaknesses = FIGHTING,BUG,FAIRY
Resistances = GHOST,DARK
Immunities = PSYCHIC

[9]
Name = ???
InternalName = QMARKS
IsPseudoType = true
```

This table will show you how to compile or edit the type data.
| Data | Required | Description |
| :---- | :---- | :---- |
| [ID Number] | Yes | This line must come first in a section, because, as mentioned above, this line defines when a new section begins. This line contains a number inside square brackets, e.g. [42].<br>This number must be different for each type. It must be a whole number which is 0 or higher.<!--The ID number is used in Hidden Power's calculation, and when determining which icon corresponds to this type in several graphics (see below).--> |
| Name | Yes | The name of this type (e.g. Fire, Water). |
| InternalName | Yes | This must be different for each type. Also known as the ID, this is how the scripts refer to the type. Typically this is the same as the type's name, but written in all capital letters and with no spaces or symbols. <!--In the scripts, the ID is used as a symbol (i.e. with a colon in front of it, e.g. :GRASS). The ID is never seen by the player.--> |
| IsSpecialType | No | Is either `true` or `false`. If `true`, moves of this type will use the special stats for damage calculation. If false or undefined, they will use the physical stats.<br>This only applies if the setting `MOVE_CATEGORY_PER_MOVE` is `false`, though, which is only the case in the Gen 3 and older games. If that setting is true (as in Gen 4 and later), each move individually determines whether it is physical or special. |
| IsPseudoType | No | Is either `true` or `false`. If true, this type is a pseudotype, i.e. not a "proper" type. The `???` type is an example of a pseudotype. If false or undefined, this type will NOT be a pseudotype.<br>No Pokémon should have a pseudotype as one of its elemental types. Pseudotypes cannot be searched for in the Pokédex, the move "Conversion" and the ability "Color Change" cannot change a Pokémon's type to a pseudotype, and so on. |
| Weaknesses | No | A comma-separated list of the IDs of all the elemental types that will inflict double damage (i.e. are super effective) against a Pokémon of this type. |
| Resistances | No | A comma-separated list of the IDs of all the elemental types that will inflict half damage (i.e. are not very effective) against a Pokémon of this type. |
| Immunities | No | A comma-separated list of the IDs of all the elemental types that cannot inflict any damage on a Pokémon of this type. |

Note that the "???" type should be defined just like any other type. By default, it is the only pseudotype.
