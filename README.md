Hey There, I’m @TheMagicalBlob. I Make Mods/Cheats For PS4 Games.
I Mostly Screw With Debug Stuff

You Can Find Me On Discord At TheMagicalBlob#9808, Or On Youtube At https://www.youtube.com/channel/UCqYd1YadQvjnAj_LfHK4iEQ 


Below Is A (Poory Formatted For Now) List Of Patches I've Made Over The Years For Various Games. This Is My Own Personal List, So Excpect The Occasional Random Comment Or Half-Added Patch

**(F; == Find | R; == Replace With)**

**(M) Means The Address Is For Memory Editors Like PS4Cheater**

                                                                                               -------------------------
                                                                                               |Mafia II 1.00 CUSA00000|
                                                                                               -------------------------
Shooting Fills Clip 12CCD84 (reloading drains ammo)

Drain; 017010 { 0x01, 0x70, 0x10 }
Fill; 297010 { 0x29, 0x70, 0x10 }
-----------------------------------
Infinite Cash 0x801E04A7

F; 4C29F1 { 0x4C, 0x29, 0xF1 }
R; 909090 { 0x90, 0x90, 0x90 }
------------------------------
Buying Things Raises Cash 0x801E04A7 [mov [r14+r12], rcx] The Fuck Is This?

F; 4C29F1 { 0x4C, 0x29, 0xF1 }
R; 4C01F1 { 0x4C, 0x01, 0xF1 }
------------------------------
Infinite Ammo 150C574

Drains; 44 89 60 10 { 0x44, 0x89, 0x60, 0x10 }
Infinite; 44 89 68 10 { 0x44, 0x89, 0x68, 0x10 }

HP 14C288D (effects everyone for fuck sake. again.)
Mortal; C5-FA-5C-C0
Inf; C5-F2-5C-C9
------------------------------------------------------------------------------------------------------------
Super Reload 150C57E

F; 41 89 DD { 0x41, 0x89, 0xDD }
R; 41 89 DC { 0x41, 0x89, 0xDC }
--------------------------------

                                                                                                              --------------------------
                                                                                                              |Mafia III 1.00 CUSA03617|
                                                                                                              --------------------------
Infinite Cash 0x3402F07
Drain; 89 B0 D8 02 00 00 {0x89, 0xB0, 0xD8, 0x02, 0x00, 0x00}
Inf; 90 90 90 90 90 90 {0x90, 0x90, 0x90, 0x90, 0x90, 0x90}



Infinite Clip Ammo 0x2A1E30B
Drain; 89 41 18 { 0x89 0x41, 0x18 }
Infinite; nop { 0x90, 0x90, 0x90 }

Infinite Reserve Ammo 0x2A1C54D
Drain; 89 70 04 { 0x89, 0x70, 0x04 }
Infinite; nop { 0x90, 0x90, 0x90 }

Borderlands 3 1.00
-----------------
Float - Unknown Initial: 0x4DCDAC8 vmovss [rbx+0xa0], xmm1
Drain: C5-FA-11-8B-A0-00-00-00
Infinite: C5-FA-11-93-A0-00-00-00
Always 1 HP (Helps Moze): C5-7A-11-83-A0-00-00-00 or C5-FA-11-B3-A0-00-00-00

1.26

