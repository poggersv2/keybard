# keybard Journal

## Entry 1: Layout Editor
**Time Spent:** 0.5 hours

![Layout Editor](https://github.com/poggersv2/keybard/blob/main/journal/assets/layout.png)

**What I did:** 
I started by generating layout for the board using Keyboard Layout Editor NG (https://editor.keyboard-tools.xyz/). I took a standard 60% layout and extended it to include the arrow key cluster and the side macro column, with spacing in between the macros and the keyboard to leave space for the Pico.
**What I got stuck on:** 
Figuring out how to space the macro keys and arrows so they look smooth with the rest of the board. It took a bit of tweaking before I was happy with the final layout.

---

## Entry 2: Schematic
**Time Spent:** 1.0 hours

![Schematic](https://github.com/poggersv2/keybard/blob/main/journal/assets/schematic.png)

**What I did:** 
I started to wiring up the schematic. I set up the Pico and added the 5x17 matrix for the switches. 
**What I got stuck on:** 
Making sure all the GPIO pins from the Pico matched up correctly with the rows and columns without any overlapping took some ages, and I had to quadruple check it because it was a little confusing.

---

## Entry 3: PCB
**Time Spent:** 2.0 hours

![PCB Arrangement](https://github.com/poggersv2/keybard/blob/main/journal/assets/arrangement.png)

**What I did:** 
I moved on to the actual PCB layout. I imported the JSON that I exported for KLE NG and used an extention to place the switch footprints for me. Then I arranged the Pico to where I wanted it and got to routing everything
**What I got stuck on:** 
Didn't get stuck on anything, but the alignment and grid system of KiCad was kindda hard to understand.

---

## Entry 4: Routing the PCB
**Time Spent:** 2.0 hours

![PCB Routing](https://github.com/poggersv2/keybard/blob/main/journal/assets/routing.png)

**What I did:** 
Spent AGES routing all the traces across the board and wiring the rows and columns back to the Pico's pins.
**What I got stuck on:** 
Routing the matrix to make it actually work while also trying to keep the traces looking decent was definitely one of the hardest parts.

---

## Entry 5: Case Design (Plate)
**Time Spent:** 2.0 hours

![Plate Sketch](https://github.com/poggersv2/keybard/blob/main/journal/assets/plate_sketch.png)

![Switch Plate](https://github.com/poggersv2/keybard/blob/main/journal/assets/plate_extruded.png)

**What I did:** 
Started learning CAD completely from scratch using Fusion. I started by importing the plate I downloaded from KLE NG. I added tolerances and the outer case and extruded it by 1.5mm
**What I got stuck on:** 
I had zero experience with Fusion, so just figuring out the UI and the basic tools took up a long time.

---

## Entry 6: Case Design (Bezel / Top)
**Time Spent:** 1.5 hours

![Top Bezel](https://github.com/poggersv2/keybard/blob/main/journal/assets/bezel.png)

**What I did:** 
Extruded the top bezel pieces to frame the keyboard. I had to account for the height of the switches and keycaps so the board looks nice. I added a chamfer to the edges so it's not sharp
**What I got stuck on:** 
Distances and tolerances were super hard to imagine the actual physical size of everything on a screen, and doing the math for the clearance gaps and spacings was hard at first.

---

## Entry 7: Case Design (Bottom & Assembly)
**Time Spent:** 2.0 hours

![Case Bottom](https://github.com/poggersv2/keybard/blob/main/journal/assets/bottom.png)

![Case Bottom Back](https://github.com/poggersv2/keybard/blob/main/journal/assets/bottom_back.png)

![Left Half](https://github.com/poggersv2/keybard/blob/main/journal/assets/left_half.png)

![Right Half](https://github.com/poggersv2/keybard/blob/main/journal/assets/right_half.png)

![Two Halves Assembled](https://github.com/poggersv2/keybard/blob/main/journal/assets/two_halves.png)

**What I did:** 
Finished off the case by designing the bottom plate and adding all the mounting holes so it can actually be screwed together. Then I exported everything for manufacturing. I had to split the case into 6 seperate parts because it didn't fit on a 3d printer plate.

**What I got stuck on:** 
Using the right tools.

---

## Entry 8: Firmware Setup
**Time Spent:** 1.5 hours

![Firmware Code](https://github.com/poggersv2/keybard/blob/main/journal/assets/firmware.png)

**What I did:** 
I set up the RMK firmware framework using GitHub Actions so it just compiles on Github. I mapped the matrix in `keyboard.toml` to match my schematic and set up the default layout and macros in `vial.json`. 
**What I got stuck on:** 
Mapping the keys was kindda confusing.

# Total Time Spent: `15.5` Hours