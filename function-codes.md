# Move Function Codes
Documentation on Function codes for each type of Attack.

| Code | Effect |
| :---- | :--- |
| 000 | No additional effect. |
| 001 | Does absolutely nothing. (Splash) |
| 002 | Struggle, if defined as a move in moves.txt. Typically it won't be. |
| 003 | Puts the target to sleep. |
| 004 | Makes the target drowsy; it falls asleep at the end of the next turn. (Yawn) |
| 005 | Poisons the target. |
| 006 | Badly poisons the target. (Poison Fang, Toxic) |
| 007 | Paralyzes the target.<br>Thunder Wave: Doesn't affect target if move's type has no effect on it.<br>Body Slam: Does double damage and has perfect accuracy if target is Minimized. |
| 008 | Paralyzes the target. Accuracy perfect in rain, 50% in sunshine. Hits some semi-invulnerable targets. (Thunder) |
| 009 | Paralyzes the target. May cause the target to flinch. (Thunder Fang) |
| 00A | Burns the target. |
| 00B | Burns the target. May cause the target to flinch. (Fire Fang) |
| 00C | Freezes the target. |
| 00D | Freezes the target. Accuracy perfect in hail. (Blizzard) |
| 00E | Freezes the target. May cause the target to flinch. (Ice Fang)
| 00F | Causes the target to flinch. |
| 010 | Causes the target to flinch. Does double damage and has perfect accuracy if the target is Minimized. (Dragon Rush, Steamroller, Stomp) |
| 011 | Causes the target to flinch. Fails if the user is not asleep. (Snore) |
| 012 | Causes the target to flinch. Fails if this isn't the user's first turn. (Fake Out) |
| 013 | Confuses the target. |
| 014 | Confuses the target. (Chatter) |
| 015 | Confuses the target. Accuracy perfect in rain, 50% in sunshine. Hits some semi-invulnerable targets. (Hurricane) |
| 016 | Attracts the target. (Attract) |
| 017 | Burns, freezes or paralyzes the target. (Tri Attack) |
| 018 | Cures user of burn, poison and paralysis. (Refresh) |
| 019 | Cures all party Pokémon of permanent status problems. (Aromatherapy, Heal Bell)<br><br>* NOTE: In Gen 5, this move should have a target of UserSide, while in Gen 6+ it should have a target of UserAndAllies. This is because, in Gen 5, this move shouldn't call def pbSuccessCheckAgainstTarget for each Pokémon currently in battle that will be affected by this move (i.e. allies aren't protected by their substitute/ability/etc., but they are in Gen 6+). We achieve this by not targeting any battlers in Gen 5, since pbSuccessCheckAgainstTarget is only called for targeted battlers. |
| 01A | Safeguards the user's side from being inflicted with status problems. (Safeguard) |
| 01B | User passes its status problem to the target. (Psycho Shift) |
| 01C | Increases the user's Attack by 1 stage. |
| 01D | Increases the user's Defense by 1 stage. (Harden, Steel Wing, Withdraw) |
| 01E | Increases the user's Defense by 1 stage. User curls up. (Defense Curl) |
| 01F | Increases the user's Speed by 1 stage. (Flame Charge) |
| 020 | Increases the user's Special Attack by 1 stage. (Charge Beam, Fiery Dance) |
| 021 | Increases the user's Special Defense by 1 stage. Charges up user's next attack if it is Electric-type. (Charge) |
| 022 | Increases the user's evasion by 1 stage. (Double Team) |
| 023 | Increases the user's critical hit rate. (Focus Energy) |
| 024 | Increases the user's Attack and Defense by 1 stage each. (Bulk Up) |
| 025 | Increases the user's Attack, Defense and accuracy by 1 stage each. (Coil) |
| 026 | Increases the user's Attack and Speed by 1 stage each. (Dragon Dance) |
| 027 | Increases the user's Attack and Special Attack by 1 stage each. (Work Up) |
| 028 | Increases the user's Attack and Sp. Attack by 1 stage each.<br>In sunny weather, increases are 2 stages each instead. (Growth) |
| 029 | Increases the user's Attack and accuracy by 1 stage each. (Hone Claws) |
| 02A | Increases the user's Defense and Special Defense by 1 stage each. (Cosmic Power, Defend Order) |
| 02B | Increases the user's Sp. Attack, Sp. Defense and Speed by 1 stage each. (Quiver Dance) |
| 02C | Increases the user's Sp. Attack and Sp. Defense by 1 stage each. (Calm Mind) |
| 02D | Increases the user's Attack, Defense, Speed, Special Attack and Special Defense by 1 stage each. (Ancient Power, Ominous Wind, Silver Wind) |
| 02E | Increases the user's Attack by 2 stages. (Swords Dance) |
| 02F | Increases the user's Defense by 2 stages. (Acid Armor, Barrier, Iron Defense) |
| 030 | Increases the user's Speed by 2 stages. (Agility, Rock Polish) |
| 031 | Increases the user's Speed by 2 stages. Lowers user's weight by 100kg. (Autotomize) |
| 032 | Increases the user's Special Attack by 2 stages. (Nasty Plot) |
| 033 | Increases the user's Special Defense by 2 stages. (Amnesia) |
| 034 | Increases the user's evasion by 2 stages. Minimizes the user. (Minimize) |
| 035 | Decreases the user's Defense and Special Defense by 1 stage each.<br>Increases the user's Attack, Speed and Special Attack by 2 stages each.<br>(Shell Smash) |
| 036 | Increases the user's Speed by 2 stages, and its Attack by 1 stage. (Shift Gear) |
| 037 | Increases one random stat of the target by 2 stages (except HP). (Acupressure) |
| 038 | Increases the user's Defense by 3 stages. (Cotton Guard) |
| 039 | Increases the user's Special Attack by 3 stages. (Tail Glow) |
| 03A | Reduces the user's HP by half of max, and sets its Attack to maximum. (Belly Drum) |
| 03B | Decreases the user's Attack and Defense by 1 stage each. (Superpower) |
| 03C | Decreases the user's Defense and Special Defense by 1 stage each. (Close Combat, Dragon Ascent) |
| 03D | Decreases the user's Defense, Special Defense and Speed by 1 stage each. (V-create) |
| 03E | Decreases the user's Speed by 1 stage. (Hammer Arm, Ice Hammer) |
| 03F | Decreases the user's Special Attack by 2 stages. |
| 040 | Increases the target's Special Attack by 1 stage. Confuses the target. (Flatter) |
| 041 | Increases the target's Attack by 2 stages. Confuses the target. (Swagger) |
| 042 | Decreases the target's Attack by 1 stage. |
| 043 | Decreases the target's Defense by 1 stage. |
| 044 | Decreases the target's Speed by 1 stage. |
| 045 | Decreases the target's Special Attack by 1 stage. |
| 046 | Decreases the target's Special Defense by 1 stage. |
| 047 | Decreases the target's accuracy by 1 stage. |
| 048 | Decreases the target's evasion by 1 stage. (2 stages if Gen 6+) (Sweet Scent) |
| 049 | Decreases the target's evasion by 1 stage. Ends all barriers and entry hazards for the target's side OR on both sides. (Defog) |
| 04A | Decreases the target's Attack and Defense by 1 stage each. (Tickle) |
| 04B | Decreases the target's Attack by 2 stages. (Charm, Feather Dance) |
| 04C | Decreases the target's Defense by 2 stages. (Screech) |
| 04D | Decreases the target's Speed by 2 stages. (Cotton Spore, Scary Face, String Shot) |
| 04E | Decreases the target's Special Attack by 2 stages. Only works on the opposite gender. (Captivate) |
| 04F | Decreases the target's Special Defense by 2 stages. |
| 050 | Resets all target's stat stages to 0. (Clear Smog) |