Infinite Clip Ammo (OG Clip Drain Addr 0x5838EF4)[Code List.txt](https://github.com/TheMagicalBlob/TheMagicalBlob/files/9114551/Code.List.txt)

Address 5838EC2
Drain; 0x45, 0x29, 0xF4
Infinite; 0x45, 0x29, 0xF6

Shooting Increases Stach Ammo
off;
on; 

Infinite Stash Ammo
Address;
Drain; 
Infinite;


                                                                                               ----------------------------
                                                                                               |Red Dead Redemption 2 1.29|
                                                                                               ----------------------------

Reloading Restores Ammo 0x oof
F; 
-
R; 

// fuck forgot to even add it 
                                                                                               ----------------------
                                                                                               |Resident Evil 3 1.00| CUSA14123 & CUSA14168
                                                                                               ----------------------
No Reload

F; 0x223203A 0x89, 0x51, 0x20
R; 0x223203A 0x90, 0x90, 0x90
some cloth physics float, idk 0x53DB75C(M)
-------------------------------------------------------

Borderlands 3
Infinite Ammo
Offset;
Drain;
Infinite;
-
Infinite Health (Float - 0x4DCDAC0 vmovss [rbx+0xa0], xmm1 - C5-FA-11-8B-A0-00-00-00)
Offset; 0x4DCDAC3
Drain; 0x8B
Infinite; 0x93
Always 1 HP (Helps Moze): 0xB3

                                                                                                        -----------------------------
                                                                                                        |The Last of Us Part II 1.00|
                                                                                                        -----------------------------
t21

Debug Mode

F; 31 c0 eb 49 4c
R; b0 01 eb 49 4c
------------------
Disable Weapon sway on startup

F; c6 05 ac 8b 65 02 00
R; c6 05 8f 8b 65 02 01
------------------------
Depth of Field Disabled on startup

F; c6 05 54 1a 60 02 00
R; c6 05 53 1a 60 02 01
------------------------
L3 + Triangle to FPS toggle

F; 41 8a 84 24 aa 3a 00 00 89 c1 80 f1 01 41 88 8c 24 aa 3a 00 00
R; 41 8a 84 24 b8 3a 00 00 89 c1 80 f1 01 41 88 8c 24 b8 3a 00 00
------------------------------------------------------------------
Show Save Slot On Startup

F; c6 05 d8 af 2f 04 00
R; c6 05 e8 af 2f 04 01
------------------------
Disable Build Text On Startup

F; 66 41 c7 85 c4 3a 00 00 01 01
R; 66 41 c7 85 c4 3a 00 00 00 00
---------------------------------
Debug Menu Transparency Float (This Makes It Transparent)

F; B8 0A 00 00 00 9A 99 59 3F
R; B8 0A 00 00 00 00 00 00 00
------------------------------
Menu Scale Float

F; C7 05 65 85 EE 02 9A 99 19 3F
R; C7 05 65 85 EE 02 cd cc 4c 3f
---------------------------------
Draw World Axes To Novis 
(second is just for the string)

F; 48 8d 05 8b 45 e0 01
R; 48 8d 05 9e ce ec 00
-- 
F; 48 8d 35 20 4c 81 00
R; 48 8d 35 1e 20 75 00
------------------------ T2 1.00 Offsets

Disable Debug Rendering; 0x110693FAAA(Useless)
Debug Menu 0x110693FAA1
Menu Background Opacity: 0x32231E
Menu Scale: 0x32468A8
Novis: 0x341622c

                                                                                                       -----------------------------
                                                                                                       |The Last of Us Part II 1.07|
                                                                                                       -----------------------------
t27

007dd9ba camera shit Ghid
Debug Mode

F; 31 c0 eb 4c 4c
R; b0 01 eb 4c 4c
------------------
L3 & Triangle To Debug Mode Toggle

F; 74 45 67 80 3c 25 16 00 40 00 01 74 3a 41 8a 84 24 a1 3a 00 00 89 c1 80 f1 01 41 88 8c 24 a1 3a 00 00
R; 74 45 67 80 3c 25 16 00 40 00 01 74 3a 41 8a 84 24 a1 3a 00 00 89 c1 80 f1 01 41 88 8c 24 a1 3a 00 00
---------------------------------------------------------------------------------------------------------
No More Render Pause Or Reload Ingame Shaders Options

F; 48 8d 15 b8 f6 83 00
R; 48 e9 ca 02 00 00 00
------------------------
No More Debug "Paused" Icon

F; 74 10 41 c6 85 aa 3a 00 00 01 41 c6 85 b8 3a 00 00 01
R; 75 10 67 c6 05 8f 40 07 03 00 41 c6 85 b8 3a 00 00 00
---------------------------------------------------------
Movie/Audio Frame Sync Threshold To Non-ADS FOV

F: 48 8d 15 bf da e9 00
R: 48 8d 15 bf 4b e9 00
------------------------
Fixed GPU Frame Delay To X Sensitivity 1

F; 48 8d 15 54 77 e9 00
R; 48 8d 15 20 2b 68 01
------------------------
Game Frame Headstart To X Sensitivity 2

F; 48 8d 15 a0 9a dc 01
R; 48 8d 15 ac 28 68 01
------------------------
Msg Con Scale To Menu Scale

F; 48 8d 05 29 ea e7 00
R; 48 8d 05 99 df 0b 01
------------------------
Msg Con Scale To Fov Slider

F; 48 8d 05 29 ea e7 00
R; 48 8d 05 d1 11 ea 00
------------------------
Completion Text To Build Text

F; 00 43 48 45 41 54 45 44 00 43 6F 6D 70 6C 65 74 69 6F 6E 20 25 2E 31 66 25 25 25 73 20 25 73 0A 00 28 25 64 20 2F 20 25 64 29 20 25 73 0A 00 46 61 64 65 20 25 2E 33 66 0A 00 56 6F 6C 20 53 61 6D 70 6C 65 73 20 25 75 0A 00
R; 00 44 65 62 75 67 20 20 00 54 32 20 44 65 76 20 4D 65 6E 75 20 2B 20 20 20 20 20 20 20 20 20 0A 00 42 75 69 6C 64 20 35 2E 36 36 20 20 20 00 20 20 20 20 20 20 20 20 20 0A 00 20 20 20 20 20 20 20 20 20 20 20 20 20 20 0A 00
-------
Vol Samples And Fade Text 

F; 00 46 61 64 65 20 25 2E 33 66 0A 00 56 6F 6C 20 53 61 6D 70 6C 65 73 20 25 75 0A 00
R; 00 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 00
-------
Debug Menu Transparency Float (This Makes It Transparent)

F; B8 0A 00 00 00 9A 99 59 3F
R; B8 0A 00 00 00 00 00 00 00
------------------------------
Allow Screen Tear

F; c6 05 73 b2 d3 02 00
R; c6 05 73 b2 d3 02 01
------------------------
Allow Screen Tear Through Loading Screens

F; c6 05 45 c1 d3 02 00
R; c6 05 45 c1 d3 02 01
------------------------
No Screan Tear Change After Loading? needs more oned nop'd

F; c6 05 45 c1 d3 02 00
R; 90 90 90 90 90 90 90
------------------------
Show Save Slot On start-up

F; 49 8d 46 28 c6 05 5f 95 59 02 00
R; 49 8d 46 28 c6 05 6d 95 59 02 01
------------------------------------
Show Game Completion (Needs Save Slot On Screen)

F; 48 c7 05 39 c8 59 02 00 00 00 00
R; 48 c7 05 3d c8 59 02 01 00 00 00
------------------------------------
lut gamma curve to NPC Scale ( Look For "Fell Out Of The World" )

F; 00 48 64 72 20 6C 75 74 20 67 61 6D 6D 61 20 63 75 72 76 65 00
R; 00 43 68 61 6E 67 65 20 4E 50 43 20 53 63 61 6C 65 20 20 20 00
-
F; 48 8d 15 cb be dc 01
R; 48 8d 15 1b 79 42 02
------------------------
Menu Scale

F; c7 05 b5 70 ee 02 9a 99 19 3f
R; c7 05 b5 70 ee 02 cd cc 4c 3f
---------------------------------
FPS Mode Change

F; 41 c7 85 b4 3a 00 00 00 00 00 00 FPS Only
R;                       1          Verbose MS
R;                       2          Verbose Percent
R;                       3          Minimalistic
----------------------------------------------------
Verbose Addatives Bytes

F; 41 c7 85 b9 3a 00 00 01 01 01 01
R; 41 c7 85 b9 3a 00 00 01 00 00 01
------------------------------------
Broken GPU Thing Disabled (There's A Patch From illusion To Fix This)

F; 41 c7 85 b9 3a 00 00 01 01 01 01
R; 41 c7 85 b9 3a 00 00 01 01 01 00
---------------------------------
Msg con scale 0.7 on boot

F; 00 00 00 00 10 00 00 00 00 00 00 3f
R; 00 00 00 00 10 00 00 00 00 00 34 3f
---------------------------------------------------
L3 + Triangle to FPS toggle

F; 41 8a 84 24 aa 3a 00 00 89 c1 80 f1 01 41 88 8c 24 aa 3a 00 00
R; 41 8a 84 24 b8 3a 00 00 89 c1 80 f1 01 41 88 8c 24 b8 3a 00 00
---------------------------------
Enable Stat Posting On Boot

F; 66 41 c7 85 ec 3e 00 00 00 00
R; 66 41 c7 85 ed 3e 00 00 01 00
---------------------------------
Upscale Merge Threshold To NPC Scale

F; 00 55 70 73 63 61 6C 65 20 4D 65 72 67 65 20 54 68 72 65 73 68 6F 6C 64 00
R; 00 43 68 61 6E 67 65 20 4E 50 43 20 53 63 61 6C 65 20 20 20 20 20 20 20 00
-
F; 48 8d 15 d3 7b dc 01
R; 48 8d 15 1b 36 42 02
------------------------

{MsgCon +}


Culling Toggle [Option 1]

Addr
F; 48 8d 05 4f 35 dd 01
R; 48 8d 05 3e 11 e9 00
---
Str
F; 48 8d 35 a4 9f 81 00
R; 48 8d 35 81 31 75 00
------------------------
Prog Pause On Menu Open [Option 2]

F; 49 8d 8d aa 3a 00 00
R; 48 8d 0d ef 15 0c 01
------------------------
Menu Right Align [Option 3]

F; 48 8d 05 e7 33 dd 01
R; 48 8d 05 67 17 0c 01
------------------------
Debug Menu Bold Text [Option 4]

F; 49 8d 8d a9 3a 00 00
R; 48 8d 0d 82 14 0c 01
---
On By Default

F; c6 05 9a 71 ee 02 00
R; c6 05 9a 71 ee 02 01
------------------------
Swap O With Square In Debug [Option 4?]

F; 00 55 73 65 20 56 65 72 74 65 78 20 4C 69 73 74 20 28 4E 6F 20 49 6E 64 69 63 65 73 29 00
R; 00 53 77 61 70 20 4F 20 57 69 74 68 20 53 71 75 61 72 65 20 49 6E 20 44 65 62 75 67 20 00
-
F; 48 8d 05 99 d1 e8 00
R; 48 8d 05 36 d8 0b 01
------------------------------
O And Square Swapped In Debug Meny By Default

F; 66 c7 05 8c 71 ee 02 00 00
R; 66 c7 05 8c 71 ee 02 01 00
------------------------------
[Memory Plus V2] W.I.P.

-- Remove All Weapons
F; 48 8d 35 41 11 73 02
R; 48 8d 35 f9 f6 78 02
---keep vsync as is?
F; 48 8d 05 d8 bc 04 03
R; 48 8d 05 09 45 14 00
-- 
F; 
R; 
---
F; 
R; 
-- Novis
F; 48 8d 35 c3 0e 73 02
R; 48 8d 35 a8 1d 73 02
---
F; 48 8d 05 89 bb 04 03
R; 48 8d 05 73 fd e6 02
---
F; 
R; 
---
F; 
R; 
---
F; 
R; 
---
F; 
R; 
---
F; 
R; 
---
F; 
R; 
---
F; 
R; 
------------------------ T2 1.07 Offsets

Invincible Player
0x35aed44 G

Novis / Disable All Visibility: Ghid 0x301602c Memory 0x341602C  str 0x28d8025 / 0x2cd8025


byte;
Debug Mode; 0x11069DFAA1
Menu Bold Text: 0x32467b8
Menu Pause: 0x032467b9
Menu Pause: On Exit 0x032467ba (With Triangle or Touchpad)
Debug PAUSED Icon: 0x32467bb
Swap O and Square: 0x32467Bd
Menu Right Align: 0x032467be
Build info Display Byte: 0x1CB7B2 offset HEX 48 b8 00 00 00 00 01 01 00 01
Menu Background Opacity: 0x0035f6ed
Main Camera Feild of View: 0x3029a00
FPS Text Size Float: 0x28919a0
? yellow debug text and build text position: 0x28919a4
FPS Text Colour Red: 0x28919b8
FPS Text Colour Yellow: 0x2C919BC
Something To Do With FPS Text, Not Sure: 0x289199c

float;
Menu Scale: 0x32467c8
Look Sensitivity1 X: 0x3811B78
Look Sensitivity2 X: 0x3811B80
NPC Scale: 0x45b3bcc
Jump Height/Length: 0x11087123B0
debug menu code spot: 652b90

T2 1.07 Functions
Remove All Player Weapons: 0x169f610
Give All Guns And Upgrades: 0x0f12250



                                                                                                       -----------------------------
                                                                                                       |The Last of Us Part II 1.09|
t29                                                                                                    -----------------------------


Enhanced Debug Menu (Eboot.bin addr) | Strings 2DF3B50


________________________________________________
Custom String Offsets Log To Avoid Overlapping:

String                   .elf addr   ghidra addr
Disable All Visibility | 0x2DF3B50 | 0x3DEFB50



Adjust Menu Scaling | ? | ?
________________________________________________
Write Values:

Disable Debug Rendering { 0x25B0BAA } | { 0x41, 0xc6, 0x85, 0xaa, 0x3a, 0x00, 0x00, 0x00 }
Enable Stat Posting { 0x25B0BB2 } | { 0x41, 0xc6, 0x85, 0xed, 0x3e, 0x00, 0x00, 0x01 }
Show Save Slot On-Screen { 0x25B0BBA } | { 0xc6, 0x05, 0x06, 0x3c, 0xf4, 0x01, 0x01 }
Show Game Completion { 0x25B0BC1 } | { 0xc6, 0x05, 0x03, 0x3c, 0xf4, 0x01, 0x01 }
Align Debug Menus Right { 0x25B0BC8) } | { 0xc6, 0x05, 0x6f, 0xda, 0xca, 0x00, 0x01 }
Swap Square And Circle In Debug { 0x25B0BCF } | { 0xc6, 0x05, 0x67, 0xda, 0xca, 0x00, 0x01 }
Debug Menu Shadowed Text { 0x25B0BD6 } | { 0xc6, 0x05, 0x5b, 0xda, 0xca, 0x00, 0x01 }
Disable All Visibility { 0x25B0BDD } | { 0xc6, 0x05, 0x48, 0xd2, 0xa9, 0x00, 0x01 }
Prog Pause On Menu Open { 0x25B0BE4 } | { 0xc6, 0x05, 0x4e, 0xda, 0xca, 0x00, 0x00 }
Prog Pause On Menu Close { 0x25B0BEB } | { 0xc6, 0x05, 0x48, 0xda, 0xca, 0x00, 0x00 }
Set Menu Scale To 0.7 { 0x25B0BF2 } | { 0xc7, 0x05, 0x4c, 0xda, 0xca, 0x00, 0x33, 0x33, 0x33, 0x3f }
Set Menu Opacity To 0.5 { 0x25B0BFC } | { 0xc7, 0x05, 0x3e, 0xda, 0xca, 0x00, 0x00, 0x00, 0x00, 0x3f }
Disable FPS { 0x25B0C06 } | { 0x41, 0xc6, 0x85, 0xb8, 0x3a, 0x00, 0x00, 0x01 }
Set FPS Disaplay Mode To 3 { 0x25B0C0E } | { 0x41, 0xc7, 0x85, 0xb4, 0x3a, 0x00, 0x00, 0x03, 0x00, 0x00, 0x00 } // 0 FPS | 1 Verbose | 2 Verbose Percent | 3 Minimal
________________________________________________
Debug Rendering Toggle To FPS Toggle [L3 & Triangle] { 0x1C45085, 0x1C45092 } | 0xB8

F; 41 8a 84 24 aa 3a 00 00 89 c1 80 f1 01 41 88 8c 24 aa 3a 00 00
R; 41 8a 84 24 b8 3a 00 00 89 c1 80 f1 01 41 88 8c 24 b8 3a 00 00
------------------------------------------------------------------
Draw World Axes To Novis

- Change Byte
F; 48 8d 05 5f 16 9c 01 { 0x25AE9DA } | { 0x4E, 0xF4, 0xA9, 0x00 }
R; 48 8d 05 4e f4 a9 00

- Change String Offset To Fit Larger New String
F; 48 8d 35 7a 59 50 00 { 0x25AE990 } | { 0xbc, 0x51, 0x84 }
R; 48 8d 35 bc 51 84 00

- Add String            { 0x2DF3B50 } | { 0x44, 0x69, 0x73, 0x61, 0x62, 0x6C, 0x65, 0x20, 0x41, 0x6C, 0x6C, 0x20, 0x56, 0x69, 0x73, 0x69, 0x62, 0x69, 0x6C, 0x69, 0x74, 0x79 }
-------------------------
Msg Con Scale To Debug Menu Scale

F; 48 8d 05 39 cd a8 00 { 0x25B231B } | { 0x29, 0xc3, 0xca, 0x00 }
R; 48 8d 05 29 c3 ca 00
-
F; 48 8d 35 7f 25 50 00 { 0x25B2279 } | { 0xea, 0x18, 0x84, 0x00 }
R; 48 8d 35 ea 18 84 00

-                       { 0x2DF3B67 } | { 0x41, 0x64, 0x6A, 0x75, 0x73, 0x74, 0x20, 0x44, 0x65, 0x62, 0x75, 0x67, 0x20, 0x4D, 0x65, 0x6E, 0x75, 0x20, 0x53, 0x63, 0x61, 0x6C, 0x65 } 
------------------------
Increase Debug Menu Scale To Match Previous Games (Or In Other Words, Make It F*cking Visible...)

F; c7 05 75 97 ab 02 9a 99 19 3f { 0x7A4ECF } | { 0xcd, 0xcc, 0x4c, 0x3f } // CHANGE THIS TO 0.70!!!
R; c7 05 75 97 ab 02 cd cc 4c 3f
---------------------------------

Good Spot For Strings
0x2DF3B50(.elf addr)

Tlou2 1.09 Offsets - All (M)

byte;
Draw Stationary vs Moving Widgets: 0x3A28f0c
Debug Mode: 0x11069DFAA1
Novis: 0x3449e2c
Debug Menu Shadowed Text: 0x365A638
Debug Pause On Menu Open: 0x365A639
Debug Pause On Menu Close: 0x365A63A (Unless Closed With L3 Combo)
Swap Square And Circle In Debug: 0x365A63D
Align Debug Menus Right: 0x365A63E
Show Save Slot On Screen: 0x48F07C7
Show Game Completion: 0x48F07CB
Debug Pause: 0x365A689

float;
Debug Menu Background Opacity: 0x365A644
Debug Menu Scale: 0x365A648
IDK, Screws With The Debug Text Colours: 0x3A28f40

                                                                                                        -----------------------------------------
                                                                                                        |The Last of Us Remastered 1.10/1.11 557|
tr111                                                                                                   -----------------------------------------

Debug Mode (Pre-Boot Only)

F; c6 87 81 2e 00 00 00
R; c6 87 81 2e 00 00 01
-------------------------
Debug Mode During Or After Boot 1.09 to 1.11

Addr; 0xE30D35 {0xA30D35 + 400000}
--
On; 75 12 41 80 bd 81 2e 00 00 01 74 08 41 80 b5 81 2e 00 00 01
--
Off; 75 12 41 80 bd 81 2e 00 00 00 74 08 41 80 b5 81 2e 00 00 01
--
Default; 74 12 41 80 bd 81 2e 00 00 00 74 08 41 80 b5 85 2e 00 00 01
---------------------------------------------------------------------
L3 & Triangle To Debug Mode Toggle 1.09 to 1.11

Addr: 0xE30FC9 {0xA30FC9 + 400000}
--
F; 80 b8 81 2e 00 00 00 74 0e 48 8b 85 70 ff ff ff 80 b0 85 2e 00 00 01
--
R; 80 3d 98 bf ba 00 01 74 0e 48 8b 85 70 ff ff ff 80 b0 81 2e 00 00 01
------------------------------------------------------------------------
L3 & Triangle To FPS Toggle

F; 80 b0 85 2e 00 00 01
R; 80 b0 87 2e 00 00 01
------------------------------
Designer Mode to Spawn Horse

F; 48 8d 15 d1 fa ff ff 48 89 c3 48 8d 35 e9 33 02 01
R; 48 8d 15 e1 54 ff ff 48 89 c3 48 8d 35 1e 22 02 01
------------------------------------------------------
Player2 to Manual Camera For 1.10

F; 00 64 72 61 77 2D 73 70 6C 61 73 68 2D 73 63 72 65 65 6E 00
R; 00 4D 61 6E 75 61 6C 20 43 61 6D 65 72 61 20 20 20 20 20 00
-------
F; 48 8d 15 22 fc ff ff 48 89 c3 48 8d 35 6a da bc 00
R; 48 8d 15 82 49 b2 ff 48 89 c3 48 8d 35 f9 a3 b7 00
------------------------------------------------------
Debug Text (5.08)

F; 00 4E 4F 20 53 41 56 45 20 47 41 4D 45 20 41 43 54 49 56 45 00 41 55 54 4F 2D 53 41 56 49 4E 47 20 54 4F 20 50 52 4F 46 49 4C 45 3F 00 55 53 45 52 20 54 4F 20 43 48 4F 4F 53 45 20 41 55 54 4F 2D 53 41 56 45 20 53 4C 4F 54 00 41 55 54 4F 2D 53 41 56 45 20 54 4F 20 4C 41 54 45 53 54 20 54 41 53 4B 00 41 55 54 4F 2D 53 41 56 45 20 53 4C 4F 54 20 25 64 00 50 4C 41 59 47 4F 20 53 55 53 50 45 4E 44 45 44 0A 00 50 4C 41 59 47 4F 20 41 43 54 49 56 45 0A 00 46 61 64 65 20 25 2E 33 66 0A 00 56 6F 6C 20 53 61 6D 70 6C 65 73 20 25 75 0A 00
R; 00 4C 61 75 6E 63 68 69 6E 67 20 47 61 6D 65 2E 2E 2E 20 20 00 41 55 54 4F 2D 53 41 56 49 4E 47 20 54 4F 20 50 52 4F 46 49 4C 45 3F 00 55 53 45 52 20 54 4F 20 43 48 4F 4F 53 45 20 41 55 54 4F 2D 53 41 56 45 20 53 4C 4F 54 00 41 55 54 4F 2D 53 41 56 45 20 54 4F 20 4C 41 54 45 53 54 20 54 41 53 4B 00 20 20 4D 61 67 69 63 61 6C 20 20 00 00 00 00 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 42 75 69 6C 64 3A 20 35 2E 30 38 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 0A 00
-------
-1.10 Crash Replace v1.0- (912 to ada)

F; 00 43 72 61 73 68 2E 2E 2E 00 43 72 61 73 68 00 43 72 61 73 68 20 54 68 65 20 47 61 6D 65 00 43 72 61 73 68 20 54 68 65 20 47 61 6D 65 20 28 41 73 73 65 72 74 69 6F 6E 29 00 43 72 61 73 68 20 54 68 65 20 47 61 6D 65 20 28 52 65 63 75 72 73 69 6F 6E 29 00 43 72 61 73 68 20 54 68 65 20 47 61 6D 65 20 28 44 65 61 64 6C 6F 63 6B 29 00 43 72 61 73 68 20 54 68 65 20 47 61 6D 65 20 28 53 74 61 63 6B 20 4F 76 65 72 66 6C 6F 77 29 00 43 72 61 73 68 20 54 68 65 20 47 61 6D 65 20 28 4E 6F 20 45 6D 61 69 6C 29 00 43 61 6C 6C 20 43 72 61 73 68 20 52 65 70 6F 72 74 20 46 75 6E 63 00
R; 00 45 78 74 72 61 2E 2E 2E 00 45 78 74 72 61 00 43 72 61 73 68 20 54 68 65 20 47 61 6D 65 00 43 72 61 73 68 20 54 68 65 20 47 61 6D 65 20 28 41 73 73 65 72 74 69 6F 6E 29 00 43 72 61 73 68 20 54 68 65 20 47 61 6D 65 20 28 52 65 63 75 72 73 69 6F 6E 29 00 45 6E 61 62 6C 65 20 4D 65 6E 75 20 50 61 75 73 65 20 20 20 20 20 20 20 20 00 4D 65 6E 75 20 52 69 67 68 74 20 41 6C 69 67 6E 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 00 45 6E 61 62 6C 65 20 44 65 62 75 67 20 50 41 55 53 45 44 20 49 63 6F 6E 20 00 53 77 61 70 20 43 69 72 63 6C 65 20 41 6E 64 20 53 71 75 61 72 65 00
-------
F; bf a0 00 00 00 e8 e4 26 c1 00 48 89 c3 48 8d 35 91 3d 02 01 48 8d 15 23 03 00 00 31 c9 45 31 c0 48 89 df e8 e6 de 9b 00 4c 89 f7 48 89 de e8 6b f3 9b 00 bf a0 00 00 00 e8 b1 26 c1 00 48 89 c3 48 8d 35 6d 3d 02 01 48 8d 15 10 03 00 00 31 c9 45 31 c0 48 89 df e8 b3 de 9b 00 4c 89 f7 48 89 de e8 38 f3 9b 00 bf a0 00 00 00 e8 7e 26 c1 00 48 89 c3 48 8d 35 55 3d 02 01 48 8d 15 6d 03 00 00 31 c9 45 31 c0 48 89 df e8 80 de 9b 00 4c 89 f7 48 89 de e8 05 f3 9b 00 bf a0 00 00 00 e8 4b 26 c1 00 48 89 c3 48 8d 35 3d 3d 02 01 48 8d 15 4a 03 00 00 31 c9 45 31 c0 48 89 df e8 4d de 9b 00 4c 89 f7 48 89 de e8 d2 f2 9b 00 bf a0 00 00 00 e8 18 26 c1 00 48 89 c3 48 8d 35 24 3d 02 01 48 8d 15 47 03 00 00 31 c9 45 31 c0 48 89 df e8 1a de 9b 00 4c 89 f7 48 89 de e8 9f f2 9b 00 bf 90 00 00 00 e8 e5 25 c1 00 48 89 c3 48 89 df e8 da aa 9b 00 4c 89 f7 48 89 de e8 7f f2 9b 00 bf a0 00 00 00 e8 c5 25 c1 00 48 89 c3 48 8d 35 f1 3c 02 01 48 8d 15 04 03 00 00 31 c9 45 31 c0 48 89 df e8 c7 dd 9b 00 4c 89 f7 48 89 de e8 4c f2 9b 00 bf a0 00 00 00 e8 92 25 c1 00 48 89 c3 48 8d 35 d8 3c 02 01 48 8d 15 f1 02 00 00 31 c9 45 31 c0 48 89 df e8 94 dd 9b 00 4c 89 f7 48 89 de e8 19 f2 9b 00 bf a0 00 00 00
R; bf a0 00 00 00 e8 e4 26 c1 00 48 89 c3 48 8d 35 f5 9a 0c 01 48 8d 15 4a 78 4b 01 48 89 df e8 eb ae 9b 00 49 8b fe 48 89 de e8 70 f3 9b 00 bf a0 00 00 00 e8 b6 26 c1 00 48 89 c3 48 8d 35 a4 9d 0c 01 48 8d 15 13 78 4b 01 48 89 df e8 bd ae 9b 00 4c 89 f7 48 89 de 48 e8 41 f3 9b 00 bf a0 00 00 00 e8 87 26 c1 00 48 89 c3 48 8d 35 86 9d 0c 01 48 8d 15 e5 77 4b 01 48 89 df e8 8e ae 9b 00 49 8b fe 48 89 de e8 13 f3 9b 00 bf a0 00 00 00 e8 59 26 c1 00 48 89 c3 48 8d 35 4b 3d 02 01 48 8d 15 a0 9f 4f 01 48 89 df e8 60 ae 9b 00 49 8b fe 48 89 de 48 e8 e4 f2 9b 00 bf a0 00 00 00 e8 2a 26 c1 00 48 89 c3 48 8d 35 36 3d 02 01 48 8d 15 76 9f 4f 01 48 89 df e8 31 ae 9b 00 49 8b fe 48 89 de e8 b6 f2 9b 00 bf a0 00 00 00 e8 fc 25 c1 00 48 89 c3 48 8d 35 1e 85 0c 01 48 8d 15 08 63 4b 01 48 89 df e8 03 ae 9b 00 49 8b fe 48 89 de e8 88 f2 9b 00 bf a0 00 00 00 e8 ce 25 c1 00 48 89 c3 48 8d 35 fa 3c 02 01 48 8d 15 17 9f 4f 01 48 89 df e8 d5 ad 9b 00 49 8b fe 48 89 de 48 e8 59 f2 9b 00 bf a0 00 00 00 48 e8 9e 25 c1 00 48 89 c3 48 8d 35 b9 d1 0c 01 48 8d 15 fa be 7a 01 48 89 df e8 a5 ad 9b 00 49 8b fe 48 89 de 48 e8 29 f2 9b 00 49 8b fe e8 61 5b fd ff 90 90 90 90 90 90 90 90 bf a0 00 00 00
-------
-DoF-

Find; C6 83 70 01 00 00 01 C6 83 19 02 00 00 00 C6 83 1A
Replace; C6 83 71 01 00 00 00 C6 83 19 02 00 00 00 C6 83 1A
------------------------------------------------------------
Swap O and Triangle In Debug Menu on Start

F; c6 83 0d 04 00 00 00
R; c6 05 5d 31 e1 00 01
------------------------
[Misc.]

L3 + Triangle Toggle offset; 0xa30fd9
FPS/MS Location 0xc21c17
0x171 & 0x219 Pointers: c4fe
-----------------------------
T1 1.10 Offsets

Debug Mode: 0x114F536E81((M)...Obviously)
Point Mode: 0x0152618f
Wireframe See Through: 0x152618e
Culling: 0x1526197
Menu Right Align: 0x156897d
Menu Pause: 0x1568978
Debug Pause: 0x1568985
Pause on Menu Exit;  0x01568979
Pause Icon; 0x0156897a
Menu O And Square Swap: 0x156897C  string I used (Crash Report Func) 0x109277
----------------------------------

[Re-usable 1.10 Code For Those Who Are Curious]
}

  0006f637 90              NOP
  0006f638 bf a0 00        MOV        EDI,0xa0
           00 00
  0006f63d e8 de 19        CALL       FUN_00c81020                                     undefined FUN_00c81020()
           c1 00
  0006f642 48 89 c3        MOV        RBX,RAX
  0006f645 48 8d 35        LEA        RSI,[string]
           6a 33 02 01
  0006f64c 48 8d 15        LEA        RDX,[addr]
           44 6b 4b 01
  0006f653 48 89 df        MOV        RDI,RBX
  0006f656 e8 e5 a1        CALL       FUN_00a29840                                     undefined FUN_00a29840()
           9b 00
  0006f65b 49 8b fe        MOV        RDI,R14
  0006f65e 48 89 de        MOV        RSI,RBX
  0006f661 e8 6a e6        CALL       FUN_00a2dcd0                                     undefined FUN_00a2dcd0()
           9b 00
  0006f666 90              NOP

}
-------
}
bonuses 1.10

