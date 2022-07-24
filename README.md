Hey There, I Make Things For PS4 Games.
I Mostly Screw With Debug Stuff.
You Can Find Me On Discord At TheMagicalBlob#9808, Or On Youtube At https://www.youtube.com/channel/UCqYd1YadQvjnAj_LfHK4iEQ 



**Below Is A List Of Codes I Made To Enable The Debug Mode\Menus In PS4 Last of Us/Uncharted Games. Might As Well Shove 'Em Here**

Use The Find\Replace-With On The Decrypted eboot.bin Or Write 0x01 To The Offset Below During Gameplay



**The Last of Us Remastered 1.00**

Eboot Patch

F; C6 87 81 2E 00 00 00

R; C6 87 81 2E 00 00 01

Memory Edit
0x114ED32E81

**The Last of Us Remastered 1.09 to 1.11**

Eboot Patch

F; c6 87 81 2e 00 00 00

R; c6 87 81 2e 00 00 01


Memory Edit
0x114F536E81

**The Last of Us Part II 1.00**

Eboot Patch

F; 31 c0 eb 49 4c

R; b0 01 eb 49 4c


Memory Edit
0x110693FAA1

**The Last of Us Part II 1.07 to 1.09**

Eboot Patch

F; 31 c0 eb 4c 4c

R; b0 01 eb 4c 4c

Memory Edit
0x11069DFAA1

**Uncharted: The Nathan Drake Collection**

Eboot Patch (All Three Games, Code's The Same. Apply To All Three Executables)

F; 80 bf ba 39 00 00 00

R; 80 bf ba 39 00 00 01

Memory Edit:

**Uncharted 1**
Debug Menu: 0xD989CC | FPS Display: 0xD98970 | Task Display: 0xD97B41

-

**Uncharted 2**
Debug Menus: 0x127149C | Task Display: 0x12705C9

-

**Uncharted 3**
Debug Menus: 0x18366C4 | Task Display: 0x1835481



**Uncharted 4 1.00**

Eboot Patch

F; c6 80 95 2e 00 00 00

R; c6 80 95 2e 00 00 01

Memory Edit
0x1104FC2E95


**Uncharted 4 1.32/1.33**

Eboot Patch

F; C6 80 79 2E 00 00 00 EB

R; C6 80 79 2E 00 00 01 EB

Memory Edit
0x110491AE79



**Uncharted: The Lost Legacy 1.00**

Eboot Patch

F; c6 80 f9 2e 00 00 00

R; c6 80 f9 2e 00 00 01

Memory Edit
0x1105D1AEF9


**Uncharted: The Lost Legacy 1.08/1.09**

Eboot Patch

F; c6 80 f9 2e 00 00 00

R; c6 80 f9 2e 00 00 01

Memory Edit
0x1105D1AEF9

<!---
TheMagicalBlob/TheMagicalBlob is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
