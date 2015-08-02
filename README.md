"grim's assistant" is a featureful Expression 2 chip, written for Wiremod.



 ------------------------------------------------------------------------------------------------
	Hey there!
	I wrote the first lines of this little toy back in July of 2010 when learning the magix of Expression2.
	With the intention of stuffing every possible ability I could into one single chip a created the
assistant as a tool for my day to day Garry's Mod needs.
	As its popularity began to increasce I remained concerned with the minge-magnitude that could be unleashed
with it. It was in early 2011 that I finally decided to release the source code and unlock the anti-dupe protection
I had built into the chip.
	As of now you are able to receive updates as they are released on git, directly into the assistant embeded code updater, you are also free to share and edit it under the terms of the General Public License version 2.
	I hope you have fun with this simple toy. As some users have already done, feel free to email me with any questions you might have. Even tho it has been years since I coded into the assistant, I still enjoy helping people using it.

> The small percentage of the code I didnt write is credited in the Command List Below.

> 25% of the maxquota is a lot while idle, I know. I dont know how to decreasce that without deletting half of the code. Feel free to share if you have any method of making it more efficient in that regard.

 ------------------------------------------------------------------------------------------------

 MANY THANKS TO:
  - Luck Wielding Lunatic (for being the best gaming pal of all tiemz :D)
  - NeO_Huperman (for hosting his amazing GMod Server)
  - Silicon (for his leet skills and will to help, also for hosting his MaximumTrolling-Sponge-compatible Server :D
  - Ghostrin, bestchallenger|PT|, Clicklord, Kamakazebanzai,
     OMEGA, BeafyBubbles, Donut, mr. bubbles, Beaver, 
      Zatrac and Galacon (for the inspiration and support)
  - All the E2 authors and Minges that contributed and inspired the concepts and features in this code
 

:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

 --- Updater ---
 /update - updates or redownloads The Assistant from the Web (git repository)




 --- Position ---
 /height NUMBER - changes Height to NUMBER (Default=120)
 /up | /down - +-10 Height
 /radius NUMBER - changes the orbit radius to NUMBER (Default=70)
 /ovelocity NUMBER - changes orbit velocity to NUMBER (Default=90)

 /master - follow OWNER
 /omaster or /nomaster - orbit OWNER
 /cross - follow CROSSHAIRS
 /ocross - orbit CROSSHAIRS
 /follow PLAYER - follow PLAYER
 /orbit PLAYER or /norbit PLAYER - orbit PLAYER
 /that - follow TARGET ENTITY [CROSSHAIRS ON TARGET]
 /othat - orbit TARGET ENTITY [CROSSHAIRS ON TARGET]
 /place - hover TARGET COORDINATES [CROSSHAIRS ON MAP]
 /oplace or /noplace  - hover and orbit CROSSHAIRS COORDINATES [CROSSHAIRS ON MAP]
 /gosleep - makes the drone deactivates itself in a location [CROSSHAIRS ON MAP]



 --- Skills ---
 /sd! - Self Destruction!!!
 bba - activates EXPLOSIVE OUTPUT
 /ppinfo - activates PropInfo (MouseKey2 on target to see the owner)
 /ppinfooff deactivates PropInfo
 !brl or !brls - spawns 1 or 10 barrels, respectively (needs 'wire_expression2_concmd 1')
 /fury PLAYER - follow PLAYER with FURY MODE (hurts PLAYER)
 /efury PLAYER - follow PLAYER with FURY MODE and repetitive explosions
 /torture PLAYER - uses both the Blind major skill, the /earrape and the /efury skills to torment PLAYER
 /tortureoff - deactivates Torture
 /earrape - activates the Ear Rape skill
 /earrapeoff - deactivates the Ear Rape skill
 /e2list - lists all the Expression2 chips in the server



 --- Skills + Return ---
 (NOTE: 'say mbba' and 'say mbbas' should be binded to Keyboard Keys for easy access)

 pbba PLAYER - assassinates PLAYER with Explosives and returns (needs explosives wired to EXPLOSIVE OUTPUT)
 mbba - explodes in the CROSSHAIR LOCATION and returns
 mbbas - explodes in the CROSSHAIR LOCATION, spawning 10 flaming barrels and returns (needs a huge HP explosive, or else might kill the owner when returning) (needs 'wire_expression2_concmd 1')
 find PLAYER - finds PLAYER and returns
 findi PLAYER - finds PLAYER and returns invisible



 --- Cammo ---
 /invisible - makes the Assistant invisible
 /visible - makes the Assistant visible
 /sneak - makes OWNER invisible
 /unsneak - makes OWNER visible
 /hide = /invisible + /sneak
 /unhide = /visible + /unsneak



 --- Body ---
 /ghost - Activates GHOST Mode making the Assistant Non-Solid [!!! REQUIRES the PropCore plugin !!!]
 /unghost - Deactivates GHOST Mode
 /body reset - resets the body options (color, size...)
 /size NUMBER - changes the size to NUMBER
 /trailsize NUMBER - changes the trail size to NUMBER
 /body COLOR - changes the color preset
               COLOURs are: black, yellow, green, green2, blue, red, white, white2 and electric



 --- Sounds ---
 /soundstop - stops the music player and the ambient sounds
 /ss_(owner, ent, weld, target) - changes the source of the sound (Default='/ss_owner')
 /music | /music NUMBER - activates or changes the music track (/music will pick a random track)
 /ambient | /ambient NUMBER - activates or changes the ambient track (/ambient will pick a random track)



 --- Movement and General ---
 /on - turns ON the movement
 /off - turns OFF the movement
 /reset - turns ON the movement and restarts the position to default

 /skillsoff - turns OFF all the MAJOR SKILLS
 /reboot - reboots the chip, as if it just spawned
 /su PLAYER - changes user to PLAYER (/su reverts back to the original owner)




 ---- Major Skills ----
 ----------------------

 ::: Snake :::
 (With this skill all the OWNER's props with the model Helicopter Bomb will spin above the player's head and attack the CROSSHAIRS when the CTRL key is pressed)
 (If a player was targeted by this skill, the props will stop attacking the CROSSHAIRS position to attack the targeted player)
 (Many thanks to 'EXO's Propsnake' for providing part of the code)

 /snkon - activates Snake
 /snkoff - deactivates Snake
 /snkreset - resets Snake
 /snk PLAYER - assigns PLAYER as Snake's target (will sometimes fail, try /snkoff first)
 /snks - activates Snake and spawns 10 HeliBombs (needs 'wire_expression2_concmd 1')



 ::: Necromancer :::
 (This skill allows the player to animate a Ragdoll to attack someone)
 (I gotta thank 'Bone Example: Zombie (by Shoffing)' from the GMod's Wiki for providing the base code)

 /necro PLAYER - assigns PLAYER as NECROMANCER's target and activates it [CROSSAIRS ON THE RAGDOLL]
 /necroon - activates NECROMANCER
 /necrooff - deactivates NECROMANCER
 /necroset PLAYER - sets PLAYER as NECROMANCER'S target on that ragdoll with the ragdoll still inactive [CROSSAIRS ON THE RAGDOLL]
 /necrochange PLAYER - sets PLAYER as the new NECROMANCER's target



 ::: Psychokinesis :::
 (A skill that allows the player to pick up a Prop and throw it around, use it as a boomerang and increase its mass for maximum throwing power)
 (Thanks to 'Roflc0pter's Snake E2' for the concept)
 (E key to select prop/grab prop/release prop || Mouse1 to throw || Mouse2 to recall selected prop/increase its mass)
 ('say !brl' should be binded to a Keyboard Key for easy explosive barrel spawn)

 /kinesis - activates PSYCHOKINESIS
 /kinesisoff - deactivates PSYCHOKINESIS
 /kinesisreset - resets PSYCHOKINESIS
 mmss - increases the selected prop's mass to MAX
 !haax - DR.HAAX sounds
 !haaxoff - deactivates DR.HAAX sounds



 ::: Revenge :::
 (This skill will kill someone who kills you, with the Bomb Assassination SKill)
 (Props to 'Fairy by MURDATS' for the concept)

 /revenge - activates REVENGE MODE and avenges OWNER's last death last death
 /revengeon - activates REVENGE MODE without avenging the OWNER's last death
 /revengeoff - deactivates REVENGE MODE



 ::: Aggregate :::
 (This one allows you to make explosive barrels Aggregate in a spot)
 (All credit goes to EXO for his 'PropSplosion E2'. I just merged it with this drone because it was such a cool E2)
 (E key to make the barrels Aggregate in the CROSSHAIRS spot)
 (BROTIP: Spawn barrels in a distant location with the '!brls', activate the skill '/agg',
  press E on the Target Location, wait until the barrels start flying up, and then E again to make them rain)

 /agg - activates AGGREGATE
 /aggoff - deactivates AGGREGATE
 /aggp PLAYER - set AGGREGATE's Target to PLAYER



 ::: Blind:::
 (Covers the target's field of vision)

 /blind PLAYER - blinds PLAYER
 /unblind - deactivates the Blind Major Skill



 ::: Locate :::
 (Creates a holo HUD pointing the location of the selected players or E2 Chips)
 (Thx to Failcake's E2 Finder, for providing the brilliant concept & the color change by distance method, its pretty neat)
 (Red/Orange is for normal players and E2 Chips, Green for Steam Friends and Blue for admins)

 /locate PLAYER - activates and adds PLAYER to the Locate List
 /locate e2 /or/ friends - activates, lists and locates E2 Chips or Steam Friends
 /loca PLAYER - activates and locates PLAYER (and only PLAYER)
 /locateoff - resets the list and deactivates the LOCATE Major Skill



 ::: NPC Army :::
 (Allows the user to mobilize a group of NPCs to his will)
 (Press E to make the army go to a spot on the map near them)
 (They will attack anyone you attack)

 /army - activates the Army
 /armyoff - deactivates the Army
 /armyfollow - toggles the Follow mode
 /army WEAPON - gives WEAPON to the army (ex: /army pistol)
 /armyattack PLAYER - makes the Army target PLAYER

:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