0006eaa7 49 8b fe        MOV        RDI,R14
0006eaaa e8 61 5b        CALL       FUN_00044610                                     undefined FUN_00044610()
         fd ff
}
-------


[illusions patches]
Motion Blur Off On Startup (1.00 or 1.10?)

F; 49 89 C6 41 C6 85 6D 01 00 00 01
--
R; 49 89 C6 41 C6 85 6D 01 00 00 00
--------------------------------------
T1R 1.10 - Fix Grounded Player Spawn Health

F; 41 8b 46 0c 89 43 30 41 8b 46 14
--
R; 41 8b 46 0c 89 5b 30 41 8b 46 14
------------------------------------------


                                                                                          ------------------------------------
                                                                                          |The Last of Us Remastered 1.00 552|
                                                                                          ------------------------------------
tr100


Debug Mode (Pre-Boot Only)

F; C6 87 81 2E 00 00 00
R; C6 87 81 2E 00 00 01
------------------------
Debug Mode During Or After Boot 1.00 [DEPRICATED, USE BYTE: 0x114ED32E81 0x01]

Addr; 0xC94B0A {0x894B0A + 400000}
--
On; 74 12 41 80 be 81 2e 00 00 00 74 08 41 80 b6 85 2e 00 00 01
--
Off; 75 12 41 80 be 81 2e 00 00 01 74 08 41 80 b6 81 2e 00 00 01
-----------------------------------------------------------------
Debug PAUSED Icon Disabled On Boot

F; c6 87 85 2e 00 00 00
R; c6 05 af 4a 5e 01 00
-----------------------
Debug Menu

F; F6 45 97 01 74 10
R; F6 45 97 01 75 10
---------------------
L3 & Triangle To FPS Toggle
   41 80 B6 82 2E 00 00 01
F; 41 80 b6 85 2e 00 00 01
R; 41 80 b6 87 2e 00 00 01
---------------------------
L3 + Traingle To Debug Mode Toggle 1.00
F; 74 12 41 80 be 81 2e 00 00 00 74 08 41 80 b6 85 2e 00 00 01
-- C94B19
R; 74 12 67 80 3d 7f b5 76 ff 01 74 08 41 80 b6 81 2e 00 00 01
---------------------------------------------------------------
Player2 to Manual Camera

F; 48 8d 35 d4 56 c6 00 48 8d 15 18 fc ff ff
R; 48 8d 35 16 e8 cb 00 48 8d 15 68 97 c0 ff
--(Both Of Them)
F; 45 64 69 74 20 53 75 6E 6C 69 67 68 74 20 70 6F 73
R; 4D 61 6E 75 61 6C 20 43 61 6D 65 72 61 20 20 20 20
------------------------------------------------------
Improved Screenshot Mode
F; 
R; 


 T1 1.00 Offsets
]
Debug Mode: 0x114ED32E81 0x01
-
No Reload: 0x1678340 or 2
-
Infinite Ammo: 0x1678341
-
Point Mode: 0x189935f
-
Wireframe See Through: 0x189935e
-
Culling: 0x1899367
-
Debug Pause: 0x15E671D
-
Menu Pause: 0x15E6710
-
Menu Right Align: 0x15E6715
-
Menu O And Square Swap: 0x15E6714
-
Power Save Mode 0x1B8FA16
-
Show Level Memory Stats fuck
-
Enable Version Check 0xA90E70(.bin) 0xE8CE70(M) [Result: HYBRID (default)]
Or
Enable Version Check [Result: DEBUG] 0xA90E81(.bin) 0xE8CE81(M) (set to 0x00. this is editing a return value. This Does Not Enable The Debug Mode, Don't Get Mixed Up)
-
Show Keyboard Thing 0x1B8FA15
]
                                                                                         ---------------------------------
                                                                                         |Uncharted: Drake's Fortune 1.00|
                                                                                         ---------------------------------
1492ea0

Debug Mode
F; 80 bf ba 39 00 00 00
R; 80 bf ba 39 00 00 01


Restore Devkit Submenus: (.elf/.bin offset, not ghidra)

[Misc Debug Text]
Load HYBRID Text: 0x354650 { 0xB0, 0x01 }
Load Build & Built Text: 0x2D40B0 { 0x00, 0x00 }                            
-Remove Useless "Build: " Text: 0x2D416C { 0x00, 0x00, 0x00, 0x00, 0x00 }
OR
-"Fix" Useless Build Text: 0x2D4158 { 0x14, 0xac, 0x67, 0x00 }
-Add The "Fixed" Text: 0x94ED70 { 0x42, 0x75, 0x69, 0x6C, 0x64, 0x3A, 0x20, 0x28, 0x55, 0x6E, 0x6B, 0x6E, 0x6F, 0x77, 0x6E, 0x20, 0x42, 0x75, 0x69, 0x6C, 0x64, 0x29 }

[Quick Menu]
Characters 0x2A7E07 0x85

[Dev Menu]
BP UCC... 0xE20E2 0x75
Rendering... 0xE2124 0x85 disables the skip of the Rendering... submenu
             0xE2164 0xe92f0d0000 skips the rest of the problematic code until I can cherry-pick more
Spawn Character... 0xE2EA0 0x85
Spawn Vehicle... 0xE35B9 0x85
Player Menu... 0x271F0C 0x85 (First Part)
Player Menu... 0x272160 0x85 (Second Part)
Collision... 0xE3739 0x75
Gameplay... 0xE379A 0x75
            0x1027BC 0x85
            0x104B46 0x85
Game Objects... 0xE37FB 0x75
Levels... 0xE385D 0x85
Npc... 0xE395D 0x75
Nav Mesh... 0xE39BE 0x75
Interactive Background... 0xE3A57 0x75
Actors... & Process... 0xE3A9D 0x75
Animation... 0xE3AAF 0x75
Water... 0xE3AC1 0x75
Fx... 0xE3B22 0x75
Camera... 0xE3B83 0x75 (Submenu Isn't Called So Nothing Opens)
Clock... 0xE3BBD 0x85
Physics... 0xE3E17 0x75
Audio... 0xE4032 0x85
Particles... & Particles (PS3)... 0xE52F1 0x75 (Crashes, Needs Fixing)
Language... 0xE536D 0x85
Menu... 0xE3E7B 0x85

Good Spot For Strings: 0x94ED50 (.elf)

All (M)
? 0xD97B42
? 0xD98B19
? 0xD98974
Disable Debug Rendering 0xD98971
Disable FPS; 0xD98970
Debug Menus; D989CC
Task & Version Display; 0xD97B41
Debug Pause; D97B8C

                                                                                         ---------------------------------
                                                                                         |Uncharted 2: Among Thieves 1.00|
                                                                                         ---------------------------------
Debug Mode 0x1EB296(.elf)

F; 80 bf ba 39 00 00 00
R; 80 bf ba 39 00 00 01
------------------------

Good Spot To Put Strings lol; 0x1530672 (M)
Debug Menus; 0x127149C (byte) (M)
Some Debug Menus Text Scale; 0x1264874 (float) (M)
Paused Icon H Scale; 0xF501C4 (float) (M)

[Quick Menu]    Offset|Data
Actor Viewer... 0x6C9C|0x1C
                0x6D5E|0xE900000000

[Dev Menu]        (Offset) (Data)
Complete Tasks... 0x436CEE 0x1C
                  0x436D71 0xE900000000

Rendering... BP Rendering... System... 0x1C4708 0x1C000000
                                       0x1C4C60 0xE900000000

[Uncharted 2 PS3 1.00]
Fix Bin Files... Submenu 0x90ce68
F; 7f e1 08 08 4b ff fd dc 38 7d 00 34
--
R; 60 00 00 00 4b ff fd dc 38 7d 00 34


? 0x12705CA
? 0x1271448
? 0x1271434
Disable Debug Rendering; 0x1271432
Disable FPS; 0x1271431
Debug Mode; 0x127149C
Task, Version, And Timer Display; 0x12705C9
? 0x1270614
                                                                                         -------------------------------------
                                                                                         |Uncharted 3: Drake's Deception 1.00|
                                                                                         -------------------------------------
Debug Mode

F; 80 bf ba 39 00 00 00
R; 80 bf ba 39 00 00 01

? 0x1835482
? 0x18366DE
? 0x18366CA
? 0x18366C7
? 0x18366C9
Debug Mode; 0x18366C4
? 0x1835481
? 0x18354CC


                                                                                         ---------------------------------
                                                                                         |Uncharted 4: A Thief's End 1.00|
---------------------                                                                    ---------------------------------
Debug Mode (Pre-Boot, See Offsets For Memory Patch)

F; c6 80 95 2e 00 00 00
R; c6 80 95 2e 00 00 01
------------------------
L3 + Triangle FPS Toggle

F; 
R; 
------------------------
Super Pause To Manual Camera

F; 48 8d 35 be 0c d0 01
R; 48 8d 35 f3 27 d1 01
---
F; 48 8d 0d 0b 15 00 00
R; 48 8d 0d 6b df 2f 00
------------------------


Offsets:
Debug Mode 0x1104FC2E95
FPS 0x1104FC2E9D
Minimal FPS Display 0x1104FC2E9E
discname.txt data 0x1104FC2F18
                                                                                         ---------------------------------
                                                                                         |Uncharted 4: A Thief's End 1.32|
                                                                                         ---------------------------------


Debug Mode

F; C6 80 79 2E 00 00 00 EB
R; C6 80 79 2E 00 00 01 EB
---------------------------
Multiplayer Debug Mode

F; c6 80 7f 2e 00 00 01 c6 80 79 2e 00 00 00
R; c6 80 7f 2e 00 00 01 c6 80 79 2e 00 00 01
---------------------------------------------
Novis (Non-functional in 1.00 FFS)

F; c4 c1 78 11 85 a8 00 00 00 e8 d9 9e 3d 00 48 89 c3 48 8d 35 98 1a 6f 00 31 d2 48 89 df e8 55 2d 17 00 4c 8d 25 0e 31 9c 00 4c 8d 35 77 7f 17 00 c7 83 94 00 00 00 00 00 00 00 c7 83 98 00 00 00 03 00 00 00 48 8d 05 79 6e 5d 01 4c 89 ef 48 89 de 4c 89 23 4c 89 b3 a0 00 00 00 8a 0d 63 6e 5d 01 88 8b a8 00 00 00 48 89 43 58 c7 43 50 00 00 00 00 c7 83 90 00 00 00 01 00 00 00 e8 a6 7d 17 00 bf b0 00 00 00
R; c4 c1 78 11 85 a8 00 00 00 e8 d9 9e 3d 00 48 89 c3 48 8d 35 79 06 67 00 31 d2 48 89 df e8 55 2d 17 00 4c 8d 25 0e 31 9c 00 4c 8d 35 77 7f 17 00 c7 83 94 00 00 00 00 00 00 00 c7 83 98 00 00 00 03 00 00 00 48 8d 05 b4 ce a0 00 4c 89 ef 48 89 de 4c 89 23 4c 89 b3 a0 00 00 00 8a 0d 9e ce a0 00 88 8b a8 00 00 00 48 89 43 58 c7 43 50 00 00 00 00 c7 83 90 00 00 00 01 00 00 00 e8 a6 7d 17 00 bf b0 00 00 00
-------------------------------------------------------------------------------------------------------------------------------------------------------
L3 + Triangle FPS Toggle

F; ba 01 00 00 00 48 89 df 49 89 dc e8 49 69 70 01 84 c0 74 4e 41 80 bf 79 2e 00 00 00 74 44 41 8a 8f 7f 2e 00 00 80 f1 01 41 88 8f 7f 2e 00 00 41 0f b7 87 7e 2e 00 00 84 c0 74 27 c1 e8 08 41 88 8f 88 2e 00 00 41 88 87 dc 2e 00 00 88 c2 48 8b 0d 8c 83 f7 01 80 f2 01
R; ba 01 00 00 00 48 89 df 49 89 dc e8 49 69 70 01 84 c0 74 4e 41 80 bf 79 2e 00 00 00 74 44 41 8a 8f 88 2e 00 00 80 f1 01 41 88 8f 88 2e 00 00 41 0f b7 87 7e 2e 00 00 84 c0 74 27 c1 e8 08 41 88 8f 88 2e 00 00 41 88 87 dc 2e 00 00 88 c2 48 8b 0d 8c 83 f7 01 80 f2 01
-------------------------------------------------------------------------------------------------------------------------------------------------------

Debug Mode; 0x110491AE79

                                                                                         ---------------------------------
                                                                                         |Uncharted: The Lost Legacy 1.09|
                                                                                         ---------------------------------
Debug Mode


F; c6 80 f9 2e 00 00 00
R; c6 80 f9 2e 00 00 01
-----------------------
Debug Mode 0x1105D1AEF9
Disable Debug Rendering 0x1105D1AEFF
                                                                                         ---------------------------------
                                                                                         |Uncharted: The Lost Legacy 1.00|
                                                                                         ---------------------------------

Debug Mode

F; c6 80 f9 2e 00 00 00
R; c6 80 f9 2e 00 00 01
------------------------
Draw World Axes to Novis

F; 48 8d 35 98 51 73 00
R; 48 8d 35 59 fa 6a 00
-
F; 48 8d 05 0a 8b 65 01
R; 48 8d 05 75 2a a6 00
------------------------
L3 & Triangle Debug Rendering Toggle To FPS Toggle

F; 418a8fff2e000080f10141888fff2e0000 41 8a 8f ff 2e 00 00 80 f1 01 41 88 8f ff 2e 00 00
R; 418a8f082f000080f10141888f082f0000
--------------------------------------
NPC Scale 22b4160 ghidoffst
------------------------------------------------
Show Save Slot On Screen

F; c6 05 6e 67 fb 00 00
R; c6 05 6e 67 fb 00 01
------------------------
Menu Right Align Toggle

F; 44 72 61 77 20 57 6F 72 6C 64 20 41 78 65 73 20 28 43 61 6D 65 72 61 20 52 65 6C 61 74 69 76 65 29
R; 41 6C 69 67 6E 20 4D 65 6E 75 73 20 72 69 67 68 74 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20 20
- 
F; 48 8d 05 85 8a 65 01
R: 48 8d 05 64 70 b7 00
-------------------------------------------------------------------------------------------------------
Right By Default

F: c6 05 00 2e 0d 02 00
R: c6 05 00 2e 0d 02 01
------------------------
Restore UC4 Task Menu For Looks (illusion Told Me How To Renable It, I just Pointed Out That The Submenu Was Still There)
F: 80 bf c5 2e 00 00 00 41 0f 94 c5
R: 80 bf c5 2e 00 00 00 41 0f 95 c5
------------------------------------
[Menu Pause Toggles]

On open

F: 
R: 
-
On Close

F; 
R: 
-
No Pause By Default

F: c7 05 09 2e 0d 02 01 01 01 01
R: c7 05 09 2e 0d 02 01 01 00 00
------------------------
Toggle To Swap O and Square In Debug Menu

F: 
R: 
-
F: 
R: 
-
Swapped On Boot

F: c6 05 06 2e 0d 02 00
R: c6 05 06 2e 0d 02 01
------------------------
Enable Debug Rendering On Startup (Idk Which One Yet Lol, Just Do 'Em All)

F; c6 80 ff 2e 00 00 01
R; c6 80 ff 2e 00 00 00
------------------------
Force-Enable Msg Con in FINAL On Startup

F; c6 05 a1 19 0b 02 01
R; c6 05 9d 19 0b 02 01
------------------------
FPS Mode Set To Verbose On Boot

F; c7 83 04 2f 00 00 00 00 00 00
R; c7 83 04 2f 00 00 01 00 00 00
-
Enable Stat Posting On Boot

F; c6 83 65 32 00 00 00
R; c6 83 65 32 00 00 01
-
Offsets Lost Legacy 7737 1.00
Debug Mode; 0x1105D1AEF9
Disable Debug Rendering; 0x1105D1AEFF
Menu Pause On Open: 0x23ca338
Menu Pause On Exit: 0x23ca339
Right Align: 0x23CA33D
Pause Icon: 0x23CA33A
Swap O and Square: 0x23CA33C
NPC Scale 0x22b4160
-
NPC Scale:
Hex In Eboot: 00 00 80 3f 00 00 00 00 01 00 00 00 01 00 00 00 01 01 00 00 ef 01
Ghidra Address 22b4160
Eboot Address 22b8160
PS4 Cheater Address 26b4160
-
Write Value I didn't use yet
c6 05 86 06 09 02 01

[PS3 DEBUG MODE CODES BY illusion]

Uncharted 1
1.00 Disc 0x3e61c 409e
1.01 Disc 0x3b6ac 409e
PSN 0x3b5c4 419e

Uncharted 2
1.00 0x13c64, 419e
1.09 0x13c0c, 419e
Demo 0x87a18, 98c3
1.10 PSN 0x144e0, 419e

Uncharted 3
1.00 Disc 0x31e34 419e
1.19 Disc 0x32814 419e
1.10 GOTY 0x32624 419e


[PS4 DEBUG MODE CODES BY TheMagicalBlob]

Patch The .bin/.elf With The Hex Codes, OR Write [On 0x01] / [Off 0x00] To The Offset While The Game's Running. You Don't Need Both
---------------------------------
The Last of Us Remastered 1.00

Eboot Patch
F; C6 87 81 2E 00 00 00
R; C6 87 81 2E 00 00 01

Memory Edit
0x114ED32E81
------------
The Last of Us Remastered 1.09 to 1.11

Eboot Patch
F; c6 87 81 2e 00 00 00
R; c6 87 81 2e 00 00 01

Memory Edit
0x114F536E81
-------------
The Last of Us Part II 1.00

Eboot Patch
F; 31 c0 eb 49 4c
R; b0 01 eb 49 4c

Memory Edit
0x110693FAA1
------------
The Last of Us Part II 1.07 to 1.09

Eboot Patch
F; 31 c0 eb 4c 4c
R; b0 01 eb 4c 4c

Memory Edit
0x11069DFAA1
------------
Uncharted: The Nathan Drake Collection

Eboot Patch (All Three Games, Code's The Same. Apply To All Three Executables)
F; 80 bf ba 39 00 00 00
R; 80 bf ba 39 00 00 01

Memory Edit

Uncharted 1
Debug Menu: 0xD989CC|FPS Display: 0xD98970|Task Display: 0xD97B41
-
Uncharted 2
Debug Menus: 0x127149C|Task Display: 0x12705C9
-
Uncharted 3
Debug Menus: 0x18366C4|Task Display: 0x1835481
----------------------------------------------
Uncharted 4 1.00

Eboot Patch
F; c6 80 95 2e 00 00 00
R; c6 80 95 2e 00 00 01

Memory Edit
0x1104FC2E95
------------
Uncharted 4 1.32/1.33

Eboot Patch
F; C6 80 79 2E 00 00 00 EB
R; C6 80 79 2E 00 00 01 EB

Memory Edit
0x110491AE79
------------
Uncharted: The Lost Legacy 1.00

Eboot Patch
F; c6 80 f9 2e 00 00 00
R; c6 80 f9 2e 00 00 01

Memory Edit
0x1105D1AEF9
------------
Uncharted: The Lost Legacy 1.08/1.09

Eboot Patch
F; c6 80 f9 2e 00 00 00
R; c6 80 f9 2e 00 00 01

Memory Edit
0x1105D1AEF9
------------

Patches By TheMagicalBlob


TLOU Remastered:

1.00 (why'd you make me find this myself, anthony? XD)
F; F6 45 97 01 74 10
R; F6 45 97 01 75 10

Uncharted 2 PS3

1.00
Fix Bin Files... Submenu 0x90ce68

F; 7f e1 08 08 4b ff fd dc 38 7d 00 34
--
R; 60 00 00 00 4b ff fd dc 38 7d 00 34

<!---
TheMagicalBlob/TheMagicalBlob is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
